---
name: raptive-creator-api
description: Raptive Creator API for analyzing ad traffic, revenue, and performance data
---

# Raptive Creator API Skill

The Raptive Creator API lets publishers and creators pull their Raptive dashboard data into external tools — spreadsheets, BI platforms, custom dashboards — using OAuth 2.0 credentials generated from the Raptive dashboard.

## When to Use This Skill

Use this skill when you need to:

- **Integrate Raptive data into external tools** — connecting Raptive revenue/performance data to Google Sheets, Looker Studio, Power BI, Notion, or similar platforms
- **Build custom dashboards** — pulling ad revenue, RPM, traffic, and performance metrics alongside other business data
- **Generate or manage API tokens** — creating, rotating, or revoking Raptive Creator API credentials
- **Understand data access scope** — knowing which dashboard reports are available via API vs. dashboard-only
- **Automate reporting** — scripting periodic pulls of Raptive metrics for custom workflows
- **Debug API connection issues** — troubleshooting authentication failures, expired credentials, or permission errors

**Not needed if:** You're satisfied with the native Raptive dashboard reports — the API is optional and additive.

## Key Concepts

### Access Tiers
The Raptive Creator API is available to sites on these plans:
- **Insider**
- **Platinum**
- **Platinum Elite**
- **Luminary**

Standard/free tier sites do not have API access.

### Authentication Model
The API uses a **Client ID + Client Secret** pair (OAuth 2.0 style). Both are required to authenticate. Key rules:

- The **Client Secret is shown only once** at creation — copy and store it immediately
- Each user account supports up to **16 active API credentials**
- Credentials **expire after 365 days** from creation (unless revoked earlier)
- Deleting a token **immediately revokes API access** for that credential
- Access is **permission-scoped to the user** — the API can only access sites and reports that the credential-owning user can see in the dashboard

### Data Access Scope
The API exposes data from Raptive dashboard reports (exact report list subject to change as Raptive expands API coverage). Access is gated by your dashboard permissions — if your user can't see a report in the dashboard, you can't pull it via API.

## Quick Reference

### Creating API Tokens (Dashboard UI)

1. Log into your Raptive dashboard
2. Navigate to **Account Settings → Raptive Creator API**
3. Click **"Create token"** and give it a name
4. Copy both the **Client ID** and **Client Secret** immediately (secret won't be shown again)
5. Use these credentials in your third-party tool's API connection settings

### Token Lifecycle Management

| Action | Effect |
|--------|--------|
| Create token | Generates new Client ID + Client Secret pair |
| Delete token | Immediately blocks all API access for that credential |
| Token expires | After 365 days from creation — must create a new token |
| Max tokens | 16 active credentials per user account |

### Typical OAuth 2.0 Token Exchange (Pseudocode)

```python
import requests

# Exchange client credentials for an access token
response = requests.post(
    "https://api.raptive.com/oauth/token",  # verify exact endpoint in public API docs
    data={
        "grant_type": "client_credentials",
        "client_id": "YOUR_CLIENT_ID",
        "client_secret": "YOUR_CLIENT_SECRET",
    }
)
access_token = response.json()["access_token"]
```

> **Note:** Verify the exact token endpoint URL in Raptive's public API documentation — the pattern above reflects standard OAuth 2.0 client credentials flow.

### Making an Authenticated API Request (Pseudocode)

```python
headers = {"Authorization": f"Bearer {access_token}"}

# Pull dashboard report data
data = requests.get(
    "https://api.raptive.com/v1/reports/revenue",  # verify exact endpoint
    headers=headers,
    params={"start_date": "2025-01-01", "end_date": "2025-01-31"}
).json()
```

### Google Sheets / Looker Studio Integration Pattern

```
1. Generate Client ID + Client Secret in Raptive dashboard
2. In your tool's data connector settings, locate "Raptive" or "OAuth2 / API Key" connection
3. Enter Client ID and Client Secret
4. Authorize the connection
5. Select which reports/metrics to pull
6. Set refresh schedule (daily recommended for revenue data)
```

## Reference Files

| File | Contents | Source | Confidence |
|------|----------|--------|------------|
| `references/other.md` | Overview of API access, token creation, use cases, and FAQ from official Raptive Help Center | Official Raptive documentation | Medium |
| `references/index.md` | Index of all reference files in this skill | Auto-generated | Medium |

**Note:** This skill currently has one source document (the Raptive Help Center overview article). The public API reference docs (endpoints, request/response schemas) are linked from that article but were not scraped — consult Raptive's public API documentation directly for endpoint-level details.

## Working with This Skill

### Beginners — Start Here
1. Read `references/other.md` for the overview: what the API is, who can access it, and how to create tokens
2. Use the **Token Lifecycle Management** table above to understand credential rules
3. Follow the **Dashboard UI steps** to generate your first Client ID + Client Secret

### Intermediate — Building Integrations
1. Use the pseudocode examples above as a pattern for OAuth 2.0 client credentials flow
2. Check Raptive's public API documentation (linked from your dashboard's API settings) for exact endpoint URLs, parameters, and response schemas
3. Scope your integration to the reports your dashboard user has permission to view

### Advanced — Custom Dashboards & Automation
1. Token management: plan for annual rotation (365-day expiry) and stay under the 16-credential limit
2. Build a token refresh/rotation mechanism into long-lived integrations
3. Scope API users carefully — each token inherits the creating user's data access permissions, so use a dedicated API user with minimum necessary permissions for automated pipelines

## Common Use Cases

- **Revenue reporting alongside ad spend** — combine Raptive RPM/revenue data with Google Ads cost data in a single dashboard
- **Multi-site publisher rollups** — aggregate performance across multiple Raptive-monetized sites
- **Automated weekly/monthly reports** — email or Slack digest of key revenue metrics
- **Anomaly alerting** — flag unusual RPM drops or traffic spikes against revenue baselines
- **Integration with accounting tools** — pull revenue data into QuickBooks, Wave, or spreadsheet-based bookkeeping

## FAQ

**Q: Do I need the API?**
No — it's optional. If the built-in Raptive dashboard meets your reporting needs, skip the API.

**Q: Does Raptive support third-party tool integrations directly?**
No — Raptive does not officially support third-party tools. For implementation help, they recommend contacting a developer or posting in the Raptive Facebook group.

**Q: What happens when my token expires?**
After 365 days, the credential stops working. Create a new token in Account Settings and update your integrations with the new credentials.

**Q: Can multiple users share one token?**
Technically yes (if they have the credentials), but each token is permission-scoped to the user who created it. Best practice is for each integration to use a dedicated token from an appropriately-permissioned user.

**Q: Will more data become available via the API?**
Yes — Raptive has stated they plan to make additional data available in future API releases.

## Notes

- Source: Official Raptive Help Center article (confidence: medium — overview-level, not full API reference)
- No code examples exist in the source documentation; pseudocode above is inferred from standard OAuth 2.0 patterns
- For exact endpoint URLs, request/response schemas, and rate limits, consult Raptive's public API documentation linked from your dashboard

## Updating

To refresh this skill with updated documentation:
1. Re-run the scraper targeting the Raptive Help Center article and Raptive's public API reference
2. The skill will be rebuilt with the latest information
