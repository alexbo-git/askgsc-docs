# How to connect Google Search Console to Claude with AskGSC MCP

[← Documentation home](../README.md)

Use AskGSC's hosted remote MCP endpoint to make your authorized Google Search Console data available in a compatible Claude environment.

## Connection steps

1. [Connect Google Search Console to AskGSC](https://askgsc.app/connect).
2. In the Claude client or workspace you use, find its **custom integration/connector** settings for remote MCP servers, if supported by your plan.
3. Add a connector named **AskGSC** with this URL:

   ```text
   https://mcp.askgsc.app/mcp
   ```

4. Complete the OAuth authorization with AskGSC when Claude prompts you.
5. Start a conversation, enable/use the connection where your client requires it, and ask Claude to list your Search Console properties.

**Compatibility:** Claude's web, desktop, and developer environments do not necessarily offer the same MCP setup flow. Choose **remote MCP with OAuth**, rather than assuming a local executable or JSON configuration. Some clients or workspaces restrict custom integrations.

## Example prompts

```text
Use AskGSC to list my accessible Google Search Console properties.
```

```text
For [PROPERTY], which search queries are gaining impressions but not clicks
in the latest complete 28 days versus the previous 28 days? Return the data,
then explain which hypotheses deserve investigation.
```

```text
For [PROPERTY], inspect indexing signals for [PAGE URL]. Is Google's
last-known canonical different from the user-declared canonical?
```

AskGSC only reads authorized GSC data. Claude's explanations are interpretations, not a substitute for Google Search Console's data quality notes. See [limitations](privacy-and-limitations.md) and the [full tool reference](mcp-tools.md).

AskGSC is independent and is not an official Anthropic or Google product.
