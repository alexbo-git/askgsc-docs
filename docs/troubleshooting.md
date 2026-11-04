# Troubleshooting AskGSC MCP connection and Google Search Console data

[← Documentation home](../README.md)

## The AI client does not offer a custom MCP connector

Custom remote MCP support varies by product, plan, rollout and workspace administrator settings. Check your client's current integration options. AskGSC cannot enable unavailable client features.

## OAuth authorization did not complete

Start the connection again from your AI client's remote MCP settings, check that the server URL is exactly `https://mcp.askgsc.app/mcp`, and sign in to the correct AskGSC account. Do not copy tokens into the conversation or configure a static API key in place of OAuth. If your organization blocks custom connectors, consult its workspace settings.

## AskGSC shows no Search Console properties

Use the Google account that already has access to your property in Google Search Console. Verify that the property is present there and that you have permission to view it. AskGSC cannot grant Search Console permissions or read unrelated domains.

## The assistant says a tool is unavailable

Confirm that you selected/enabled the AskGSC connection for this chat and that OAuth authorization succeeded. Ask the assistant to discover/list the available AskGSC tools or properties before an involved analysis. Free-tier usage credits and client-side connector restrictions can also affect tool access.

## The latest days show missing or unexpectedly low traffic

Google Search Console reporting is not real time. Recent days can be incomplete. Ask for the **latest complete** date window, report its exact dates and avoid treating missing rows as zero. Google also anonymizes some query-level data.

## A URL cannot be inspected

The inspected URL must belong to a Google Search Console property you can access. Verify the exact protocol, domain/subdomain and property. URL Inspection returns **Google's last-known state**, not a live test.

## A page is absent from a report

Search Console query/page rows can be incomplete or capped. Filters, search type, pagination and dimensions can change the returned sample. Absence of a row does **not** prove zero impressions or zero clicks.

## Still blocked?

Use [AskGSC's contact page](https://askgsc.app/contact) to report the relevant AI client, connection step, and **non-sensitive** error message. Never share passwords, access/refresh tokens or raw authorization headers.
