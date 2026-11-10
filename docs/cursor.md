# AskGSC for Cursor

Connect Cursor to your Google Search Console data using AskGSC's hosted, read-only Streamable HTTP MCP server.

## Install from the Cursor Marketplace

Once AskGSC is approved, select **Install** from its Cursor Marketplace listing. Cursor supports OAuth for remote Streamable HTTP MCP servers and should prompt you to authenticate.

1. Complete the AskGSC OAuth authorization prompt from Cursor.
2. Connect the Google account that has Search Console access at https://askgsc.app/connect if not already connected.
3. In Cursor Agent, ask: **List my available Google Search Console properties.**

## Manual MCP configuration

If the Marketplace installation is unavailable, add the following to Cursor's user or project `mcp.json`:

```json
{
  "mcpServers": {
    "askgsc": {
      "type": "http",
      "url": "https://mcp.askgsc.app/mcp"
    }
  }
}
```

The endpoint uses OAuth authorization with dynamic client registration. **Do not put Google OAuth credentials, API keys, access tokens, or static OAuth client credentials in your configuration.** Cursor is responsible for initiating the MCP OAuth flow. If authorization does not launch, check Cursor's MCP connection settings and the provider authorization status.

## Useful prompts

- For my property, compare the latest 28 complete days with the previous 28 and identify the largest traffic losses.
- Find pages with high impressions but low click-through rates. Show the supporting GSC data.
- Before suggesting SEO modifications, identify existing pages that generate organic traffic and should be preserved.

AskGSC is read-only and cannot change your site or Google Search Console. Data is not real time. The Cursor plugin is free to install; AskGSC's separate service has Free and optional Pro plans.

[Pricing](https://askgsc.app/pricing) · [Privacy and limitations](privacy-and-limitations.md)
