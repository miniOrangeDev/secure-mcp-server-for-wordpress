# Connect another AI app

The plugin uses the open **MCP** standard, so it works with any AI app that can connect to a "remote MCP server" or "custom connector". This includes Gemini, Perplexity, Gemini CLI, VS Code, Claude Code and many more.

> **Looking for a specific app?** These have their own step-by-step guides:
> [Claude](connect-claude.md) · [ChatGPT](connect-chatgpt.md) · [Cursor](connect-cursor.md) · [Grok](connect-grok.md) · [Codex](connect-codex.md) · [Windsurf](connect-windsurf.md) · [Antigravity](connect-antigravity.md)

You can connect several apps at once. Each connection has its own permissions and its own entries in the activity log.

## The connection URL

Every app needs this one URL. It's the same for every WordPress site:

```text
https://gateway.miniorange.ai/v2/mcp
```

The app doesn't need your site's address up front. You enter it on the sign-in page when you connect.

## Steps (any app)

1. **Find "Add connector" or "Add MCP server".** Most AI apps keep this under **Settings → Connectors**, **Integrations** or **MCP**. Look for options called *custom connector* or *remote MCP server*.
2. **Paste the connection URL** wherever it asks for the connector or server URL.
3. **Enter your site's address** when the miniOrange sign-in page asks which site to connect.
4. **Log in to WordPress and approve access.** Done.

> 💡 **Can't find "Connectors" or "Add MCP server"?** Your AI plan may need that feature switched on first. Check your app's help pages for "MCP" or "custom connectors".

### Plans that can add a custom connector

| App | Plan needed |
|---|---|
| **Gemini** | Gemini Pro |
| **Perplexity** | Perplexity Pro, Max or Enterprise. The free plan has no custom connectors. |

---

## Setup for developer tools

These tools are set up with a command or a settings file. In every case you add the same URL, and the first time it's used you'll be asked to sign in through your browser.

> App menus and file locations change between versions. If something below doesn't match what you see, search your app's documentation for "remote MCP server".

### Claude Code

Run this in your terminal:

```bash
claude mcp add --transport http wordpress https://gateway.miniorange.ai/v2/mcp
```

Then start Claude Code, type `/mcp`, choose **wordpress**, and sign in.

### Gemini CLI

Add this to `~/.gemini/settings.json`:

```json
{
  "mcpServers": {
    "wordpress": {
      "httpUrl": "https://gateway.miniorange.ai/v2/mcp"
    }
  }
}
```

Restart Gemini CLI, then run `/mcp auth wordpress` to sign in.

### VS Code (GitHub Copilot agent mode)

Add this to `.vscode/mcp.json` in your project, or run **MCP: Add Server** from the Command Palette:

```json
{
  "servers": {
    "wordpress": {
      "type": "http",
      "url": "https://gateway.miniorange.ai/v2/mcp"
    }
  }
}
```

### Windsurf and Antigravity

See the step-by-step guides: [Connect Windsurf](connect-windsurf.md) · [Connect Antigravity](connect-antigravity.md)

### Any other MCP client

| Setting | Value |
|---|---|
| Server URL | `https://gateway.miniorange.ai/v2/mcp` |
| Transport | Streamable HTTP |
| Authentication | OAuth 2.1 with PKCE (the client must support MCP sign-in) |

---

## Something not working?

- **The app says it can't connect:** your site must be live on the internet with `https://`. Run the connection test in **Secure MCP Server → Troubleshooting**.
- **Connected, but no tools:** make sure your agent is turned on and your WordPress role has tools ticked in **AI Agents**.
- More help: [Troubleshooting](troubleshooting.md) · [miniOrange's setup guide for all AI apps](https://plugins.miniorange.com/connect-ai-agents-to-wordpress-using-mcp-guide)
