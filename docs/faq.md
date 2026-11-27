# Frequently asked questions

## The basics

### What does this plugin do?
It lets AI assistants like Claude, ChatGPT and Cursor work on your WordPress site. You ask in plain language ("schedule this post for Monday", "put these products on sale") and the AI does it, within limits you set.

### What is MCP?
MCP (Model Context Protocol) is an open standard that lets AI assistants use tools in other apps, a bit like a universal plug. This plugin turns your WordPress site into an "MCP server", so any AI app that supports MCP can connect to it. You don't need to understand MCP to use the plugin.

### Do I need to know how to code?
No. You install the plugin, tick which tools to allow, and connect your AI app by clicking through a few screens. See [Getting started](getting-started.md).

### Is it free?
Yes. The plugin is free on [WordPress.org](https://wordpress.org/plugins/miniorange-secure-mcp-server/) with all 518 tools, role permissions, secure sign-in and the activity log. The paid **Pro** plan adds 254 more tools for 39 plugin integrations and bulk media, including Divi, and the **Business** plan adds human approval and data-masking rules on top. [See pricing](https://plugins.miniorange.com/mcp-server-ai-policy-enforcement-wordpress#pricing).

### Which AI apps work with it?
Claude, ChatGPT, Gemini, Grok, Cursor, Codex, Windsurf, Antigravity, Perplexity, Gemini CLI, VS Code, Claude Code and any other app that supports remote MCP servers. You can connect several at once. Each app has its own setup guide; see [Getting started](getting-started.md#step-3-connect-your-ai-app).

### How many tools are there?
518 in the free plan, covering WordPress content, the block editor, menus, widgets, users, settings, theme editing and maintenance, plus WooCommerce, Yoast SEO, Rank Math, Advanced Custom Fields, Elementor, Kadence, Contact Form 7, WPForms, Gravity Forms and Fluent Forms, Wordfence and UpdraftPlus, and four tools for Governed REST API access. The Pro plan adds 254 more for 39 plugin integrations, 772 in all. Tools for another plugin only appear when that plugin is active. See [What your AI can do](what-your-ai-can-do.md).

## Safety

### Is it safe to give AI access to my site?
The plugin was built for exactly this. The AI never sees your password, it can only use the tools you allow for each role, every action is checked against WordPress's own permissions, and everything is logged. See [Security and control](security-and-control.md).

### Can the AI do more than I can?
No. The AI acts as the WordPress user who connected it, and every action is checked against that user's permissions, exactly as in wp-admin.

### Can the AI break my site or theme?
Theme changes never go straight to your live site. They go into a draft, are checked for errors, can be previewed, and are backed up when published. If the site fails, the change rolls back automatically. Content edits save revisions you can restore, and deleting things needs confirmation.

### What if the AI makes a mistake?
- **Page lock** stops the AI from overwriting a page someone else changed in the meantime.
- **Revisions** let you roll any post back.
- **Theme changes** can be undone with one restore.
- **The activity log** shows exactly what happened.

### How do I stop an AI's access?
Click **Revoke** in **AI Agents**. Access ends immediately. You can also pause an agent or switch off any individual tool.

### Does my data go through a third party?
The tools run, and every permission is checked, on your own WordPress site. Your AI app's requests pass through the **miniOrange Gateway** (`gateway.miniorange.ai`) on their way to your site. Sign-in happens on your own WordPress login page.

## Features

### Does it work with WooCommerce?
Yes. 41 tools cover products, orders, refunds, customers, coupons and sales reports.

### Does it work with Yoast SEO and Rank Math?
Yes. The AI can update SEO titles, meta descriptions, focus keywords, schema, social cards, canonicals, robots settings and more.

### Does it work with Elementor, Divi or Kadence?
Yes. Elementor (12 tools) and Kadence Blocks (18 tools) are in the free plan. The Pro plan adds Divi 4 and Divi 5 (22 tools), more Elementor Pro tools (16), and Bricks, Beaver Builder, WPBakery, Avada Builder, Breakdance and Oxygen.

### Which plugins does the Pro plan add?
254 more tools for 39 plugin integrations and bulk media: Divi 4 and 5, Elementor Pro, Bricks, Beaver Builder, WPBakery, Avada Builder, Breakdance and Oxygen; WooCommerce Subscriptions, Bookings and Memberships, Subscriptions for WooCommerce, Easy Digital Downloads, MemberPress and Paid Memberships Pro; Tutor LMS, LearnDash and LifterLMS; Rank Math SEO, All in One SEO, SEOPress and Yoast SEO Premium; Advanced Custom Fields Pro, Meta Box and JetEngine; WPML, Polylang and TranslatePress; Formidable Forms, Ninja Forms and Forminator; FluentCRM and MailPoet; The Events Calendar, Event Tickets and Events Calendar Pro; Houzez; and WP Rocket. It also adds four media library tools that need no plugin: find media used nowhere on the site and delete it, resize large images in bulk, and set alt text in bulk. Each set only appears when that plugin is active. See the [full list with tool counts](what-your-ai-can-do.md#pro-plan-254-more-tools).

### Can the AI edit just one part of a page?
Yes. For block-editor pages it can change a single heading, paragraph or button and leave every other block exactly as it was. In Elementor it can change one line of code in a large HTML widget, or one sentence in a long text block, without resending the whole widget. It can also find and replace one sentence inside a post or setting.

### Can someone without edit rights review my SEO?
Yes. The read-only SEO tools show each post's SEO title, meta description, focus keywords and indexing, or list posts with SEO issues. They need only permission to read the post, so even a Subscriber's AI can review SEO without being able to change it. They work with Rank Math and Yoast SEO.

### Can the AI change my logo, site icon or custom CSS?
Yes. It can set or remove your logo and site icon from the media library or a web address, and read and change your Additional CSS and your theme's Customizer settings, including Astra's. These changes wait in the theme draft so you can preview them, and publishing backs them up for one-step undo.

### Can the AI edit my images?
Yes. It can crop (by shape, such as 16:9 or square, keeping the part you name), rotate, flip and resize, either as a new image or in place with the original kept. It can restore an original and make missing image sizes. It can also give you an upload link to add a file yourself, which works only for your account.

### Can it use my other plugins?
Yes. With **Governed REST API access**, the AI can use the REST API of almost any plugin, such as booking, membership or LMS plugins. It's read-only by default, and you allow writes route by route.

### Does it work on WordPress multisite?
Yes. **Network Admin → Secure MCP Server** lists every site on the network with a link to its settings. Plugin tools are offered only to people who can manage plugins for the network, and the AI can't look up users who don't belong to the site it's working on.

### Is the plugin available in my language?
The admin, the approval screen and the deactivation form are available in Arabic (laid out right to left), Chinese (Simplified), German, Italian, Japanese and Russian, and follow each person's WordPress language. What the AI sees stays in English.

### Can I connect more than one AI app?
Yes, as many as you like. Each has its own permissions and its own entries in the log.

### Can my team use it?
Yes. Each team member connects their own AI app and gets the tools allowed for their WordPress role. Members can open **Your AI Access** in WordPress to see what they're allowed to do and how to connect.

## Setup problems

### Why can't my AI app reach my site?
AI apps need your site to be **live on the internet with HTTPS**. A site on your own computer (localhost) or behind a firewall can't be reached. Run the test in **Secure MCP Server → Troubleshooting**. See [Troubleshooting](troubleshooting.md).

### Why doesn't the AI see any tools?
Usually there's no enabled agent, or the connecting user's role has no tools ticked. Check **AI Agents**. After a plugin update, new tools start switched off.

### Why don't I see the AI's change on my site?
Caches are cleared automatically, but site-wide changes like menus can take up to a minute to show. If you use an unusual cache, clear it manually or ask the AI to clear caches.

### What are the requirements?
WordPress 6.9 or newer, PHP 7.4 or newer (8.0+ recommended), and a public HTTPS site.
