# Connect Antigravity to WordPress

Antigravity is Google's agent-first development environment, powered by Gemini. Once it's connected to your site, its agent can work on your WordPress content, theme and settings, all within the limits you set.

⏱️ About 3 minutes

## Before you start

- The **Secure MCP Server** plugin is installed and you've **created an agent**. If not, see [Getting started](getting-started.md).
- You have **Antigravity** installed and are signed in with your Google account.

## Steps

### 1. Copy the Connection URL

In WordPress, go to **Secure MCP Server → Connect to AI** and choose **Any other AI**. Copy the **Connection URL**:

```text
https://gateway.miniorange.ai/v2/mcp
```

Keep the panel open. You'll need **Your Site URL** from it in step 6.

### 2. Open Antigravity's MCP settings

In Antigravity, press **Ctrl + L** to open the Agent panel. Click the **More options** icon (top right of the panel) and choose **MCP Servers**. Open the **Manage MCP servers** tab and click **View raw config**.

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

### 4. Refresh

Go back to **Manage MCPs** and click **Refresh**. **wp-mcp-server** shows an **Unauthorized** error. This is expected until you sign in.

### 5. Start sign-in

Click **Authenticate**. Antigravity takes you to **Settings → Customizations**. Under **Installed MCP Servers**, click **Refresh**, then click **Authenticate**.

### 6. Enter your site's address

Your browser opens the miniOrange sign-in page. Paste your site's address (**Your Site URL** from the plugin), for example `https://www.your-site.com`, and click **Continue**.

### 7. Sign in and approve

Your own WordPress login page opens. Log in with your usual WordPress account and click **Allow Access**.

### 8. Paste the code back into Antigravity

The page shows an authentication code. Click **Copy to Clipboard**. Go back to **Settings → Customizations** in Antigravity, paste the code into the box under **wp-mcp-server**, and click **Submit**.

### 9. Refresh once more

Click **Refresh**. The error disappears and the number of available tools is shown.

**That's it.** Antigravity can now use the tools you allowed.

## Try it

> *"Look at my site and tell me which theme, page builder and plugins it uses."*

> *"Change the footer text in my theme, give me a preview, and publish it once I say yes."*

## Something not working?

| What you see | What to do |
|---|---|
| **Unauthorized** before signing in | Expected. Follow steps 5 to 9. |
| Still **Unauthorized** after submitting the code | Click **Refresh** again. If it stays, repeat steps 5 to 9 and make sure you copied the full code. |
| Antigravity can't reach your site | Your site must be live on the internet with `https://`. Run the test in **Secure MCP Server → Troubleshooting**. |
| Connected, but no tools | Check that your agent is turned on and that your WordPress role has tools ticked in **AI Agents**. |

More help: [Troubleshooting](troubleshooting.md) · [Full Antigravity guide on miniOrange's website](https://plugins.miniorange.com/connect-wordpress-with-antigravity-mcp-guide)
