# Use AskGSC in Cursor

AskGSC provides read-only Google Search Console data to Cursor via a hosted MCP server. It requires an AskGSC account and access to a Google Search Console property; you do not need to install or run a local service.

## Install

1. Install the AskGSC plugin from the Cursor Marketplace once it has been approved, or configure the MCP manually with the server URL `https://mcp.askgsc.app/mcp`.
2. Authenticate using the OAuth flow presented by Cursor (if supported by your installed Cursor version) and authorize the appropriate AskGSC account.
3. Connect your Google Search Console property in [AskGSC](https://askgsc.app/connect).
4. In Cursor Agent, ask: *List my Search Console properties.*

If Cursor does not offer the expected OAuth flow, consult [troubleshooting](troubleshooting.md). OAuth compatibility with Cursor should be confirmed in a local installation before publishing.

## Try these prompts

- For my property, compare the last 28 complete days with the previous 28 days. Identify pages losing clicks, with the underlying numbers.
- Find search queries with impressions but few clicks, and recommend which existing pages to improve first.
- Before proposing SEO changes to this application, check GSC performance and identify high-performing pages that should be preserved.

AskGSC cannot make changes to Google Search Console or the codebase. Google Search Console reports may lag and do not represent live rankings.

[Product and pricing](https://askgsc.app/pricing) · [Data and permissions](privacy-and-limitations.md)
