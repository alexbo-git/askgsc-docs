# 15 Google Search Console prompts for ChatGPT and Claude

[← Documentation home](../README.md)

These prompts assume an authenticated AskGSC MCP connection. Replace `[PROPERTY]`, `[PAGE URL]` and `[BUSINESS GOAL]` with your details. Ask for complete reporting dates and have the assistant distinguish unavailable data from zero.

## Traffic and trends

1. **SEO overview:** “Use AskGSC for [PROPERTY]. Summarize clicks, impressions, CTR and average position over the latest complete 28 days, compared with the previous 28 days. State exact dates.”
2. **Traffic losses:** “Which matched pages on [PROPERTY] had the biggest absolute click drops between the last two complete 28-day periods? Show both sets of numbers.”
3. **Rising queries:** “Which queries on [PROPERTY] gained the most impressions in the latest complete 28 days versus the previous period? Did clicks rise too?”
4. **Country breakdown:** “For [PROPERTY], compare clicks and impressions by country between the last two complete months. Rank segments by absolute click change.”
5. **Device breakdown:** “For [PROPERTY], compare mobile and desktop CTR and average position for [PAGE URL] over the same complete period.”

## Pages, content and CTR

6. **Top pages:** “Which 20 pages on [PROPERTY] generated the most Google Search clicks in the latest complete 28 days? Include impressions and CTR.”
7. **Page queries:** “What are the main visible GSC queries for [PAGE URL]? Return clicks, impressions, CTR and average position.”
8. **CTR opportunities:** “Use AskGSC to identify high-impression query–page pairs on [PROPERTY] with CTR worth investigating. Do not forecast traffic gains.”
9. **Refresh priorities:** “Which pages on [PROPERTY] lost clicks while retaining meaningful impressions? Suggest three review candidates aligned to [BUSINESS GOAL], separating evidence from hypotheses.”
10. **Query overlap:** “Which queries on [PROPERTY] appear across multiple URLs? Explain why this might be legitimate rather than SEO cannibalization.”

## Technical signals

11. **One URL:** “Use AskGSC to inspect Google's last-known indexing status for [PAGE URL]. Summarize canonical, crawl and coverage signals where available.”
12. **Batch inspection:** “Inspect the last-known indexing information for these five URLs on [PROPERTY]: [URL1], [URL2], [URL3], [URL4], [URL5]. Flag failed inspections separately.”
13. **Sitemaps:** “List submitted sitemaps for [PROPERTY]. Which have errors or warnings in Google's reported data?”

## Decisions and reporting

14. **Pre/post release:** “Compare [PAGE URL] on [PROPERTY] during [DATE RANGE A] versus [DATE RANGE B], keeping length and filters consistent. What changed, and what could we verify before blaming the release?”
15. **Next SEO action:** “For [PROPERTY], combine the observed page losses, query–page opportunities and [BUSINESS GOAL]. Recommend one page to investigate first, give evidence and propose a later measurement window.”

**Interpretation rules:** Search Console data can be delayed, sampled, anonymized or incomplete. CTR is not conversion rate, and average position is not a live ranking. A recommendation is a hypothesis until tested.

More examples: [AskGSC's online prompt collection](https://askgsc.app/prompts/google-search-console).
