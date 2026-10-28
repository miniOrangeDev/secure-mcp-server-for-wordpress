# Connect Codex to WordPress

Codex is OpenAI's coding agent. Once it's connected to your site, Codex can work on your WordPress content, theme and settings while you build, all within the limits you set.

⏱️ About 2 minutes · No code needed

## Before you start

- The **Secure MCP Server** plugin is installed and you've **created an agent**. If not, see [Getting started](getting-started.md).
- You have **Codex** installed and are signed in with your OpenAI account.

## Steps

### 1. Find the plugin in Codex

In Codex, click the **Plugins** icon in the left sidebar and search for **MCP Server for WordPress**.

### 2. Install it

Click the **+** button to install the plugin.

### 3. Enter your site's address

You'll land on the miniOrange sign-in page. Type or paste your site's address, for example `https://www.your-site.com`, and click **Continue**.

> 💡 You can copy your exact site address from **Secure MCP Server → Connect to AI → Any other AI** (**Your Site URL**).

### 4. Sign in and approve

Your own WordPress login page opens. Log in with your usual WordPress account and click **Allow Access**.

**That's it.** Codex can now use the tools you allowed.

## Try it

> *"Look at my site and tell me which theme, page builder and plugins it uses."*

> *"Change the footer text in my theme, give me a preview, and publish it once I say yes."*

> *"Why aren't my scheduled posts publishing? Check cron and the error log."*

> 🛡️ **Theme changes are safe to try.** They go into a private draft that is checked for errors and previewed before going live. If the site breaks after publishing, the change rolls back automatically.

## Something not working?

| What you see | What to do |
|---|---|
| Codex can't reach your site | Your site must be live on the internet with `https://`. Addresses on your own computer (`localhost`) or a private network won't work. Run the test in **Secure MCP Server → Troubleshooting**. |
| Connected, but Codex sees no tools | Check that your agent is turned on and that your WordPress role has tools ticked in **AI Agents**. |

More help: [Troubleshooting](troubleshooting.md) · [Full Codex guide on miniOrange's website](https://plugins.miniorange.com/connect-wordpress-with-codex-mcp-guide)
