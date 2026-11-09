# ROASaurus plugin

Connects your coding agent to the ROASaurus MCP server and adds three skills and three commands for webshop ad analysis.

- MCP server: `https://app.roasaurus.com/mcp` (streamable HTTP, OAuth 2.1 with dynamic client registration). This is
  the only network endpoint the plugin uses.
- Skills: `ads-audit`, `wasted-spend`, `tracking-health`.
- Commands: `/roasaurus:audit`, `/roasaurus:wasted-spend`, `/roasaurus:tracking-health`.

## Requirements

A ROASaurus account with a connected store, as an owner or admin of its workspace. No API keys or other credentials go
into the plugin: on first use you sign in through the browser and pick the store on the consent page. Read-only tools
are always on; write access (proposals to the Actions inbox, applying approved changes) only when you tick it there.

## Links

Docs: https://roasaurus.com/integrations/mcp/claude-code · Privacy: https://roasaurus.com/privacy ·
Support: hello@roasaurus.com
