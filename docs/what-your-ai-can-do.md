# What your AI can do

The plugin gives your AI assistant **483 tools**: actions it can take on your WordPress site. You choose which ones each user role can use, and you can switch any of them off.

Tools for other plugins (like WooCommerce or Yoast) **only appear if that plugin is installed and active** on your site.

**Jump to:** [Content](#your-content) · [Site management](#site-management) · [Online store](#online-store-woocommerce) · [SEO](#seo-yoast-seo-and-rank-math) · [Page builders](#page-builders) · [Forms](#forms-and-leads) · [Custom fields](#custom-fields-acf) · [Other plugins](#other-plugins-governed-rest-api-access) · [Example prompts](#example-prompts)

---

## Your content

| Area | Tools | What the AI can do |
|---|---:|---|
| **Posts and pages** | 56 | Write, edit, publish, schedule, duplicate, set page templates and featured images, trash and restore |
| **Categories, tags and media** | 45 | Manage categories and tags, upload images from a link or file, update alt text and captions; crop, rotate, flip and resize images while keeping the original; get an upload link to add a file yourself |
| **Block editor** | 12 | Change *one* heading, paragraph or button and leave every other block exactly as it was; insert, move, duplicate and delete blocks and patterns; see where a synced pattern is used and turn it into ordinary blocks |
| **Find and replace** | 6 | Change one sentence in a post, custom field or setting without rewriting the whole thing |
| **Revisions** | 9 | List, compare and restore earlier versions |
| **Comments** | 21 | Moderate, reply, search and mark spam |
| **Custom post types and fields** | 19 | Work with any custom content type, such as portfolios, events or team members |
| **Preview links** | 2 | Create an expiring link so anyone can view a draft without logging in |

## Site management

| Area | Tools | What the AI can do |
|---|---:|---|
| **Users and roles** | 38 | Create users, assign roles, update profiles, send password reset links |
| **Settings, plugins, themes and updates** | 34 | Site title, tagline, homepage, timezone; activate and update plugins; check site health |
| **Menus and navigation** | 16 | Build menus, add and reorder items, assign menu locations, edit block-theme navigation |
| **Widgets and sidebars** | 8 | Add, update, move and delete widgets, including block widgets |
| **Theme editing** | 41 | Edit templates, global styles, patterns and theme files; set the logo and site icon; change Additional CSS and your theme's Customizer settings. Always in a draft you preview first |
| **Maintenance** | 8 | Clear caches, refresh permalinks, run scheduled tasks, read the error log |
| **Site overview** | 1 | Tells the AI how your site is built (theme, page builder, plugins) so it picks the right tools |

## Online store (WooCommerce)

**41 tools.** Run your store by chatting with it:

- Create and update **products**, attributes, categories and tags, including sale prices and sale dates
- Look up, create and update **orders**, change order status, add notes and issue **refunds**
- Manage **customers**, see purchase history and customer groups
- Create and update **coupons**
- Get **reports**: sales, orders, products, customers, coupon usage and top sellers

## SEO (Yoast SEO and Rank Math)

**17 tools.** Update SEO titles and meta descriptions in bulk, set focus keywords, mark cornerstone content, and control robots settings, canonical URLs, breadcrumb titles and sitemap inclusion. Manage Open Graph and X (Twitter) cards and schema types. Rank Math SEO data is supported too. **Read-only SEO tools** let the AI review each post's SEO title, meta description, focus keywords and indexing, or list posts with SEO issues, with only permission to read the post, so even a Subscriber's AI can run an SEO review without editing rights.

## Page builders

| Builder | Tools | What the AI can do |
|---|---:|---|
| **Elementor** | 12 | Read a page layout or one whole element; change text, images, links and styling without breaking the design; fix one line of code in a large HTML widget or one sentence in a long text block; move, duplicate or delete elements; preview the result |
| **Kadence Blocks** | 18 | Build new Kadence pages; insert rows, columns, headings, buttons, icons and images; update text and styling |
| **Divi 4 and Divi 5** | Pro plan | Read Divi layouts and update modules, text, images, links and styling without opening the visual builder |

Pages made with the normal WordPress block editor use the **Block editor** tools above.

## Forms and leads

**54 tools** for **Contact Form 7** (with Flamingo), **WPForms**, **Gravity Forms** and **Fluent Forms**:

- List forms and fields; read and count entries
- Mark entries read or unread; trash, restore or delete them
- **Export entries as CSV**
- Check form settings and notifications. With Fluent Forms, the AI can also create, update and test notifications and confirmation messages.

## Custom fields (ACF)

**25 tools** for **Advanced Custom Fields**: read and update any field value, work with repeaters, flexible content, relationships and options pages, create field groups and fields, and search posts by field value.

## Other plugins: Governed REST API access

Beyond the 483 built-in tools, the AI can use the **REST API** of almost any plugin on your site, such as a booking, membership or LMS plugin, with no plugin update needed.

You stay in control:

- **Read-only to start.** A new agent can read posts, pages and media. Anything that *changes* data needs your permission.
- **Route by route.** Allow each route, for reading or writing, per user role.
- **Global off switches.** Turn off all create, update or delete actions for the whole site in one click.
- **Dangerous actions are always blocked.** Installing or activating plugins and themes, batch requests and blueprint imports can never be allowed this way.

---

## Example prompts

Copy any of these into your AI app.

**Content**
- *"Write a blog post about our summer sale, add it to the News category and schedule it for Monday 9 AM."*
- *"Change the heading in my homepage hero to 'Spring Collection'."*
- *"Replace 'Call us on 555-0100' with 'Call us on 555-0199' everywhere on the site."*
- *"Draft a post about our new service and send me a preview link I can share with my team."*
- *"Crop this photo to 16:9, keeping the left side, and save it as a new image."*

**Store**
- *"Find all products under $50 and put them on a 20% sale until Sunday."*
- *"Which were our top 10 products last month?"*
- *"Create a coupon WELCOME10 for 10% off first orders, valid until the end of the year."*

**SEO**
- *"Write meta descriptions for every post that doesn't have one."*
- *"Which pages are set to noindex? List them for me."*
- *"Which posts have SEO issues, such as a missing meta description?"*

**Site upkeep**
- *"Add our new Pricing page to the main menu, right after About."*
- *"Why aren't my scheduled posts publishing? Check cron and the error log."*
- *"Which plugins have updates available?"*
- *"Change the footer text in my theme, preview it, then publish."*
- *"Set our new logo as the site logo and the site icon, and let me preview it before it goes live."*
- *"Add some custom CSS to make the header buttons rounded."*

**Forms**
- *"Export this month's Gravity Forms entries as CSV."*
- *"How many contact form messages did we get this week?"*

**Other plugins**
- *"Use the REST API to list this week's bookings from my booking plugin."*

---

**Want to see what's switched on?** In WordPress, open **Secure MCP Server → Abilities** to see every tool, or **Your AI Access** to see which tools your role has.
