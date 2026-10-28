# Toca MCP server (remote)

Toca (https://toca.bio) is a WhatsApp-first link-in-bio for small businesses: hotels, clinics, shops, restaurants. This MCP server lets an AI assistant build and manage your Toca page.

**This repo holds metadata only (README + `server.json`). There is no source code here; the server is hosted by Toca.**

- Endpoint (Streamable HTTP): `https://toca.bio/mcp`
- Auth: OAuth 2.1 with PKCE (discovery at `https://toca.bio/.well-known/oauth-protected-resource/mcp`), or a Toca panel API key as Bearer token
- Docs / setup (ES + EN): https://toca.bio/conectar-ia
- Account: free Toca account required (Plan Gratis works; some features are Pro)
- Registry name: `bio.toca/toca`

## Connect
Add a custom/remote MCP connector in your client with URL `https://toca.bio/mcp` and sign in with Toca when asked.

```json
{ "mcpServers": { "toca": { "url": "https://toca.bio/mcp" } } }
```

## Tools (17)
Read: get_page, inspect_website, import_from_url, check_username, get_stats, list_leads
Write: update_profile, add_block, update_block, reorder_blocks, toggle_block, set_image_from_url, publish, create_short_link
Sensitive write: remove_block, apply_template, set_username
(Studio admin accounts also see create_client, set_plan, set_verified, find_clients.)

## Example prompts
- "Show me my Toca page and its links."
- "Add a WhatsApp button to my Toca page with the number +591…"
- "Update my Toca bio to: …"
- "How many visits did my Toca page get this week?"
- "Move my Linktree https://linktr.ee/… to Toca."

## Links
Privacy: https://toca.bio/en/privacy · Terms: https://toca.bio/en/terms · Support: hello@toca.bio
Operated by Supracell OÜ.
