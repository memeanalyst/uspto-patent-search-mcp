# USPTO Patent Search — New Patent Alerts — MCP Server

Search USPTO's official US patent index from your AI agent or MCP client — by keyword, assignee, inventor or CPC class — and get each patent as a clean structured record: publication number, title, assignee, inventor, filing/publication/priority dates, application number, CPC codes and the official USPTO PDF. Monitoring mode on a schedule turns the same search into a quiet feed of only-new US patents.

This repo is the MCP listing for the [USPTO Patent Search — New Patent Alerts](https://apify.com/magnova/uspto-patent-search) Actor by Magnova on Apify. The server is hosted by Apify at the pinned endpoint below — there is nothing to install or run from this repository; you just point your MCP client at the URL.

## Tools

The pinned connection loads a focused tool set:

- **magnova--uspto-patent-search** — Search USPTO's official US patent index by keyword, assignee, inventor or CPC class, or monitor a search for only-new patents. Returns structured records: publication number, title, assignee, inventor, dates, application number, CPC codes and the official USPTO PDF link.
- **fetch-actor-details** — Fetch the Actor's full input schema, pricing, and documentation, so an agent can check parameters and cost before running it.
- **get-actor-run / get-dataset-items** — Run and storage helpers, loaded automatically, used to fetch the results a run produced.

## Connect

Pinned endpoint (Streamable HTTP):

```
https://mcp.apify.com?tools=fetch-actor-details,magnova/uspto-patent-search
```

On first connect, your client will ask you to sign in with your Apify account (OAuth). If your client cannot do OAuth, pass your Apify API token as an `Authorization: Bearer <YOUR_APIFY_TOKEN>` header instead.

### Cursor / VS Code / other Streamable HTTP clients

```json
{
  "mcpServers": {
    "uspto-patent-search": {
      "url": "https://mcp.apify.com?tools=fetch-actor-details,magnova/uspto-patent-search"
    }
  }
}
```

### Claude Desktop

Claude Desktop's config file only runs local commands, so use the `mcp-remote` bridge:

```json
{
  "mcpServers": {
    "uspto-patent-search": {
      "command": "npx",
      "args": [
        "-y",
        "mcp-remote",
        "https://mcp.apify.com?tools=fetch-actor-details,magnova/uspto-patent-search"
      ]
    }
  }
}
```

The same pinned URL also lives in this repo's `.mcp.json`, and `server.json` is the listing for the Official MCP Registry, published as `io.github.memeanalyst/uspto-patent-search-mcp`.

## Pricing

Pay per event, billed to your own Apify account: **$0.004 per patent — $4 per 1,000 patents**. No start fee, no subscription, and you are only charged for records actually delivered.

## Links

- Actor on Apify Store: https://apify.com/magnova/uspto-patent-search
- MCP endpoint: https://mcp.apify.com?tools=fetch-actor-details,magnova/uspto-patent-search

*Patent records come from USPTO's official public patent index.*
