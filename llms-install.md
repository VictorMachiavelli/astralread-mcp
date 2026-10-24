# Installing the AstralRead MCP server (for AI agents)

AstralRead is a hosted remote MCP server — there is nothing to clone, build or run, and no API key.

1. Add a remote MCP server named `astralread` with the URL `https://astralread.com/mcp`
   (transport: streamable HTTP; no authentication, no headers).
   For a JSON config: `{"mcpServers": {"astralread": {"url": "https://astralread.com/mcp"}}}`
2. Verify by calling `sky_today` with no arguments — it returns today's Moon sign and phase.
3. For a birth chart call `natal_chart` with `birth_date` (YYYY-MM-DD), `birth_time` (HH:MM, local) and `place` (a city name), or `latitude` / `longitude` / `timezone`; `lang` is `ru` or `en`.
   Ask the user for these; if the time is unknown, say the houses and the Ascendant are uncertain.
