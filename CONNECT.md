# Connecting to SOS Flights

Server URL: `https://www.sosflights.help/mcp` (Streamable HTTP, no authentication).

## Claude (claude.ai / Claude Desktop)

Settings → Connectors → Add custom connector → paste `https://www.sosflights.help/mcp`.

## Claude Code

```bash
claude mcp add --transport http sosflights https://www.sosflights.help/mcp
```

## ChatGPT

Settings → Apps & Connectors → Advanced → Developer mode → Create → MCP server URL `https://www.sosflights.help/mcp`, authentication: none.

## Cursor / VS Code / other clients

```json
{
  "mcpServers": {
    "sosflights": {
      "url": "https://www.sosflights.help/mcp"
    }
  }
}
```

## Quick test

```bash
curl -s https://www.sosflights.help/mcp \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json, text/event-stream' \
  -d '{"jsonrpc":"2.0","id":1,"method":"initialize","params":{"protocolVersion":"2025-06-18","capabilities":{},"clientInfo":{"name":"test","version":"0"}}}'
```

More: https://www.sosflights.help/en/connect
