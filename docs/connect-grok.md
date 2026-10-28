# Connect Grok to WordPress

Once you're connected, you can ask Grok to write posts, update products, fix SEO and more on your WordPress site, all from a chat.

⏱️ About 2 minutes · No code needed

## Before you start

- The **Secure MCP Server** plugin is installed and you've **created an agent**. If not, see [Getting started](getting-started.md).
- You have a **Grok account** that can add custom connectors. Depending on your Grok plan, this may need to be switched on first.

## Steps

### 1. Copy the Connection URL

In WordPress, go to **Secure MCP Server → Connect to AI** and choose **Any other AI**. Copy the **Connection URL**:

```text
https://gateway.miniorange.ai/v2/mcp
```

Keep the panel open. You'll need **Your Site URL** from it in step 4.

### 2. Open Connectors in Grok

In Grok, click **Plugins** in the bottom-left menu. On the **Connectors** page, click **New Connector** (top right) and choose **Custom**.

### 3. Add the connector

- **Name:** anything you'll recognise, such as *My WordPress site*
- **Server URL:** paste the Connection URL

Click **Add Connector**.

### 4. Enter your site's address

You'll land on the miniOrange sign-in page. Paste your site's address (**Your Site URL** from the plugin), for example `https://www.your-site.com`, and click **Continue**.

### 5. Sign in and approve

Your own WordPress login page opens. Log in with your usual WordPress account and click **Allow Access**.

**That's it.** Start chatting with your site in Grok.

## Try it

> *"What can you do on my WordPress site?"*

> *"Show me the comments waiting for moderation."*

> *"Write meta descriptions for every post that doesn't have one."*

## Something not working?

| What you see | What to do |
|---|---|
| Grok can't reach your site | Your site must be live on the internet with `https://`. Addresses on your own computer (`localhost`) or a private network won't work. Run the test in **Secure MCP Server → Troubleshooting**. |
| No "Custom" connector option | Your Grok plan may not include custom connectors, or the feature may need to be switched on. |
| Connected, but Grok sees no tools | Check that your agent is turned on and that your WordPress role has tools ticked in **AI Agents**. |

More help: [Troubleshooting](troubleshooting.md) · [Full Grok guide on miniOrange's website](https://plugins.miniorange.com/connect-wordpress-with-grok-mcp-guide)
