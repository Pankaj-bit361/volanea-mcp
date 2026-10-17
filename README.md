# Volanea MCP server

<!-- mcp-name: io.github.Pankaj-bit361/volanea -->

Connect your AI coding agent to [Volanea](https://www.volanea.com) — transactional email, campaigns, and automation on one API. Your agent can set up email in your app for you: create templates, segments, workflows, and webhooks, then prove it works with a test send.

This is a **remote** MCP server — there is nothing to install or run.

```
https://api.volanea.com/mcp
```

Transport: Streamable HTTP. Auth: OAuth 2.1 (your client opens a browser and you sign in to Volanea), or an API key sent as `Authorization: Bearer sk_...`.

## Connect

**Claude Code**

```bash
claude mcp add volanea --transport http https://api.volanea.com/mcp
```

To use an API key instead of signing in:

```bash
claude mcp add volanea --transport http https://api.volanea.com/mcp \
  -H "Authorization: Bearer sk_test_..."
```

**Cursor, Windsurf, VS Code, and other MCP clients** — add a server with the URL above. Clients that support OAuth sign you in automatically; otherwise set the `Authorization` header to your API key.

Use a **test key** (`sk_test_...`) while building: messages render and log exactly like live ones, and nothing is delivered.

## What your agent can do

- Check project status, domains, and API key mode
- Create and render templates, segments, workflows, and webhook endpoints
- Send test email and read back what was rendered and delivered
- Track events and test workflows end to end
- Create campaign drafts (a human sends them)
- Create agent inboxes and read, search, or wait for incoming email

## Links

- Website: https://www.volanea.com
- Docs: https://www.volanea.com/docs
- Pricing: https://www.volanea.com/pricing — 1,000 emails free every month, no card needed
