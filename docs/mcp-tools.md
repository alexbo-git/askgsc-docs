# AskGSC MCP tools: Google Search Console analytics for AI assistants

[← Documentation home](../README.md)

AskGSC exposes **11 read-only tools** through its hosted MCP server at `https://mcp.askgsc.app/mcp`. Your AI client decides which tools to call based on your request.

| Tool | Purpose | Example question |
| --- | --- | --- |
| `gsc_list_properties` | Discover accessible GSC properties | “Which properties can I analyze?” |
| `gsc_query_search_analytics` | Retrieve clicks, impressions, CTR, position with dimensions and filters | “Show mobile clicks in France by month.” |
| `gsc_compare_periods` | Compare two windows using consistent dimensions and filters | “What changed since last month?” |
| `gsc_overview` | Summarize metrics, daily trends and optional segment breakdowns | “Give me a 28-day performance overview.” |
| `gsc_opportunities` | Find candidate query–page opportunities using CTR, impressions and position | “Which pages deserve a CTR review?” |
| `gsc_content_decay` | Surface pages showing observed click declines between samples | “Which pages are losing clicks?” |
| `gsc_cannibalization` | Find query overlap between multiple pages | “Which URLs show up for the same queries?” |
| `gsc_page_diagnosis` | Combine a page's performance, top queries and URL indexing signals | “What is happening with this URL?” |
| `gsc_inspect_url` | Request Google's last-known indexed URL information | “What does Google know about this URL's indexing?” |
| `gsc_inspect_urls` | Inspect a small batch of URLs (up to 10) | “Check these five pages.” |
| `gsc_sitemaps` | Review submitted sitemaps and reported errors or warnings | “Which sitemaps need attention?” |

## Metrics and dimensions

The Search Analytics tools work with these core Google Search Console metrics:

- **Clicks:** clicks reported by Search Console (not GA4 sessions).
- **Impressions:** search appearances reported by Search Console (not monthly keyword search volume).
- **CTR:** clicks divided by impressions, within the requested data scope.
- **Average position:** an impression-weighted Search Console metric, not a live fixed ranking.

Supported analysis dimensions include queries, pages, dates, countries, devices and search appearance. Search type and filters are available where supported by the Google API. Time-based analysis can aggregate into daily, weekly, monthly, quarterly or yearly summaries, subject to the source data and tool parameters.

## SEO analysis tools explained

### `gsc_overview`

An at-a-glance comparison for a specified site and period: current and previous clicks, impressions, CTR, average position and a trend series. Optional country/device breakdowns help locate where changes happened.

### `gsc_opportunities`

Ranks **candidate query–page pairs** based on observed Search Console signals. It does not predict extra traffic or guarantee a ranking improvement.

### `gsc_content_decay`

Highlights matched pages with substantial observed click declines across comparable periods. A page missing from the newer sample is **not** automatically treated as zero clicks.

### `gsc_cannibalization`

Surfaces queries that appear on multiple pages. **Query overlap is not proof of harmful cannibalization**; different URLs may legitimately rank for the same search intent.

### `gsc_page_diagnosis`

Provides an exact URL's recent performance, important visible queries and available indexing information. It is **not** an HTML crawler or a full technical SEO audit.

### `gsc_inspect_url` and `gsc_inspect_urls`

Inspect Google's **last-known indexing state** for one or a small set of URLs. Signals can include Google-selected canonical, indexing verdict, crawler, robots and last crawl. These tools cannot run a live indexability test or request indexing.

### `gsc_sitemaps`

Reviews the sitemap records and errors/warnings that Search Console exposes. The number of submitted sitemap URLs does **not** equal the number indexed by Google. AskGSC does not submit or edit sitemaps.

## API and data caveats

- Google data may be delayed or preliminary for recent dates.
- Query-level and page-level results can be incomplete because of Google's anonymization, privacy thresholds or API limits.
- Tool output can be paginated, filtered or capped; a small sample is not a complete census.
- Some comparisons require matching windows, search types and filters to be meaningful.
- Only authorized properties are available. No third-party site data can be read without Google permission.

For concrete workflows, see [SEO use cases](use-cases.md) and [prompts](prompts.md).
