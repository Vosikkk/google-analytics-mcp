# Connecting to Vosik Signals GA4 MCP

## Remote endpoint

```text
https://ga4.vosiksignals.win/mcp
```

This is a **hosted Streamable HTTP MCP server**, not a local stdio executable.

## ChatGPT

Add a custom MCP connection in ChatGPT's supported connection workflow, supply the endpoint above, and complete the Google OAuth authorization when prompted. The exact settings labels may differ by plan and product version.

## Other MCP clients

For Claude, Cursor, and other clients, use their **remote MCP / Streamable HTTP** setup flow and the same endpoint. The client must support the server's OAuth authorization flow. These integrations are not yet verified end-to-end; please open an issue if you test one successfully or encounter a reproducible failure.

## First check

Ask:

> List the Google Analytics accounts and properties I can access.

If no properties appear, confirm the Google account you authorized has access to the intended GA4 property.

## Troubleshooting

- **OAuth prompt doesn't appear:** Check whether your client supports OAuth for remote MCP servers.
- **Access denied:** Confirm you authorized the correct Google account and granted the requested read-only scope.
- **No properties:** Confirm your Google account has GA4 property access.
- **Unsupported request:** Try a simpler query or ask the client to list available MCP tools.

Never post authorization codes, access tokens, refresh tokens, or private analytics data in public issues.
