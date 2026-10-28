# Troubleshooting

> 🩺 **The quickest fix:** in WordPress, open **Secure MCP Server → Troubleshooting** and run the connection test. It checks your site from the inside *and* from the outside, shows only the problems that are likely to be real, and tells you exactly what to change and who can change it (you or your web host).

If you'd rather read first, find what you're seeing below.

**Jump to:** [Can't connect](#the-ai-app-cant-reach-my-site) · [No tools](#connected-but-the-ai-sees-no-tools-or-fewer-than-expected) · [Stops working after connecting](#it-connects-but-every-request-fails) · [Works sometimes](#it-works-sometimes-but-not-always) · [Changes don't show](#i-dont-see-the-ais-change-on-my-site) · [Getting help](#still-stuck)

---

## The AI app can't reach my site

**Most common causes:**

- **The site isn't public.** AI apps run on the internet and can't reach a site on your own computer (`localhost`) or behind a company network. The plugin shows a warning if it detects this.
- **The address isn't HTTPS, or the certificate has a problem.** Open your site in a private browser window. The address should start with `https://` and show no security warning. If it does, renew the certificate in your hosting panel (usually under *SSL* or *Security*).
- **A firewall or security plugin is blocking the connection.** See [below](#a-firewall-or-security-plugin-is-blocking-the-connection).
- **The site is down or showing an error.** Fix the site first, then try again.

## Connected, but the AI sees no tools (or fewer than expected)

Check these in order:

1. **Do you have an agent, and is it turned on?** Open **AI Agents**. If you have no agent, create one. If you have one, make sure it's enabled.
2. **Does your role have tools ticked?** Edit the agent, find the column for *your* WordPress role (the role of the person who connected), and tick the tools to allow. Save.
3. **Did you just update the plugin?** New tools start **switched off**. Turn on the ones you want in **AI Agents**.
4. **Is the related plugin active?** WooCommerce, Yoast, Elementor and other tools only appear when that plugin is active.
5. **Refresh the connection.** Wait a minute, then disconnect and reconnect the connector in your AI app so it fetches a fresh list.

## It connects, but every request fails

It looks connected, but the AI is never recognised as signed in, or every request comes back as *unauthorized*.

**Use one public HTTPS address.** In **Settings → General**, make sure *WordPress Address* and *Site Address* are the **same `https://` address**, all with `www` or all without it.

**Your server may be removing the sign-in header.** This is common on some shared hosting. The Troubleshooting page tells you if this is the problem, and gives you the exact fix for your server.

### Technical fixes (for you or your host)

**Apache:** back up `.htaccess`, then add these lines at the very top, above `# BEGIN WordPress`:

```apache
RewriteEngine On
RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]
```

If that doesn't work, some hosts only accept this instead:

```apache
SetEnvIf Authorization "(.*)" HTTP_AUTHORIZATION=$1
```

**Nginx:** add this inside the site's PHP `location` block and reload Nginx. On managed hosting, send it to your host:

```nginx
fastcgi_param HTTP_AUTHORIZATION $http_authorization;
```

**HTTPS ends at a proxy or load balancer:** add this near the top of `wp-config.php`:

```php
if ( isset( $_SERVER['HTTP_X_FORWARDED_PROTO'] ) && 'https' === strtolower( $_SERVER['HTTP_X_FORWARDED_PROTO'] ) ) {
	$_SERVER['HTTPS'] = 'on';
}
```

**Redirects:** never redirect `/wp-json/` URLs (for example from non-www to www). The connection doesn't follow redirects there.

## A firewall or security plugin is blocking the connection

**Signs:** nothing works whichever way you connect, the connection starts but never finishes, or it works for some people and not others.

**What to do:** allow these addresses in your firewall, security plugin (such as Wordfence or Sucuri) or hosting panel:

```text
/wp-json/mosmcp/*
/index.php?rest_route=/mosmcp/*
```

### Cloudflare

Cloudflare may treat the AI connection as a bot. In Cloudflare, go to **Security → WAF → Custom rules**, create a rule, choose **Edit expression** and paste:

```text
(starts_with(http.request.uri.path, "/wp-json/mosmcp/v1/")) or (http.request.uri.query contains "rest_route=/mosmcp/")
```

Set the action to **Skip**, tick *Super Bot Fight Mode* (or *Bot Fight Mode*) and *Security Level*, save, and move the rule to the top. On Cloudflare's Free plan, you may need to turn Bot Fight Mode off instead.

### Other specific fixes

- **Wordfence:** open **Tools → Live Traffic**, find the blocked requests to `/wp-json/mosmcp/` and allowlist them.
- **"Disable REST API" options:** if a security plugin only lets logged-in users use the REST API, add `mosmcp/v1` to its allowlist.
- **Password-protected site** (a browser pop-up asks for a username and password before the site loads): AI apps can't answer that pop-up. Remove it, or exclude the paths above from it.
- **Gateway IP addresses:** the Troubleshooting page lists the exact miniOrange Gateway IP addresses to allow. Allowlist all of them in every firewall or CDN in front of your site.
- **Outgoing connections:** your server must be able to reach `gateway.miniorange.ai` over HTTPS.

## It works sometimes but not always

- **Caching.** A cache plugin or CDN may be serving a saved copy instead of a live answer. Exclude `/wp-json/mosmcp/` from caching and redirects, then purge the whole cache.
  - **LiteSpeed Cache:** **Cache → Excludes → Do Not Cache URIs** → add `/wp-json/mosmcp/`
  - **Cloudflare:** add a Cache Rule that bypasses the cache when the URI path starts with `/wp-json/mosmcp/`
- **Old DNS records.** If your domain points at more than one server and some aren't your site, connections fail at random. Remove the extra A/AAAA records in your domain settings.
- **Only some gateway addresses are allowed.** Allowlist all of them (see above).

## I don't see the AI's change on my site

The plugin clears page caches automatically after every change, for the most common cache plugins, hosts and CDNs.

- A **changed page** is cleared straight away.
- **Site-wide changes** (like a menu edit) can take **up to a minute** to show, because the full cache is cleared at most once a minute to keep busy sites fast.
- If you use a cache the plugin doesn't recognise, clear it from that cache's settings, or ask the AI: *"Clear the site caches."*

## The AI was disconnected

Remove the connector in your AI app and add it again to sign in fresh. If you **revoked** access in **AI Agents**, this is expected. Just connect again when you're ready.

---

## Still stuck?

1. In **Secure MCP Server → Troubleshooting**, click **Copy for support**. This copies a report with passwords and secrets removed.
2. Send it to us:
   - 💬 [WordPress.org support forum](https://wordpress.org/support/plugin/miniorange-secure-mcp-server/)
   - ✉️ **info@xecurify.com**
   - Or use the **Contact Support** button inside the plugin
