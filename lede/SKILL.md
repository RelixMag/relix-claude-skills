---
name: lede
description: Lede platform documentation - CMS and publishing tools for media companies
---

# Lede Skill

Lede is a CMS and publishing platform for media companies. It integrates WordPress (content), Beehiiv (email newsletters), Beacon (analytics), and Stripe (subscriptions) into a unified publisher stack with a central Publisher App for configuration.

## When to Use This Skill

Use when asked about:
- **Paywalls & content gating** — registration walls, paywall configuration, category overrides
- **Subscriber management** — free vs. paid subscriptions, gift subscriptions, coupon/promo codes
- **Email newsletters** — Beehiiv integration, automations, opt-in/opt-out, newsletter sync
- **Analytics** — Beacon analytics, traffic reports, conversion/revenue reports
- **Revenue** — ad blocker detection, ad campaigns/sponsorships, intro pricing
- **WordPress content creation** — post/page blocks, author bylines, ticker block, reusable blocks
- **Site configuration** — WordPress admin settings, theme options
- **MCP integration** — connecting Claude/AI tools to Lede via the MCP endpoint
- **API usage** — subscriber preferences, unsubscribe requests
- **Integrations** — Coral (commenting), GAM (Google Ad Manager)

**Do NOT use** for general WordPress or Beehiiv questions unrelated to the Lede platform.

## Quick Reference

### MCP Integration

Connect Claude or other AI tools to Lede via its MCP server:

```json
{
  "mcpServers": {
    "lede": {
      "type": "http",
      "url": "https://app.joinlede.com/mcp"
    }
  }
}
```

### Key Platform Facts

| Concept | Detail |
|---|---|
| Publisher App | Central admin at `app.joinlede.com` — products, analytics, newsletter settings |
| Beacon analytics | First-party, event-based; **not real-time** — caches up to 6 hours, ends yesterday |
| Unique Users | Count of distinct browser IDs; **not additive** across days — change date range instead |
| Sessions | End after 30 min inactivity; don't reset at midnight (unlike GA) |
| Newsletters | Managed via Beehiiv; synced automatically when created/updated in Publisher App |
| Beehiiv automations | Must have active "Add by API" trigger or Lede enrollment is rejected |
| Gift subscriptions | Available platform-wide; specialty products can be excluded via support ticket |
| Discount/promo timing | Notify Lede **24 hours in advance** before activating on production |
| Ad blocker hard mode | Requires soft mode to be enabled first |
| Dates in Beacon | All UTC — "day" = 00:00–23:59 UTC, not local midnight |

### Paywall / Content Gating

- Configure registration walls and paywalls in the Publisher App
- Category-specific overrides are available
- Ad blocker detection has soft mode (dismissible banner) and hard mode (full content gate)
- Hard mode CTA adapts to reader's state (anonymous / registered / subscriber)

### Beehiiv Automation Setup

1. In Beehiiv: create automation with an active **"Add by API" trigger**
2. In Publisher App → Settings → Newsletter Options: assign automations per product or for free registrations
3. Lede enrolls subscribers at the moment of registration or purchase
4. Separate automations can be assigned per product (e.g., annual vs. gift)

### WordPress Content Blocks (Lede-specific)

- **Ticker Block** — scrolling marquee text, available on pages/reusable blocks (not posts); pause/play accessible; reduced-motion users see static text
- **Featured Post Block** — configurable spotlight block
- **Media Card Block** — rich media card layout
- **Engagement Block** — reader interaction elements
- **Affiliate Block** — affiliate link management
- **Custom Embed Block** — extended embed support beyond core WordPress

## Reference Files

All reference files are in `references/`:

| File | Content | Pages |
|---|---|---|
| `analytics.md` | Beacon analytics system — what it tracks, how Unique Users/Sessions are counted, report types, known limitations | 5 pages |
| `api.md` | Subscriber preferences and unsubscribe request handling via API | 1 page |
| `creating-content-wordpress-admin.md` | All Lede-specific WordPress blocks (Ticker, Featured Post, Media Card, Engagement, Affiliate, Embed), author bylines, reusable blocks, page layout options | 27 pages |
| `email-newsletters-beehiiv.md` | Newsletter structure, Beehiiv sync, opt-in/opt-out, creating newsletters, paid tiers, Beehiiv automations, segments | 10 pages |
| `emails-legacy-sendgrid-docs.md` | Legacy SendGrid email documentation (older infrastructure) | ~40 pages |
| `integrations-coral-gam.md` | Coral (commenting) and Google Ad Manager integrations | — |
| `other.md` | Miscellaneous platform documentation | — |
| `publisher-dashboard.md` | Publisher App navigation, dashboard features | — |
| `site-configuration-wordpress-admin.md` | WordPress admin site configuration, theme settings | — |
| `user-revenue-generation.md` | Ad blocker detection, sponsorships/ad campaigns, content gate overrides, gift articles, gift subscriptions, promotional/intro pricing, paywall configuration | 10 pages |

## Key Concepts

**Beacon (Analytics):** Lede's own first-party analytics. Events are batched, not real-time. Reports cache for up to 6 hours. Purchase events arrive from both browser and server — the de-duplicated view counts each purchase exactly once. The standalone Beacon dashboard at `app.ledebeacon.com` has been retired — everything is in Publisher App.

**Newsletter vs. Beehiiv:** Lede manages newsletters as a concept (who is subscribed to what). Beehiiv is the sending platform. Lede creates custom fields in Beehiiv automatically and syncs preferences bidirectionally.

**Default Newsletter:** Every publisher has one; new subscribers are automatically opted into it. Additional newsletters require explicit opt-in.

**Product Groups:** Subscription products are organized in product groups. Specialty product groups can be excluded from gift subscriptions.

**Content Gates:** Lede supports both registration walls (free account required) and paywalls (paid subscription required). Per-category overrides let publishers gate specific sections differently from the default.

## Working with This Skill

### For a specific feature
Read the matching reference file directly — e.g., questions about Beehiiv automations → `references/email-newsletters-beehiiv.md`.

### For analytics questions
Start with `references/analytics.md`. Most common gotchas (non-additive Unique Users, UTC dates, 6-hour cache) are documented there.

### For revenue/monetization questions
`references/user-revenue-generation.md` covers ad blocker detection, paywalls, gifting, and promo pricing end-to-end.

### For WordPress content questions
`references/creating-content-wordpress-admin.md` is the largest file (27 pages) — use the Contents sections at the top of each article to navigate.

### For email/newsletter setup
`references/email-newsletters-beehiiv.md` covers the current Beehiiv integration. Use `references/emails-legacy-sendgrid-docs.md` only for legacy/historical SendGrid context.

## Source Notes

- All documentation sourced from official Lede docs at `docs.joinlede.com`
- Confidence: medium (scraped from official docs, no codebase cross-validation)
- No conflicting sources — single official documentation source

## Updating

To refresh with latest documentation:
1. Re-run the scraper with the same configuration
2. The skill will be rebuilt with the latest information
