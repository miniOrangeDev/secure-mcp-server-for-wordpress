# Connect Claude to WordPress

Once you're connected, you can ask Claude to write posts, update products, fix SEO and more on your WordPress site, all from a chat.

⏱️ About 2 minutes · No code needed

## Before you start

- The **Secure MCP Server** plugin is installed and you've **created an agent**. If not, see [Getting started](getting-started.md).
- You have a **Claude account**. On Team and Enterprise plans, your workspace admin may need to allow connectors first.

## Steps

### 1. Open the connector page

Open **[miniOrange MCP for WordPress](https://claude.ai/directory/miniorange-mcp-for-wordpress)** in the Claude directory and click **Connect**.

> You can also start from the plugin. Go to **Secure MCP Server → Connect to AI**, choose **Claude**, and the setup panel links you to the same page.

### 2. Enter your site's address

You'll land on the miniOrange sign-in page. Type or paste your site's address, for example:

```text
https://www.your-site.com
```

> 💡 The plugin shows your exact site address in the Claude setup panel, with a copy button.

### 3. Sign in and approve

Your own WordPress login page opens. Log in with your usual WordPress account and click **Allow access**.

**That's it.** You'll be sent back to Claude, and the tools you allowed now show up there.

## Try it

Start a new chat and ask:

> *"What can you do on my WordPress site?"*

> *"Change the heading in my homepage hero to 'Spring Collection'."*

> *"Write meta descriptions for every post that doesn't have one."*

## Video walkthrough

[![Connect Claude to WordPress using Secure MCP Server](https://img.youtube.com/vi/MUtolq0HRhM/hqdefault.jpg)](https://www.youtube.com/watch?v=MUtolq0HRhM)

## Using Claude Desktop or Claude Code?

- **Claude Desktop** uses the same connectors as claude.ai. Once you've connected on the web, it works in the desktop app too.
- **Claude Code** (the terminal tool for developers) is set up with a command. See [Connect another AI app](connect-other-ai-apps.md#claude-code).

## Something not working?

| What you see | What to do |
|---|---|
| Claude can't reach your site | Make sure your site address starts with `https://` and opens in a private browser window. Then run the test in **Secure MCP Server → Troubleshooting**. |
| Connected, but Claude sees no tools | Check that your agent is turned on and that your WordPress role has tools ticked in **AI Agents**. |
| It worked before but stopped | Remove the connector in Claude's settings and connect again. |

More help: [Troubleshooting](troubleshooting.md) · [Full Claude guide on miniOrange's website](https://plugins.miniorange.com/connect-wordpress-with-claude-mcp-guide)
