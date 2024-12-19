[![official JetBrains project](http://jb.gg/badges/incubator-flat-square.svg)](https://github.com/JetBrains#jetbrains-on-github)
# JetBrains MCP Proxy Server

The server proxies requests from client to JetBrains IDE.

<a href="https://glama.ai/mcp/servers/k7xzbtlxvb"><img width="380" height="200" src="https://glama.ai/mcp/servers/k7xzbtlxvb/badge" alt="mcp-jetbrains MCP server" /></a>

## Install MCP Server plugin

https://plugins.jetbrains.com/plugin/26071-mcp-server

## Usage with Claude Desktop

To use this with Claude Desktop, add the following to your `claude_desktop_config.json`.
The full path on MacOS: `~/Library/Application\ Support/Claude/claude_desktop_config.json`, on Windows: `%APPDATA%/Claude/claude_desktop_config.json`.

```json
{
  "mcpServers": {
    "jetbrains": {
      "command": "npx",
      "args": ["-y", "@jetbrains/mcp-proxy"]
    }
  }
}
```

If you're running multiple IDEs with MCP server and want to connect to the specific one, add to the MCP server configuration:
```json
"env": {
  "IDE_PORT": "<port of built-in webserver>"
}
```

## How to build
1. Tested on macOS
2. `brew install node pnpm`
3. Run `pnpm build` to build the project

