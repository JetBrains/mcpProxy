[![official JetBrains project](http://jb.gg/badges/incubator-flat-square.svg)](https://github.com/JetBrains#jetbrains-on-github)
# JetBrains MCP Proxy Server


The server proxies requests from client to JetBrains IDE.

## How to build
1. Tested on macOS
2. `brew install node pnpm`
3. Run `pnpm build` to build the project

## Usage with Claude Desktop

To use this with Claude Desktop, add the following to your `claude_desktop_config.json`:

```json
{
  "mcpServers": {
    "github": {
      "command": "npx",
      "args": [
        "<project_location>/dist/src/index.js"
      ],
      "env": {
        "IDE_PORT": "<port of built-in webserver, can be omitted than default 63343>"
      }
    }
  }
}
```