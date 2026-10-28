# Connect Windsurf to WordPress

Windsurf is an AI code editor, and its AI assistant is called Cascade. Once it's connected to your site, Cascade can work on your WordPress content, theme and settings while you build, all within the limits you set.

⏱️ About 3 minutes

## Before you start

- The **Secure MCP Server** plugin is installed and you've **created an agent**. If not, see [Getting started](getting-started.md).
- You have **Windsurf** installed and are signed in.

## Steps

### 1. Copy the Connection URL

In WordPress, go to **Secure MCP Server → Connect to AI** and choose **Any other AI**. Copy the **Connection URL**:

```text
https://gateway.miniorange.ai/v2/mcp
```

Keep the panel open. You'll need **Your Site URL** from it in step 5.

### 2. Open Windsurf's MCP settings

In Windsurf, open the **Cascade** panel. Click the **Actions** icon (top right of Cascade), then **Open Customizations**. Go to the **Installed** tab and click **Add custom MCP**.

### 3. Add the server

A file called `mcp_config.json` opens. Paste this in, then save the file:

```json
{
  "mcpServers": {
    "wp-mcp-server": {
      "serverUrl": "https://gateway.miniorange.ai/v2/mcp"
    }
  }
}
```

> If the file already lists other servers, add the `"wp-mcp-server": { ... }` entry inside the existing `"mcpServers"` section instead of replacing the whole file.

### 4. Connect

Go back to the **Installed** tab. **wp-mcp-server** shows as **Not connected**. This is expected until you sign in. Click **wp-mcp-server**, then click **Connect**.

### 5. Enter your site's address

Your browser opens the miniOrange sign-in page. Paste your site's address (**Your Site URL** from the plugin), for example `https://www.your-site.com`, and click **Continue**.

### 6. Sign in and approve

Your own WordPress login page opens. Log in with your usual WordPress account and click **Allow Access**.

**That's it.** Go back to Windsurf. The status changes to **Connected** and your tools are listed.

## Try it

Ask Cascade:

> *"Look at my site and tell me which theme, page builder and plugins it uses."*

> *"List my draft posts and tell me which ones are missing a featured image."*

## Something not working?

| What you see | What to do |
|---|---|
| Status stays **Not connected** | Finish the browser sign-in and make sure you clicked **Allow Access**. |
| Not sure which URL goes where | The **Connection URL** goes in `mcp_config.json`. **Your Site URL** (your WordPress address) goes on the sign-in page. |
| Windsurf can't reach your site | Your site must be live on the internet with `https://`. Run the test in **Secure MCP Server → Troubleshooting**. |
| Connected, but no tools | Check that your agent is turned on and that your WordPress role has tools ticked in **AI Agents**. |

More help: [Troubleshooting](troubleshooting.md) · [Full Windsurf guide on miniOrange's website](https://plugins.miniorange.com/connect-wordpress-with-windsurf-mcp-guide)
