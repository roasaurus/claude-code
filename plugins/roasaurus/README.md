# ROASaurus plugin

Connects your coding agent to the ROASaurus MCP server and adds three skills and three commands for webshop ad analysis.

- MCP server: `https://app.roasaurus.com/mcp` (streamable HTTP, OAuth 2.1 with dynamic client registration). This is
  the only network endpoint the plugin uses.
- Skills: `ads-audit`, `wasted-spend`, `tracking-health`.
- Commands: `/roasaurus:audit`, `/roasaurus:wasted-spend`, `/roasaurus:tracking-health`.

## Requirements

A ROASaurus account with a connected store, as an owner or admin of its workspace. No API keys or other credentials go
into the plugin: on first use you sign in through the browser and pick the store on the consent page. Most read-only
tools are always on; `ad_entities`, `meta_delivery_diagnosis` and proposals to the Actions inbox need the `actions:write`
box ticked there; an owner or admin then approves
each one in the inbox. The skills never apply changes themselves, so leave `actions:apply` (changes without the inbox) off.

## What the skills do

- `ads-audit` (`/roasaurus:audit [platform] [7|14|30|90]`, default 30 days): read-only; covers every connected ad account,
  also those ROASaurus may not change; ranks findings by measured profit over the period and labels platform-reported
  conversions apart from ROASaurus attribution.
- `wasted-spend` (`/roasaurus:wasted-spend [7|14|30|90]`, default 14 days): two categories (spend without attributed orders;
  orders but negative profit); the campaigns you confirm become proposals in the Actions inbox, with the status the tool returns.
- `tracking-health` (`/roasaurus:tracking-health [platform]`): read-only; purchase-event acceptance and consent only from
  the delivery and consent data of `admin:read` (a named API key with that scope; the browser sign-in does not ask for it),
  and says so when that is missing.

Any other number of days gets the list of valid options instead of a report.

## Links

Docs: https://roasaurus.com/integrations/mcp/claude-code · Privacy: https://roasaurus.com/privacy ·
Support: hello@roasaurus.com
