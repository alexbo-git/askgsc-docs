# AskGSC: read-only Google Search Console access and data limitations

[← Documentation home](../README.md)

## Data access

AskGSC uses Google OAuth with the Search Console **read-only** scope `https://www.googleapis.com/auth/webmasters.readonly`. It can query the Google Search Console properties your connected Google account is already authorized to see. Its MCP tools do **not** submit URLs for indexing, change search settings, edit a site or update sitemaps.

Your connected AI client makes tool calls to the hosted AskGSC MCP endpoint; the assistant may use the returned information to answer your questions. Review the AI client's own privacy and data handling policies when deciding what to ask or share. See the [AskGSC privacy policy](https://askgsc.app/privacy-policy) for the service's current processing disclosures.

## What the metrics mean

| Metric | Meaning | Not equivalent to |
| --- | --- | --- |
| Clicks | Search Console-reported search clicks | Analytics sessions or revenue |
| Impressions | Appearances recorded by Search Console | External keyword search volume |
| CTR | Clicks divided by impressions in the requested scope | Conversion rate |
| Average position | Search Console's aggregated position measure | A live or fixed SERP ranking |

## Data and inference limits

- Search Console's newest data can be delayed or incomplete.
- Google may omit anonymized queries, and some grouped/API results may represent only the accessible sample.
- An absent page or query row does not establish zero traffic.
- URL Inspection reports the **last-known indexing state**; it does not run live tests or request indexing.
- Overlapping queries across pages are clues to investigate, not proof of damaging cannibalization.
- Drops in clicks alone do not prove a cause. Consider seasonality, SERP changes, indexing, content and date-window comparability.
- AskGSC does not provide analytics conversions, sales, full-site crawling, backlink indexes or real-time rank monitoring.

## Documentation only

This public repository contains user documentation and examples, **not** the application source code, private architecture or credentials. Do not open issues containing sensitive data. AskGSC is not affiliated with Google, OpenAI or Anthropic.
