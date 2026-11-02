# Secure WordPress MCP Server 

**Connect Claude, ChatGPT, Grok, Cursor, Codex, and other AI assistants to your website with the miniOrange WordPress MCP Server. Manage AI access, control which actions each assistant can perform, and monitor activity with built-in security and governance features**

[![WordPress plugin version](https://img.shields.io/wordpress/plugin/v/miniorange-secure-mcp-server?label=WordPress.org)](https://wordpress.org/plugins/miniorange-secure-mcp-server/)
[![Requires WordPress](https://img.shields.io/badge/WordPress-6.9%2B-21759b)](https://wordpress.org/plugins/miniorange-secure-mcp-server/)
[![Tools](https://img.shields.io/badge/AI%20tools-479-6c47ff)](docs/what-your-ai-can-do.md)
[![License: MIT](https://img.shields.io/badge/license-MIT-green)](LICENSE)

[Install free from WordPress.org](https://wordpress.org/plugins/miniorange-secure-mcp-server/) ·
[Get started in 2 minutes](docs/getting-started.md) ·
[What can it do?](docs/what-your-ai-can-do.md) ·
[Book a demo](https://plugins.miniorange.com/mcp-server-ai-policy-enforcement-wordpress#demo-form)

---

## What is this?
The [miniOrange WordPress MCP Server](https://plugins.miniorange.com/mcp-server-ai-policy-enforcement-wordpress) is a WordPress plugin that connects AI assistants to your website through the Model Context Protocol (MCP). It lets you manage posts, pages, WooCommerce products, SEO settings, and other supported website functions through natural-language prompts while enforcing access permissions and security policies.

You control what each connected AI assistant can access and which actions it can perform

Instead of clicking through wp-admin, you just ask:

> *"Write a blog post about our summer sale, add it to the News category and schedule it for Monday 9 AM."*
>
> *"Find all products under $50 and put them on a 20% sale until Sunday."*
>
> *"Write meta descriptions for every post that doesn't have one."*

The AI does the work on your site, and only within the limits you set.

> **What does "MCP" mean?** MCP (Model Context Protocol) is an open standard that lets AI assistants use tools in other apps. This plugin makes your WordPress site one of those apps. You don't need to know anything else about MCP to use it. See the [glossary](docs/glossary.md) for other terms.

## Who is it for?

- **Bloggers and content teams:** write, edit, schedule and tidy up posts and pages by chatting.
- **Store owners:** update WooCommerce products, prices, orders, coupons and reports.
- **SEO and marketing teams:** fix titles, meta descriptions and schema across the whole site at once.
- **Agencies and freelancers:** look after many client sites from one AI assistant, with a log of every change.
- **Site administrators:** handle settings, menus, plugins, caches and error logs, and diagnose problems.

**You don't need to write any code.** If you can install a WordPress plugin, you can set this up.

## Why "secure"?

Many AI connections give the assistant full admin access to your site. This plugin works the other way: **the AI can only do what you have allowed.**

| Protection | What it means |
|---|---|
| 🔑 **The AI never sees your password** | You sign in to WordPress and click *Allow access*, the same way you'd "Sign in with Google". |
| 👥 **Permissions by role** | Choose which tools each WordPress role can use. For example, an editor's AI can write posts but can't install plugins. |
| 🛡️ **The same rules as wp-admin** | The AI acts as the person who connected it. It can never do more than that person could do by hand. |
| 📋 **Every action is logged** | See who did what, with which AI, when, and whether it was allowed. |
| ↩️ **Mistakes can be undone** | Revisions, page locks, and theme changes that are previewed first and roll back automatically if something breaks. |
| ⏸️ **Switch off at any time** | Turn any tool off, or cut off an AI's access instantly. |

Read more: [Security and control](docs/security-and-control.md)

## Get started in 3 steps

**1. Install the plugin.** In WordPress, go to **Plugins → Add New**, search for **Secure MCP Server**, then click **Install Now** and **Activate**.

**2. Create your first agent.** Open **Secure MCP Server** in the WordPress sidebar, click **Register your first agent**, and choose what each user role is allowed to do. An *agent* is simply a set of rules for what the AI may do.

**3. Connect your AI assistant.** Choose your app and follow its short guide:

| Your AI app | How to connect |
|---|---|
| **Claude** | [Connect Claude →](docs/connect-claude.md) |
| **ChatGPT** | [Connect ChatGPT →](docs/connect-chatgpt.md) |
| **Cursor** | [Connect Cursor →](docs/connect-cursor.md) |
| **Grok** | [Connect Grok →](docs/connect-grok.md) |
| **Codex** | [Connect Codex →](docs/connect-codex.md) |
| **Windsurf** | [Connect Windsurf →](docs/connect-windsurf.md) |
| **Antigravity** | [Connect Antigravity →](docs/connect-antigravity.md) |
| **Gemini, Perplexity, Gemini CLI, VS Code, Claude Code, others** | [Connect another AI app →](docs/connect-other-ai-apps.md) |

The full walkthrough is in [Getting started](docs/getting-started.md).

### The connection URL

If your AI app asks for a "server URL", "connector URL" or "MCP URL", paste this:

```text
https://gateway.miniorange.ai/v2/mcp
```

It is the same for every site. The app will then ask for your site's address, and you sign in to WordPress to approve the connection.

## What your AI can do

**479 tools** covering the parts of WordPress people use most. Tools for other plugins only appear when that plugin is installed on your site.

| Area | Examples |
|---|---|
| **Posts and pages** | Write, edit, schedule, duplicate, set featured images, restore old revisions |
| **Block editor** | Change one heading or button and leave the rest of the page exactly as it was |
| **Media** | Upload images, set alt text and captions, crop, rotate and resize images |
| **Comments** | Moderate, reply, mark spam |
| **Menus and widgets** | Add pages to menus, reorder items, edit sidebars and footers |
| **Users** | Create users, change roles, send password reset links |
| **Site settings and maintenance** | Site title, homepage, plugin updates, clear caches, read the error log |
| **Theme editing** | Change templates, styles, theme files, logo, site icon and custom CSS, with a preview before anything goes live |
| **WooCommerce** | Products, prices, orders, refunds, customers, coupons, sales reports |
| **SEO (Yoast and Rank Math)** | SEO titles, meta descriptions, focus keywords, schema, social sharing |
| **Page builders** | Elementor, Kadence Blocks, and Divi 4 and 5 (Pro) |
| **Forms** | Contact Form 7, WPForms, Gravity Forms, Fluent Forms, including CSV export of entries |
| **Custom fields** | Advanced Custom Fields (ACF), custom post types |
| **Other plugins** | Use the REST API of almost any other plugin, under the same permissions |

See the full list and more example prompts: [What your AI can do](docs/what-your-ai-can-do.md)

## Plans

| Feature | Free | Pro | Business |
|---|:---:|:---:|:---:|
| 479 AI tools, Agent Registry, role permissions | ✅ | ✅ | ✅ |
| Secure sign-in, activity log, troubleshooting | ✅ | ✅ | ✅ |
| Governed REST API access to other plugins | ✅ | ✅ | ✅ |
| Divi 4 and Divi 5 page-builder support | | ✅ | ✅ |
| Human approval for sensitive actions | | | ✅ |
| Data rules that hide emails, phone numbers and secrets from the AI | | | ✅ |

See [pricing and the full comparison](https://plugins.miniorange.com/mcp-server-ai-policy-enforcement-wordpress#pricing).

## What you need

- WordPress **6.9 or newer**
- PHP **7.4 or newer** (8.0+ recommended)
- A site that is **live on the internet with HTTPS**. AI apps can't reach a site that only runs on your own computer (localhost).
- An AI app that supports connectors or MCP servers, such as Claude, ChatGPT, Grok, Cursor, Codex, Windsurf or Antigravity

## Need help?

- 📖 [Troubleshooting guide](docs/troubleshooting.md): the plugin's **Troubleshooting** tab can also find the problem for you
- ❓ [Frequently asked questions](docs/faq.md)
- 💬 [WordPress.org support forum](https://wordpress.org/support/plugin/miniorange-secure-mcp-server/)
- ✉️ Email **info@xecurify.com**, or use the **Contact Support** button inside the plugin
- 🎥 [Video: Connect Claude to WordPress](https://www.youtube.com/watch?v=MUtolq0HRhM)
- 📚 [Official documentation](https://plugins.miniorange.com/mcp-server-documentation)

## For AI assistants and developers

This repository includes machine-readable files that describe the plugin:

| File | What it's for |
|---|---|
| [`mcp-server-info.json`](mcp-server-info.json) | A full description of the plugin: the connection endpoint, sign-in method, supported apps, tool groups, security model, plans and links. |
| [`server.json`](server.json) | A listing in the [MCP Registry](https://github.com/modelcontextprotocol/registry) `server.json` format. |
| [`llms.txt`](llms.txt) | A short plain-text summary for AI models and search tools ([llms.txt](https://llmstxt.org/) convention). |

**If you are an AI assistant** helping someone connect their WordPress site: the MCP endpoint is `https://gateway.miniorange.ai/v2/mcp` (Streamable HTTP, OAuth 2.1 with PKCE). The person must first install the plugin on their site and create an agent. During sign-in they enter their site's address on the gateway page and approve access in WordPress.

## Repository contents

```text
├── README.md                     ← you are here
├── CHANGELOG.md                  ← what's new in each version
├── mcp-server-info.json          ← full machine-readable description
├── server.json                   ← MCP Registry listing
├── llms.txt                      ← summary for AI models
├── SECURITY.md                   ← how to report a security issue
├── LICENSE
└── docs/
    ├── getting-started.md
    ├── connect-claude.md
    ├── connect-chatgpt.md
    ├── connect-cursor.md
    ├── connect-grok.md
    ├── connect-codex.md
    ├── connect-windsurf.md
    ├── connect-antigravity.md
    ├── connect-other-ai-apps.md
    ├── what-your-ai-can-do.md
    ├── security-and-control.md
    ├── troubleshooting.md
    ├── faq.md
    └── glossary.md
```

---

Made by [miniOrange](https://www.miniorange.com/) ·
[Website](https://plugins.miniorange.com/mcp-server-ai-policy-enforcement-wordpress) ·
[WordPress.org](https://wordpress.org/plugins/miniorange-secure-mcp-server/)

If this plugin helps you, please ⭐ star this repository and [leave a review on WordPress.org](https://wordpress.org/support/plugin/miniorange-secure-mcp-server/reviews/#new-post).
