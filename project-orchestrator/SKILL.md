---
name: project-orchestrator
description: >
  Use when given a numbered list of action items to plan and execute a
  multi-step project. Classifies each task by owner (agent vs. human) and
  timing (parallel vs. sequential), creates git branches for human tasks,
  builds a TASKS.md tracker, creates a Claude Code task list, and outputs
  an execution plan with agent dispatch instructions. Trigger phrases: "plan
  this," "break this into tasks," "help me execute these," "set this up,"
  "I have X steps to do," "organize this project," "what should run in
  parallel," "create a task list from this."
---

# Project Orchestrator

Use this skill when given a numbered list of action items for a multi-step project. It produces: a classified task list, a TASKS.md reference file, git branches for human-owned tasks, a Claude Code task list, and a ready-to-execute plan with agent dispatch.

---

## Step 1: Read and Confirm the Task List

Before classifying, restate the list back in your own words to confirm you understood every item. If anything is ambiguous (unclear owner, unclear dependency), ask one focused question before proceeding. Do not classify tasks you're unsure about — ask first.

---

## Step 2: Classify Each Task

Ask two questions per task:

### Q1 — Who does this?

| Owner | Criteria | Action |
|-------|----------|--------|
| `agent` | Claude can execute autonomously: research, data pulls, API calls, analysis, writing first drafts, running scripts | Dispatch as subagent |
| `human` | Requires human judgment, authority, relationships, credentials only the human has, or physical action | Create a git branch for this task |

**When to ask instead of guess:** If a task could go either way (e.g., "review the vendor contract" — is this Claude reading a doc, or Carly making a decision?), ask before assigning.

### Q2 — When can it start?

| Timing | Criteria |
|--------|----------|
| `parallel` | Independent — needs no output from any other task before it starts |
| `sequential` | Depends on the output or completion of another specific task |

**Default to sequential when uncertain.** Parallel tasks that secretly share state cause race conditions and overwritten outputs.

### Combined Classifications

- `agent-parallel` — Claude runs it now, alongside other parallel tasks
- `agent-sequential` — Claude runs it after its dependency completes
- `human-parallel` — Carly can start it now, in its own branch
- `human-sequential` — Carly starts it after its dependency completes

---

## Step 3: Build TASKS.md

Create `TASKS.md` in the project's working directory. If working inside a named project folder, create it there. Format exactly:

```markdown
# [Project Name] — Task Tracker
Started: [YYYY-MM-DD]  |  Status: 🔄 In Progress

## Summary
Total: N  |  Done: 0  |  In Progress: 0  |  Blocked: 0

## Tasks

| ID  | Task | Owner | Timing | Branch | Depends On | Status | Notes |
|-----|------|-------|--------|--------|------------|--------|-------|
| T01 | [description] | agent | parallel | — | — | ⏳ todo | — |
| T02 | [description] | human | parallel | task/T02-description | — | ⏳ todo | — |
| T03 | [description] | agent | sequential | — | T01 | ⏳ todo | — |
| T04 | [description] | human | sequential | task/T04-description | T02 | ⏳ todo | — |

## Status Key
⏳ todo  |  🔄 in-progress  |  ✅ done  |  ❌ blocked  |  ⏭ skipped
```

Rules:
- IDs are `T01`, `T02`, ... in the original list order
- Branch column is `—` for agent tasks
- Depends On lists the IDs this task must wait for, comma-separated if multiple; `—` if none
- Notes are empty to start; filled in as work completes

---

## Step 4: Create Claude Code Task List

After writing TASKS.md, use TaskCreate for each item. Task name format: `T01: [task description]`. This keeps Claude Code's native task panel in sync with TASKS.md.

---

## Step 5: Create Git Branches for Human Tasks

For every task classified as `human`, create a branch and immediately return to the base branch:

```bash
git checkout -b task/T02-kebab-description
git checkout -        # return to previous branch
git checkout -b task/T04-kebab-description
git checkout -
```

**Naming convention:** `task/[ID]-[kebab-case-description]`
Examples: `task/T02-review-vendor-proposals`, `task/T04-approve-final-copy`

- Keep descriptions short (3-5 words max)
- Use only lowercase letters, numbers, hyphens
- If the repo has no git history yet, initialize: `git init && git commit --allow-empty -m "init"`
- If this is not a git repo and branching doesn't make sense (e.g., a pure research project with no files), skip branch creation and note it in TASKS.md

After creating all branches, update the Branch column in TASKS.md.

---

## Step 6: Output the Execution Plan

Present three sections in your response:

### Agent Launch Block
List all `agent-parallel` tasks that will be dispatched now. For each, write the exact prompt you'll send to the agent, including: the task goal, what files/context to read, and the instruction to update TASKS.md on start and finish.

```
Dispatching agents now (in parallel):

T01: [task name]
Prompt: "Update T01 in TASKS.md to 🔄 in-progress. [Task instructions.] 
When complete, update T01 to ✅ done and add a one-line result summary in Notes."

T03: [task name]
Prompt: "..."
```

### Human Work Queue
List all human tasks with their branch and when they can start.

```
Your tasks (branches created):

▶ Start now:
  - task/T02-description → [what to do]

⏸ Wait for [T01] first:
  - task/T04-description → [what to do after T01 is done]

Check out each branch when you're ready. Update TASKS.md status as you go:
🔄 when you start, ✅ when done, ❌ if blocked (with reason in Notes).
```

### Sequential Agent Queue
List any `agent-sequential` tasks in dependency order.

```
After agents complete, I'll run:

T05 (depends on T01, T02): [what it will do and what input it needs]
T07 (depends on T05): [...]
```

---

## Status Update Protocol

Every task — whether run by Claude, an agent, or Carly — follows this protocol:

1. **Before starting:** Edit TASKS.md, change status to `🔄 in-progress`, update Summary counts
2. **On completion:** Change status to `✅ done`, add a one-line outcome in Notes, update Summary counts
3. **On failure or block:** Change status to `❌ blocked`, add reason and next step in Notes

Agents receive this protocol in their dispatch prompt. Carly receives it in the Human Work Queue section.

---

## Anti-Patterns

| Mistake | Why it fails | Fix |
|---------|-------------|-----|
| Classifying a decision task as `agent` | Claude can gather info but can't make judgment calls that require human authority or context | Reclassify as `human`; brief the agent to prepare materials instead |
| Running parallel tasks that write to the same output file | Both overwrite each other | Make them sequential, or split outputs and merge at the end |
| Skipping TASKS.md and going straight to agents | No shared state; can't track what happened | Always create TASKS.md first |
| Creating branches in a non-git directory without asking | `git init` changes the project setup unexpectedly | Check for `.git` first; ask before initializing |
| Using vague branch names like `task/T02-stuff` | Makes the branch meaningless in a week | Use descriptive 3-5 word names: `task/T02-review-sponsor-deck` |
| Dispatching sequential agents in parallel | Agent B runs before Agent A's output exists | Respect the Depends On column |

---

## Quick Reference: Decision Tree

```
For each task:
  └─ Can Claude execute this without human judgment?
       ├─ Yes → owner: agent
       │    └─ Does it need another task's output first?
       │         ├─ Yes → agent-sequential (note dependency)
       │         └─ No  → agent-parallel (dispatch now)
       └─ No  → owner: human
            └─ Create branch: task/[ID]-[description]
            └─ Does it need another task's output first?
                 ├─ Yes → human-sequential (note dependency)
                 └─ No  → human-parallel (Carly can start now)
```
