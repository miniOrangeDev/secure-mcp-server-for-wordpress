# Connect Gemini to WordPress

Once you're connected, you can ask Gemini to write posts, update products, fix SEO and more on your WordPress site, all from a chat.

⏱️ About 2 minutes · No code needed

## Before you start

- The **Secure MCP Server** plugin is installed and you've **created an agent**. If not, see [Getting started](getting-started.md).
- You have a **Google account that can add custom connectors in Gemini**. Personal and Gemini Enterprise accounts can. Standard Google Workspace accounts can't. The plugin's connect guide also says to use a **Gemini Pro** plan.
- Your site is live on the internet with `https://`. Addresses on your own computer (`localhost`) or a private network won't work.

## Steps

### 1. Copy the Connection URL

In WordPress, go to **Secure MCP Server → Connect to AI** and choose **Gemini**. A panel opens with the **Connection URL** and **Your Site URL**. Copy the Connection URL:

```text
https://gateway.miniorange.ai/v2/mcp
```

Keep the panel open. You'll need **Your Site URL** from it in step 3.

### 2. Add the connector in Gemini

In Gemini, click **Customize**, then **Connectors**, then **Custom**.

- **MCP Server URL:** paste the Connection URL

Click **Next**. Accept the custom app guidelines and click **Connect**.

### 3. Enter your site's address

You'll land on the miniOrange sign-in page. Paste your site's address (**Your Site URL** from the plugin), for example `https://www.your-site.com`, and click **Continue**.

### 4. Sign in and approve

Your own WordPress login page opens. Log in with your usual WordPress account and click **Allow Access**. Gemini shows the abilities your role allows. Review them and click **Connect**.

**That's it.** Start chatting with your site in Gemini.

## Try it

> *"What can you do on my WordPress site?"*

> *"Show me the comments waiting for moderation."*

> *"Write meta descriptions for every post that doesn't have one."*

## Something not working?

| What you see | What to do |
|---|---|
| Gemini can't reach your site | Your site must be live on the internet with `https://`. Addresses on your own computer (`localhost`) or a private network won't work. Run the test in **Secure MCP Server → Troubleshooting**. |
| No "Custom" connector option | Your Google account may not support custom connectors. Standard Google Workspace accounts can't add them. |
| Connected, but Gemini sees no tools | Check that your agent is turned on and that your WordPress role has tools ticked in **AI Agents**. |

Each person connects Gemini with their own WordPress account, so one site can have several connections, each with its own permissions and its own entries in the **Activity Log**.

More help: [Troubleshooting](troubleshooting.md) · [Full Gemini guide on miniOrange's website](https://plugins.miniorange.com/connect-wordpress-with-gemini-mcp-guide)
