# Changelog

What's new in each version of **Secure WordPress MCP Server**.

The latest version is always on [WordPress.org](https://wordpress.org/plugins/miniorange-secure-mcp-server/). To update, go to **Dashboard → Updates** in WordPress.

> ⚠️ **After updating:** new tools start **switched off** so nothing new is allowed without your say-so. Open **Secure MCP Server → AI Agents** and turn on the ones you want for each role.

---

## 1.5.6

**Highlights: exact edits inside Elementor widgets and read-only SEO tools (4 new tools)**

### Added
- **Exact edits for Elementor:** change a line of code in a large HTML widget, or a sentence in a long text block, without sending the whole widget back. Several edits can be made at once; they all apply or none do, and when a phrase is not found the AI is shown the closest text.
- **Full read of one Elementor element:** long HTML and text are no longer cut short when the AI reads them.
- **Read-only SEO tools:** read each post's SEO title, meta description, focus keywords and indexing, as saved and as search engines see them, or list the posts with SEO issues. They need only permission to read the post, so a Subscriber's AI can review SEO without editing rights. Works with Rank Math and Yoast SEO.

### Security
- Custom field and setting edits now refuse code a user is not allowed to add, such as scripts, iframes or onclick handlers, and say why. Posts and Elementor already worked this way.

## 1.5.5

**Highlights: logo and site icon, custom CSS and theme settings, image editing and upload links (15 new tools)**

### Added
- **Logo and site icon (3 tools):** see your site's logo and icon, and set or remove them from the media library or a web address. A site icon is cut to a 512 × 512 square the way the Customizer does it, keeping the part you name.
- **Additional CSS and theme settings (4 tools):** read and change the site's custom CSS, and every setting your theme offers in the Customizer, including Astra's. Each value is checked by the theme's own rules and saved through the Customizer when published.
- **Synced pattern tools:** see everywhere a pattern is used, turn one use into ordinary blocks, and delete a pattern safely by turning each remaining use into ordinary blocks, so no page loses its content.
- **Image editing:** crop by shape (16:9, square and so on) keeping the part you name, rotate, flip and resize, as a new image or in place with the original kept. Restore an original, and make missing image sizes.
- **Upload links:** the AI gives you a link to upload a file, such as a logo or a photo, straight into your media library. It works only for your account, behind your normal sign-in.
- **Previewed before going live:** logo, icon, CSS and theme settings wait in the theme draft, so you can preview them first. Publishing backs them up for one-step undo.
- **Everyone connects their own AI:** the approval screen, Connect page and AI Agents page now show that each person connects their own AI with their own WordPress account and gets only the abilities their role allows. The AI Agents page opens with a short guide to role-based AI access, which you can dismiss.
- **Team dashboard widget:** team members whose role has abilities see their role, how many abilities their AI gets and three steps to connect, with links to the connect steps and to **Your AI Access**. Administrators do not get it.
- **More setup guides:** the dashboard's connect guide now has steps for Gemini, Perplexity, Grok and Antigravity, including the plan each app needs to add a custom connector. The Connect page links to the Grok and Antigravity setup guides.

### Improved
- After a menu is assigned to a location or a widget is added to an area, the AI now checks the site's pages and says when the theme does not show it yet, and where to switch it on.
- WooCommerce, ACF, Yoast SEO, forms and Kadence changes now clear page caches automatically too.

### Security
- On sites that accept SVG files, SVGs added by AI are cleaned of scripts, outside links and CSS that could load files from other sites, and a drawing built to freeze the browser of whoever opens it is refused.
- Theme checks now use their short-lived sign-in only on this site's own pages and always remove it when they finish, so a post whose address points to another site (with Page Links To, for example) can no longer receive it.

### Fixed
- The role matrix on the AI Agents page no longer offers abilities to roles that cannot use them, such as deleting pages for a Subscriber, or WooCommerce's own product and order abilities for every role. WordPress still refused those calls, and grants like that are now flagged so you can turn them off.
- An agent that was switched off no longer loses its claim to the abilities it owns, which could let two agents own the same ability for a role. Saving now names the agent that already owns an ability.
- The plugin page no longer shows blank, or lets you click away, before the setup guide appears on a first visit.
- A warning on menu links to a #section of a page.
- Minor bug fixes.

## 1.5.4

**Highlights: block-by-block editing, menus, widgets and shareable previews (38 new tools)**

### Added
- **Block editor editing (11 tools):** list, find and read the blocks on any page or post; change one block's text or settings; insert, replace, move, duplicate and delete blocks, including patterns and synced patterns. Every other block stays exactly as it was, and every change saves a revision.
- **Menus and navigation (16 tools):** create, rename and delete menus; add, update, remove and reorder menu items; assign menu locations; edit block-theme Navigation menus, with undo.
- **Widgets and sidebars (8 tools):** list widget areas and widgets; add, update, move and delete widgets, including block widgets.
- **Shareable preview links:** an expiring link lets anyone view a draft without signing in. You can cancel it at any time.
- **Site overview:** tells the AI how your site is built (theme, page builder, plugins, caches) and which tools it may use.

### Improved
- Page caches, host caches and CDNs are now cleared automatically after every AI change, so changes show straight away. To keep busy sites fast, the whole cache is cleared at most once a minute; a changed page is always cleared immediately.
- When a tool exists but is switched off for a role, the AI now says so and explains how to turn it on, instead of "unknown tool".
- The AI is now told when content it writes would be saved as one Classic block, and how to write editable blocks instead.

### Fixed
- REST routes that plugins such as Media File Renamer only offer to signed-in users are now available to AI apps.
- Write requests through the REST API no longer arrive without data in plugins that read the request body as JSON.
- REST routes added by another plugin are picked up without reactivating it, and a route the user can't access is explained instead of returning "No route was found".
- Kadence headings and buttons now insert correctly into an empty column.
- Tools with no inputs no longer fail with "input is not of type object".

## 1.5.3

### Fixed
- AI apps are no longer disconnected when a sign-in refresh is interrupted by a timeout or restart.
- AI replies no longer break when another plugin prints PHP notices or warnings.

### Improved
- The Debug Log now always records failures, without usernames or IP addresses, with a request ID so a failed call can be traced end to end.
- AI apps get a log reference instead of a broken reply when a tool crashes.
- Troubleshooting: a gateway check that couldn't be completed is now shown as *inconclusive* instead of a failure.

## 1.5.2

### Added
- Cursor setup.

### Fixed
- AI apps failing to connect, or not seeing a new agent, on sites using LiteSpeed Cache or another page cache. *Purge your cache once after updating.*
- AI edits removing forms, scripts and styles, and dropping backslashes. AI edits now follow the same rules as editing by hand.
- Kadence block edits damaging links and settings in other blocks on the same page. *Affected pages can be restored from Revisions.*
- Kadence duplicate and delete reporting an error even though the change was made.

## 1.5.1

### Improved
- The Troubleshooting page now shows only likely connection problems.

## 1.5.0

### Added
- **Governed REST API access:** the AI can use the REST API of your other plugins, with per-role permissions. New agents start read-only.
- **Troubleshooting page** that finds out why an AI app can't connect.

### Improved
- Connection reliability with AI providers.

## 1.4.14

### Added
- **Theme editing for block themes:** templates, template parts, global styles, style variations and patterns.
- **Theme file editing:** read, search and change theme code in a private draft.
- Every theme change waits in a draft you can preview. Publishing backs up first and rolls back automatically if the site breaks.

### Improved
- The AI is told which inputs each tool needs and why a change was refused, including the closest matching text when wording isn't found.

## 1.4.13

### Added
- **Find and replace:** change part of a post, custom field or setting without rewriting it.
- **8 maintenance tools:** scheduled events, permalinks, caches and the error log.
- **Fluent Forms support (14 tools):** forms, fields, confirmations, notifications and submissions.

## 1.4.12

### Added
- **34 site administration tools:** site settings, plugin management, theme details, updates and Site Health.

## 1.4.11

### Added
- Rank Math SEO update tool.
- Sale schedule dates for WooCommerce products.

### Improved
- Security and performance of the connection flow.

## 1.4.10

### Fixed
- Page and edge caches (such as LiteSpeed or Cloudflare) could make a connected app report "No agent configured" even after an agent was enabled.

## 1.4.9

### Added
- Built-in debug log for connection and sign-in activity.

## 1.4.8
- Minor bug fixes.

## 1.4.7

### Added
- **Elementor support (10 tools):** read and edit Elementor pages, including text, images, links and styling, with separate tablet and mobile values.
- **Custom post types (19 tools):** edit items, custom fields, taxonomies, featured images and status for any content type.
- **Media uploads** from public links or supplied files, with real file-type checks.
- More **Yoast SEO** fields: breadcrumb title, canonical URL, focus keyphrase, social cards, robots, cornerstone content and schema.
- Editable **slugs**, with warnings about changed URLs.

## 1.4.6

### Added
- **Kadence Blocks support (17 tools):** read, edit and build Kadence pages, plus per-page layout options. Edits change only the targeted block.

## 1.4.5

### Improved
- ChatGPT is shown first when connecting, with clearer setup steps.
- A warning appears if your site is only reachable on localhost.
- Refreshed sign-in screen.

## 1.4.4
- Onboarding improvements.

## 1.4.3
- Minor bug fixes.

## 1.4.2

### Added
- **Role-and-tool grid:** see and compare what every role can do on one screen.
- **Onboarding checklist** for new installs.

## 1.4.1

### Added
- "Update Page" tool.

## 1.4.0

### Added
- **Tool library:** 260+ ready-to-use, security-reviewed tools for content, users, comments, WooCommerce, ACF, Yoast SEO, Contact Form 7, WPForms and Gravity Forms.
- **Test Connection** and **troubleshooting guide**.

### Improved
- Security hardening: protected user data can't be accessed, and CSV exports are protected against spreadsheet formula injection.

## 1.3.1
- Minor fixes and reliability improvements.

## 1.3.0

### Added
- **Activity log:** a full record of every tool call, with filters and details.
- **Dashboard:** active agents, total actions, success rate and average response time.

## 1.2.3
- Clearer role-and-tool editor and general polish.

## 1.2.2

### Added
- **Role-based Agent Registry:** grant tools to each WordPress role.
- **"My AI Access"** view so every user can see the tools available to them.

## 1.2.1

### Added
- Contact Support button and quick Setup Guide link.

## 1.2.0

### Added
- **Agent Registry** for managing connected AI apps.
- On/off switch for each tool.
- Redesigned interface.

## 1.1.1
- In-plugin support form.

## 1.1.0

### Added
- **MCP server** that offers WordPress abilities as tools to AI apps.
- **Secure sign-in** (OAuth 2.1 with PKCE) so ChatGPT and Claude can connect.

## 1.0.0
- First release: a read-only viewer for WordPress abilities.
