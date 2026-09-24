# Relix Claude Skills

Claude Code skills for the Relix team. These skills extend Claude's capabilities with Relix-specific workflows and general marketing/SEO tools.

## How to Install

### Option A — Clone and symlink (recommended for teams)
```bash
git clone https://github.com/RelixMag/relix-claude-skills.git ~/relix-skills
```
Then in Claude Code settings, point your skills directory to `~/relix-skills`.

### Option B — Copy individual skills
Copy any skill folder into your Claude skills directory:
- **Mac (Claude Code CLI):** `~/.claude/skills/`
- **Claude Desktop:** `~/Library/Application Support/Claude/skills/`

## Skills

### Relix-specific
| Skill | Description |
|-------|-------------|
| `lede` | Lede CMS workflows — creating content, analytics, API reference |
| `raptive-creator-api` | Pull Raptive ad revenue data via the Creator API |
| `seo-audit` | SEO audit workflow using Google Search Console + GA4 |
| `programmatic-seo` | Programmatic SEO content generation |
| `email-processor` | Process and analyze email/ticket buyer lists |

### General tools
| Skill | Description |
|-------|-------------|
| `competitive-ads-extractor` | Extract and analyze competitor ads from ad libraries |
| `skill-seekers` | Generate new skills from documentation |
| `task-observer` | Task tracking and progress monitoring |

### Marketing skills (50 skills in `marketingskills-ALL/`)
A full suite of marketing skills covering: ads, analytics, copywriting, CRO, email, SEO, social, and more. Originally from [Corey Haines' marketingskills repo](https://github.com/coreyhainesco/marketingskills).

### Superpowers skills (`superpowers-ALL/`)
Process skills for working with Claude effectively: brainstorming, planning, debugging, code review, and more.

## Contributing

To add or update a skill, open a PR. Each skill needs a `SKILL.md` file at its root.
