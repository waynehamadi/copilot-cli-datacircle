# Datacircle for GitHub Copilot CLI

Find the best GTM APIs. We benchmark all the GTM APIs and we put the results on our website: https://datacircle.dev

This plugin adds Datacircle's MCP server, https://api.datacircle.dev/mcp, and a skill that tells Copilot when to use it. You need no key and no account.

| Tool | What it gives |
| --- | --- |
| `list_apis` | Every GTM API on the sheet, with how many plans and providers it has, and links to its sheet and its best page |
| `search_plans` | The plans of one API or of every API, best first by score, or sorted by provider or price. Each plan comes with its price per 1,000, rate limits, speed, the fields it returns and its page on datacircle.dev |

## Install

```bash
copilot plugin install waynehamadi/copilot-cli-datacircle
```

Then ask Copilot, for example: "Which email finder API is best for under $5 per 1,000?"

`/mcp` lists the server and its two tools, and `/skills` lists the `datacircle` skill.

The plugin follows the Agent Plugins 1.0 format (`plugin.json`, `mcp.json` and `skills/`), so other apps that read that format can install it too.

## Network

Each tool call is one HTTPS request to https://api.datacircle.dev/mcp and nothing else. The request holds only the tool's own arguments: no key, nothing from your files. The plugin runs no code on your computer.

## Links

- Datacircle: https://datacircle.dev
- The MCP server's docs: https://datacircle.dev/docs/mcp
- What each key means: https://datacircle.dev/fields

MIT license.
