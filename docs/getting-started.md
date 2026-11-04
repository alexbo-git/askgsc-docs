# Getting started with the AskGSC Google Search Console MCP server

[← Documentation home](../README.md)

AskGSC provides a **hosted remote MCP server** that helps an AI assistant analyze data from Google Search Console. No Google Cloud project, local installation, or API key is required for regular users.

## Prerequisites

- A Google account with access to at least one Google Search Console property.
- An AskGSC account, created via Google authorization.
- An AI client supporting **custom remote MCP servers with OAuth**. Support differs by plan and workspace.

## Step 1 — Authorize your Search Console property

Open **https://askgsc.app/connect** and continue with the relevant Google account. Grant the read-only Search Console permission. AskGSC can access only the GSC properties that this Google account is already authorized to view. Your trial starts once an eligible property is connected.

## Step 2 — Add the remote MCP connector

Open your AI client's integration, app, or custom connector settings. Choose the option to add a **remote MCP server**, if available, and use:

```text
Name: AskGSC
URL:  https://mcp.askgsc.app/mcp
Authentication: OAuth (authorize when prompted)
```

Confirm the authorization in your browser. **Do not paste Google access tokens, refresh tokens, or personal API credentials into a chat or repository.** The MCP endpoint handles its own authentication flow.

For client-specific guidance, see [ChatGPT](chatgpt.md) or [Claude](claude.md).

## Step 3 — Make a test request

Start with property discovery:

```text
Use AskGSC to list the Google Search Console properties I can access.
```

Then test an overview:

```text
For [PROPERTY], summarize clicks, impressions, CTR and average position
for the latest complete 28 days and compare with the preceding 28 days.
Include the dates and any data-quality caveats.
```

Use the exact property name or `siteUrl` that AskGSC returns. GSC supports both URL-prefix properties (for example, `https://example.com/`) and domain properties (for example, `sc-domain:example.com`); these are not interchangeable.

## Next steps

- [MCP tools](mcp-tools.md): know which data your assistant can request.
- [SEO workflows](use-cases.md): investigate losses and identify opportunities.
- [Prompt library](prompts.md): ask focused, repeatable questions.
- [Troubleshooting](troubleshooting.md): fix connection and data problems.

**Need the latest offer?** Visit [AskGSC pricing](https://askgsc.app/pricing). The trial does not automatically charge you.
