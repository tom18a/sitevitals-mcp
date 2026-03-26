# SiteVitals MCP Server

<!-- mcp-name: io.github.tom18a/sitevitals -->

An MCP (Model Context Protocol) server for the [SiteVitals](https://www.sitevitals.co.uk) website monitoring platform. Connect your AI assistant to your SiteVitals account to query live uptime, SEO, security, performance, and SSL data in plain English.

## What you can ask

- "How are all my sites performing right now?"
- "Which of my sites has the worst SEO score?"
- "Did any of my sites go down in the last 7 days?"
- "Is my SSL certificate about to expire on any domains?"
- "What security issues does my site have?"

## Tools

| Tool | Description |
|------|-------------|
| `list_sites` | List all monitored sites with current health scores |
| `get_site_health` | Detailed scores and trends for a specific site |
| `get_site_uptime` | Uptime history and downtime incidents (up to 90 days) |
| `get_latest_checks` | Latest SEO, security and page speed check results |
| `get_ssl_domain_status` | SSL certificate and domain expiry status |

Full tool definitions are in the [`tools/`](./tools/) directory.

## Connection

This is a **hosted remote MCP server** — there is nothing to install or run locally. Connect via OAuth from any MCP-compatible AI client.

**MCP Server URL:**
```
https://www.sitevitals.co.uk/api/mcp
```

**Authentication:** OAuth 2.1 with PKCE. You will be prompted to log in to your SiteVitals account when connecting.

## Documentation

- [Connection Guide](https://www.sitevitals.co.uk/docs/mcp/connect)
- [Tool Reference](https://www.sitevitals.co.uk/docs/mcp/tools)
- [MCP Overview](https://www.sitevitals.co.uk/docs/mcp)

## Security & Privacy

- Authentication uses OAuth 2.1 with PKCE — no passwords or API keys are shared with your AI assistant
- Access is scoped to your own sites only
- All tools are **read-only** — the MCP server cannot make changes to your sites or account
- All requests are logged in your SiteVitals account for transparency
- You can revoke access at any time from your SiteVitals account settings

## Requirements

A [SiteVitals account](https://www.sitevitals.co.uk/signup) is required to use this MCP server.

## License

MIT
