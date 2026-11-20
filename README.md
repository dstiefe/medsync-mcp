# MedSync Devices (plugin)

Slash commands for the MedSync device-graph MCP, so people can type them in their own Claude.

| Command | What it does |
|---|---|
| `/compare <device> and <device>` | Side by side: sizes, what each IFU says it is used with, labels. Shown as a card with three tabs. No verdict. |
| `/works-with <devices>` | Whether devices fit or work together, or what works with one. |
| `/label <question>` | What a label (IFU) says: an indication, a time window, a patient case. |
| `/sizes <devices>` | Inner and outer diameter and the insertable length. |

## How it connects

`.mcp.json` points at the MedSync devices MCP, `https://mcp.medsync-ai.com/mcp` (the test deployment, 2026-11-20). Override it with the environment variable `MEDSYNC_DEVICES_URL`. The first use asks the person to sign in to MedSync.

The commands only tell Claude which of the server's tools and guide pages to use. The data, the comparison card and the rules live on the server (repository `medsync_agentic_vs4`, branch `mcp-test`, `api/v6/kg_agents/mcp_graph.py` and `mcp_wiki/`).

## Layout

```
.claude-plugin/plugin.json        name, version, author
.claude-plugin/marketplace.json   lets the plugin be added from a repository
.mcp.json                         the connection
skills/<command>/SKILL.md         one folder per slash command
```

## Not done yet

- Not tested inside claude.ai (does the command appear, and does `/compare Raptor 71 and Zoom 71` run the card).
- Not published: no repository yet.
- To be combined with `medsync-ai-screening` later, if Daniel decides (2026-11-20).
