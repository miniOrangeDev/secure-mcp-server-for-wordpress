# Getting started

This guide takes you from nothing to chatting with your WordPress site in about 2 minutes. You don't need to write any code.

**On this page**
1. [Before you start](#before-you-start)
2. [Install the plugin](#step-1-install-the-plugin)
3. [Create your first agent](#step-2-create-your-first-agent)
4. [Connect your AI app](#step-3-connect-your-ai-app)
5. [Try it out](#step-4-try-it-out)

---

## Before you start

Check that you have:

- ✅ **Admin access to a WordPress site** running WordPress 6.9 or newer
- ✅ **A site that is live on the internet with HTTPS**, meaning its address starts with `https://`. A site that only runs on your own computer (`localhost`) can't be reached by AI apps.
- ✅ **An AI app** such as Claude, ChatGPT or Cursor. Some apps only offer connectors on certain paid plans.

## Step 1: Install the plugin

1. Log in to your WordPress dashboard.
2. Go to **Plugins → Add New Plugin**.
3. Search for **Secure MCP Server**.
4. Click **Install Now** on *Secure MCP Server for Claude, ChatGPT, Gemini and other AI Agents* by miniOrange, then click **Activate**.

You'll see **Secure MCP Server** in your WordPress admin sidebar.

**Installing from a zip file instead:**

1. Download the plugin zip from [WordPress.org](https://wordpress.org/plugins/miniorange-secure-mcp-server/) (or the zip you received from miniOrange).
2. In WordPress, go to **Plugins → Add New Plugin → Upload Plugin**.
3. Choose the zip file, click **Install Now**, then **Activate**.

## Step 2: Create your first agent

An **agent** is a set of rules that says what the AI is allowed to do on your site, for each WordPress user role. The AI can't do anything until you've created one.

1. Open **Secure MCP Server** from the admin sidebar.
2. Click **Register your first agent**.
3. Give the agent a name you'll recognise, such as *Content assistant*, and click **Next**.
4. Choose which tools each user role can use. You'll see a grid with tools down the side and roles across the top.
   - **Not sure what to pick?** Start small. Give your own role the content tools (posts, pages, media) and add more later.
   - Use **Select all** or **Clear** to tick a whole category or a whole role at once.
5. Click **Create & Continue**, then **Continue**.

You'll now see **Connect your AI client**.

> 💡 **Tip:** The rules apply to the person who connects the AI. If an *Editor* connects ChatGPT, ChatGPT gets the Editor's tools, and is still limited to what an Editor can normally do in WordPress.

## Step 3: Connect your AI app

Pick your app in the plugin, or use the guide for it below:

- [Connect Claude](connect-claude.md)
- [Connect ChatGPT](connect-chatgpt.md)
- [Connect Cursor](connect-cursor.md)
- [Connect Grok](connect-grok.md)
- [Connect Codex](connect-codex.md)
- [Connect Windsurf](connect-windsurf.md)
- [Connect Antigravity](connect-antigravity.md)
- [Connect another AI app](connect-other-ai-apps.md): Gemini, Perplexity, Gemini CLI, VS Code, Claude Code and others

Every app follows the same pattern:

1. **Add the connector** in your AI app.
2. **Enter your site's address** when the miniOrange sign-in page asks for it.
3. **Log in to WordPress** and click **Allow access**.

Your WordPress password is entered on *your own site*, never in the AI app.

## Step 4: Try it out

Start a new chat in your AI app and try something harmless first:

> *"What can you do on my WordPress site?"*

> *"List my 5 most recent posts."*

> *"Show me the comments waiting for moderation."*

Then try something real:

> *"Draft a blog post about our opening hours over the holidays. Don't publish it, just save it as a draft and give me a preview link."*

More ideas: [What your AI can do](what-your-ai-can-do.md)

## What's next?

- **Check the activity log.** Open **Secure MCP Server → Activity Log** to see every action the AI took.
- **Add more tools as you need them.** Open **AI Agents**, edit your agent and tick more boxes. When you update the plugin, new tools start switched off, so turn on the ones you want.
- **Invite your team.** Each team member connects their own AI app with their own WordPress account. Each person gets only the tools their role allows, and their own entries in the log. Members whose role has tools see a dashboard widget with their role, how many tools their AI gets and three steps to connect, and can open **Your AI Access** to see which tools they have. Administrators don't see the widget.
- **Something not working?** Open the plugin's **Troubleshooting** tab, or read the [troubleshooting guide](troubleshooting.md).
