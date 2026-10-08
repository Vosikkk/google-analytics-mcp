# Vosik Signals — Google Analytics 4 MCP

Connect your Google Analytics 4 data to an AI assistant through a hosted, read-only MCP server.

**MCP endpoint:** `https://ga4.vosiksignals.win/mcp`

> This repository documents the hosted service. The server's source code is not published here, and no self-hosted package is provided.

## Features

- Discover Google Analytics accounts and GA4 properties accessible to your Google account.
- Query GA4 reports for selected date ranges.
- Analyze traffic, users, acquisition, and other available metrics and dimensions.
- Continue exploring results conversationally in an MCP-compatible AI client.

The server requests the Google OAuth scope `https://www.googleapis.com/auth/analytics.readonly`. Google has verified the OAuth application for this scope. Access is limited to the Google Analytics properties your Google account is permitted to view.

## Connect

1. In an AI client supporting remote MCP over Streamable HTTP and OAuth, add a custom MCP server.
2. Use this URL:

   ```text
   https://ga4.vosiksignals.win/mcp
   ```

3. Follow the Google authorization flow.
4. Ask the assistant to list your Google Analytics accounts and properties.

ChatGPT is the primary integration tested by the maintainer. Compatibility with other clients (including Claude and Cursor) depends on their remote MCP and OAuth support and has not yet been verified end-to-end.

## Example prompts

- List my Google Analytics accounts and properties.
- Show sessions and active users for the last seven days, broken down by date.
- Compare traffic for the last 28 days against the previous 28 days.
- Show acquisition sources for a GA4 property.

Supported queries depend on the available MCP tools, the Google Analytics API, and your property permissions.

## Security and privacy

- Google OAuth authorization is required.
- Google Analytics access is **read-only**.
- OAuth credential properties are encrypted at rest using AES-GCM by the OAuth provider; network connections use HTTPS/TLS.
- Credentials are used for authenticated API requests, not included in normal report responses.

See the [Privacy Policy](https://vosiksignals.win/privacy) for details on data handling, retention, and deletion.

**Never include OAuth tokens, private analytics reports, or personal information in public GitHub issues.**

## Feedback

Use GitHub Issues to report bugs, request features, or share client compatibility results. Include the client name, error message, and reproduction steps, but redact sensitive information.

## Service

- Website: https://vosiksignals.win
- MCP: https://ga4.vosiksignals.win/mcp
- Privacy Policy: https://vosiksignals.win/privacy

This is documentation for a hosted service, **not an open-source release of the server code**.
