# How to connect Google Search Console to ChatGPT with AskGSC MCP

[← Documentation home](../README.md)

AskGSC lets ChatGPT access read-only Search Console data via a remote MCP connector. It does not require uploading spreadsheets or installing a local MCP server.

## Connection steps

1. [Create or open your AskGSC account](https://askgsc.app/connect) using a Google account with access to Search Console.
2. Authorize Google's read-only Search Console permission.
3. In ChatGPT, open the available **app/plugin/connector settings** for your plan or workspace and choose the option to add a **custom MCP server**. Custom MCP connection controls and labels may vary.
4. Enter **AskGSC** and `https://mcp.askgsc.app/mcp`.
5. Choose the supported OAuth authorization flow, sign in to AskGSC when requested, and approve the connection.
6. In a conversation with the connector enabled, ask ChatGPT to **use AskGSC** and list your GSC properties.

**Note:** custom remote MCP connectors may be unavailable on some ChatGPT plans or managed workspaces. This is a client-side availability limit, not an AskGSC configuration option.

## Three useful first prompts

```text
Use AskGSC to list all my authorized Search Console properties.
```

```text
Use AskGSC to compare the latest complete 28 days of organic search
performance for [PROPERTY] with the preceding 28 days. Show clicks,
impressions, CTR and average position, then identify the largest page changes.
```

```text
Use AskGSC to investigate [PAGE URL]. Compare its recent clicks and queries,
then inspect Google's last-known indexing status. Separate facts from hypotheses.
```

## What happens in the background?

ChatGPT requests data through one or more of AskGSC's **11 MCP tools**. AskGSC reads the Google Search Console data you authorized; ChatGPT then interprets those responses. ChatGPT can draw SEO conclusions or propose edits, but AskGSC's tools **cannot change Search Console or your website**.

For more, see [all 11 tools](mcp-tools.md), [troubleshooting](troubleshooting.md), and the [AskGSC ChatGPT guide](https://askgsc.app/connect-google-search-console-chatgpt).

AskGSC is independent and is not an official OpenAI or Google product.
