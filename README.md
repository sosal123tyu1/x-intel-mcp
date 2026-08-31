# x-intel-mcp

Zero-fee X/Twitter social intelligence MCP server for AI agents (Claude, Cursor, Pi).

## Install

```bash
npx x-intel-mcp
# or
bunx x-intel-mcp
```

## Configure (Claude Desktop)

```json
{
  "mcpServers": {
    "x-intel": {
      "command": "npx",
      "args": ["-y", "x-intel-mcp"]
    }
  }
}
```

## Tools

- `x_search` — search recent public posts by query
- `x_profile` — recent posts from a public handle

## License

MIT
