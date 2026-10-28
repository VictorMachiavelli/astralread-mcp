# AstralRead MCP server

[![M8ven Score](https://m8ven.ai/badge/mcp/victormachiavelli-astralread-mcp-1ptasp?v=f66290e65e41cf96c750345aea0a1afe)](https://m8ven.ai/mcp/victormachiavelli-astralread-mcp-1ptasp?s=readme)

<img src="logo.png" width="96" align="right" alt="AstralRead">

**Astrology calculations for AI assistants** — a public, read-only remote [Model Context Protocol](https://modelcontextprotocol.io) server by [AstralRead](https://astralread.com).
No account, no API key; birth data is used only for the calculation and is never stored. Russian and English.

```
https://astralread.com/mcp        (streamable HTTP)
```

| Tool | What it returns |
|---|---|
| `natal_chart` | a birth chart: planets, houses, angles, major aspects with orbs |
| `transits_today` | the tight transits of a day to a birth chart |
| `sky_today` | the sky of a day: Moon sign and phase, exact aspects, ingresses, stations |
| `vedic_chart` | the sidereal (Jyotish) chart with nakshatras |
| `vimshottari_dasha` | the Vimshottari dasha periods |
| `kb_lookup` | links to AstralRead's knowledge-base pages for a placement |

Positions come from an astronomical ephemeris; the knowledge base behind `kb_lookup` is grounded in classic astrology
and psychology books. For self-reflection, not fortune-telling.

## Connect

**ChatGPT** — the AstralRead app is in the ChatGPT apps directory: <https://astralread.com/en/app>.

**Claude** (claude.ai, Desktop) — Settings → Connectors → Add custom connector → URL `https://astralread.com/mcp`.

**Claude Code**
```bash
claude mcp add --transport http astralread https://astralread.com/mcp
```

**Cursor / Windsurf / VS Code / Cline** — add to your MCP config:
```json
{
  "mcpServers": {
    "astralread": { "url": "https://astralread.com/mcp" }
  }
}
```

**Gemini, Mistral Le Chat, Grok, Perplexity** — where custom connectors are available on your plan, add a connector
with the URL `https://astralread.com/mcp` (no authentication).

## Try asking

- "Build my natal chart: 14 March 1990, 08:30, Lisbon."
- "Which transits affect my chart today?"
- "What's the sky like today — Moon sign, retrogrades, exact aspects?"
- "What is my Vimshottari dasha period right now?"

## More

- Official MCP Registry: `com.astralread/astrology`
- Server card: <https://astralread.com/.well-known/mcp/server-card.json>
- Agent skill: <https://astralread.com/.well-known/agent-skills/astralread/SKILL.md>
- Every astralread.com page is also available as Markdown (`Accept: text/markdown`); site map for agents: <https://astralread.com/llms.txt>
- Contact: support@astralread.com

This repository holds the connection docs; the server itself is hosted by AstralRead.
