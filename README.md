# AskGSC — Google Search Console MCP for ChatGPT, Claude & AI assistants

**Ask questions about your Google Search Console data directly from ChatGPT, Claude, and other MCP-compatible assistants.** AskGSC is a hosted, read-only [Model Context Protocol (MCP)](https://modelcontextprotocol.io/) server with 11 tools for SEO performance analysis, query and page research, period comparisons, indexing checks, and sitemap diagnostics.

**Website:** [askgsc.app](https://askgsc.app/) · **Start free:** [Connect Google Search Console](https://askgsc.app/connect) · **MCP server:** `https://mcp.askgsc.app/mcp` · **Pricing:** [Free and Pro](https://askgsc.app/pricing)

> **Documentation repository, not the AskGSC application source code.** The hosted service is operated by AskGSC. You don't need to clone this repository, install packages, host an MCP server, or manage Google API credentials.

## What can AskGSC do?

AskGSC allows your AI assistant to retrieve Google Search Console data for properties you have permission to view:

- **SEO performance:** clicks, impressions, CTR, and average position across time.
- **Search queries and pages:** identify traffic drivers, declining pages, and emerging queries.
- **Segmentation:** analyze by page, query, date, country, device, and other supported Search Console dimensions.
- **Before/after comparisons:** compare periods and find where changes are concentrated.
- **SEO opportunities:** investigate high-impression/low-CTR pages and potential query-to-page overlaps.
- **Technical signals:** inspect Google's last-known URL indexing information and submitted sitemap warnings.

Everything runs through **read-only Google OAuth access**. AskGSC cannot modify your Search Console properties, submit URLs for indexing, or edit your website.

## Connect Google Search Console to ChatGPT or Claude

1. Open **[askgsc.app/connect](https://askgsc.app/connect)** and sign in with the Google account that can access your Search Console property.
2. Approve the read-only Google Search Console permission and select an authorized property.
3. In an AI assistant that supports custom remote MCP servers, add AskGSC as a connector. Paste the MCP URL below and complete its OAuth authorization.
4. Ask your assistant a question about your Search Console data.

```text
https://mcp.askgsc.app/mcp
```

Custom MCP availability and setup menus depend on the AI client, plan, and workspace. The remote server is **not** an npm package or a command to execute locally.

**Cursor plugin:** [Cursor installation guide](docs/cursor.md) · **Setup guides:** [Getting started](docs/getting-started.md) · [ChatGPT](docs/chatgpt.md) · [Claude](docs/claude.md) · [Troubleshooting](docs/troubleshooting.md)

## Example Google Search Console prompts

Use a precise site/property and a complete date range to get more useful answers:

```text
List my available Google Search Console properties and help me pick the right one.
```

```text
For [PROPERTY], compare the most recent complete 28 days with the preceding
28 days. Which pages lost the most clicks? Show both periods and note data gaps.
```

```text
For [PROPERTY], find query–page pairs with strong impressions but low CTR.
Give me five opportunities to investigate, with the underlying GSC metrics.
```

```text
For [PROPERTY], check Google's last-known indexing status for [PAGE URL].
Explain any canonical, crawl or indexing signals worth investigating.
```

More examples: [15 practical SEO prompts](docs/prompts.md) · [SEO workflows](docs/use-cases.md).

## The 11 MCP tools

| MCP tool | What it helps you do |
| --- | --- |
| `gsc_list_properties` | Find authorized Search Console properties |
| `gsc_query_search_analytics` | Explore metrics by query, page, date, country, device, and filters |
| `gsc_compare_periods` | Compare performance between two date ranges |
| `gsc_overview` | Get a Search Console performance overview and trends |
| `gsc_opportunities` | Identify candidate SEO and CTR opportunities |
| `gsc_content_decay` | Find pages with observed click declines |
| `gsc_cannibalization` | Surface queries shared by multiple URLs for investigation |
| `gsc_page_diagnosis` | Diagnose a URL using performance and indexing signals |
| `gsc_inspect_url` | Read Google's last-known URL indexing status |
| `gsc_inspect_urls` | Check indexing signals for a small batch of URLs |
| `gsc_sitemaps` | Review submitted sitemap errors and warnings |

[Read the MCP tool reference](docs/mcp-tools.md)

## Who is it for?

- **SEO specialists:** investigate rankings, CTR, query changes, and technical signals without exporting spreadsheets.
- **SaaS founders:** decide which existing pages deserve attention before producing more content.
- **Content teams:** identify topics and refresh candidates from their own Search Console data.
- **Developers and AI-assisted workflows:** bring search performance evidence into compatible conversational tools.

## Pricing

AskGSC starts with a **14-day full-access trial, no credit card required**. After the trial, Free is available with **20 MCP credits/month by default**; the actual allowance is shown in your account. **Pro costs €4.99/month** with no AskGSC monthly credit cap while active, subject to Google and infrastructure limits. **The free trial does not automatically convert to paid.** See [current pricing](https://askgsc.app/pricing).

## Important limitations

Google Search Console is not a real-time ranking tracker. Its data may be delayed or incomplete, and some queries are anonymized or omitted. Average position is not a live SERP position. Indexing inspection reflects **Google's last-known state**, not a live crawl. Query overlap is not proof of SEO cannibalization. AskGSC provides data and deterministic analyses; your AI assistant interprets them, and **you** make the SEO decisions.

Read [Data, permissions, and limitations](docs/privacy-and-limitations.md).

## Documentation

| Guide | Topic |
| --- | --- |
| [Getting started](docs/getting-started.md) | Connect Google, choose a property, add remote MCP |
| [ChatGPT setup](docs/chatgpt.md) | Use Search Console in ChatGPT via MCP |
| [Claude setup](docs/claude.md) | Use Search Console in Claude via MCP |
| [MCP tool catalog](docs/mcp-tools.md) | All 11 tools, capabilities, and limits |
| [SEO workflows](docs/use-cases.md) | Traffic losses, CTR, opportunities, indexing |
| [SEO prompt library](docs/prompts.md) | Ready-to-adapt prompts |
| [Troubleshooting](docs/troubleshooting.md) | Authentication, missing properties, missing data |
| [Privacy and limitations](docs/privacy-and-limitations.md) | Read-only access and analytical caveats |
| [Documentation en français](README.fr.md) | Présentation et connexion en français |

**Further reading:** [AskGSC integrations](https://askgsc.app/integrations) · [Official AskGSC ChatGPT guide](https://askgsc.app/connect-google-search-console-chatgpt) · [Google Search Console prompt library](https://askgsc.app/prompts/google-search-console)

AskGSC is an independent service and is **not affiliated with Google, OpenAI, or Anthropic**.
