# SEO use cases with AskGSC and Google Search Console MCP

[← Documentation home](../README.md)

These workflows use **your own authorized Google Search Console data**. They are best used with a specific property and complete, comparable date windows.

## 1. Find pages losing organic traffic

Ask for a 28-day-versus-28-day comparison by page. Identify the largest absolute click losses (not just the biggest percentage changes on tiny pages), then check whether impressions, CTR or average position moved.

**Tools:** `gsc_compare_periods`, `gsc_content_decay`, `gsc_page_diagnosis`.

**Decision:** which existing page deserves manual review, and what information is still missing?

## 2. Find CTR opportunities

Look at query–page pairs with meaningful impressions and comparatively low CTR. Ask your assistant to separate possible title/snippet improvements from differences in ranking and search intent.

**Tools:** `gsc_opportunities`, `gsc_query_search_analytics`.

**Decision:** which page merits a SERP review before changing its title or content?

## 3. Compare mobile and desktop SEO performance

Use the same complete period and compare clicks, impressions and CTR by device. Add a country filter when the site's market is geographically specific.

**Tools:** `gsc_query_search_analytics`, `gsc_compare_periods`, `gsc_overview`.

**Decision:** which device-country segment warrants attention?

## 4. Diagnose one page after a change

Compare the page before and after a deployment, then inspect Google's last-known indexing information. Treat the temporal relationship as a **clue**, not proof that the release caused the change.

**Tools:** `gsc_page_diagnosis`, `gsc_inspect_url`.

**Decision:** whether to inspect the live website, title/canonical changes, internal links, or content fit.

## 5. Investigate potential keyword cannibalization

Find queries present for multiple URLs. Check whether these pages serve different intents and whether one URL is clearly preferred. A shared query alone does not prove an issue.

**Tools:** `gsc_cannibalization`, `gsc_query_search_analytics`.

**Decision:** whether pages need consolidation, clearer differentiation, or no action.

## 6. Review submitted sitemaps and indexing signals

Ask for sitemap errors/warnings, then investigate particular URLs through inspection. This is based on Google's available records; it does not crawl your website or test live indexing.

**Tools:** `gsc_sitemaps`, `gsc_inspect_urls`.

**Decision:** what to verify in Search Console and on the live site.

## Measure after making a change

Capture the original dates, page, queries, relevant country/device scope and metric values. Compare an equivalent later period, while accounting for Google reporting delays and seasonality. Avoid attributing changes automatically to one edit.

[Copy ready-to-adapt prompts](prompts.md)
