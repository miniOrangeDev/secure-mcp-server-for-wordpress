# Security and control

Letting an AI work on a live website is a big step. This plugin is built so that **the AI can only do what you've allowed, everything it does is recorded, and mistakes can be undone.**

---

## Three checks on every action

Every time the AI tries to do something, it has to pass three checks:

```text
  AI asks to do something
          │
          ▼
  ① Is this a real, approved WordPress user?   ── no ──▶ refused
          │ yes
          ▼
  ② Is this tool allowed for their role?       ── no ──▶ refused
          │ yes
          ▼
  ③ Could this user do it in wp-admin?         ── no ──▶ refused
          │ yes
          ▼
       Done, and logged
```

1. **The connection belongs to a real WordPress user.** When you connect an AI app, you log in to *your own* WordPress site and click *Allow access*. The app gets a secure pass that only works for that user, on that site. Passes that have expired, been revoked or belong to another site are refused.
2. **Role-based permissions.** In the **Agent Registry** you decide which tools each WordPress role can use. Tools a role isn't allowed are hidden from the AI and can't be used.
3. **WordPress's own permission checks.** Each action is checked exactly as if the user did it by hand in wp-admin, down to the individual post, page or comment. **The AI can never do more than the person who connected it.**

## The AI never sees your password

Sign-in uses **OAuth 2.1 with PKCE**, the same kind of secure sign-in behind "Sign in with Google". You type your password on your own WordPress login page, never in the AI app. You can revoke access at any time.

## You decide what the AI can do

- **Agent Registry:** create named agents and, for each WordPress role, tick exactly which tools are allowed. Everything is shown in one grid.
- **On/off switch for every tool:** turn any tool off for the whole site from the **Abilities** page.
- **Pause an agent** without losing its settings.
- **Revoke access instantly:** click **Revoke** and the AI app is cut off straight away.
- **New tools start switched off** when you update the plugin, so nothing new is allowed without your say-so.

**For example:** an Editor's AI can write and publish content but can't install plugins, and a Shop Manager's AI can update orders but can't change site settings.

## Mistakes are hard to make and easy to undo

- **Destructive actions need confirmation.** Every tool tells the AI whether it only reads or makes changes, and deleting things needs an extra confirmation.
- **Page lock.** If a page was changed after the AI read it (for example, a colleague edited it), the AI's edit is refused rather than overwriting their work.
- **Revisions.** Content changes save a revision, so you can roll any post back.
- **Safe theme editing.** Theme changes never go straight to your live site:
  - They go into a private **draft**.
  - Code is **checked for errors** before it's accepted.
  - You can **preview** the draft, and the site is tested before it goes live.
  - Publishing takes an **automatic backup**. If the site fails, **everything rolls back automatically**.
  - You can undo any publish later with one click.
- **Block-by-block editing.** The AI can change a single heading or button and leave the rest of the page exactly as it was.

## Everything is recorded

The **Activity Log** records every action, allowed or refused: who connected, which AI app, which tool, the result and the time. You can filter by agent, status, tool, user and date.

The **Dashboard** shows active agents, number of actions, success rate and response time at a glance.

## Protection against misuse

- **Prompt-injection detection:** watches for content that tries to trick the AI into doing something you didn't ask for.
- **Unusual-behaviour detection:** flags activity that doesn't look normal.
- **Rate limits:** stop any one AI app from making too many requests (enforced by the miniOrange Gateway).
- **Dangerous routes are always blocked:** plugin and theme installs and activations can never be granted through the REST API.

## Business plan extras

- **Human approval:** sensitive actions wait for a person to approve them before they happen.
- **Data rules:** automatically hide emails, phone numbers, secrets and other sensitive data from the AI. You define the rules.

[See plans and pricing](https://plugins.miniorange.com/mcp-server-ai-policy-enforcement-wordpress#pricing)

## Where does my data go?

The tools run, and every permission is checked, **on your own WordPress site**. Your AI app connects through the **miniOrange Gateway** (`gateway.miniorange.ai`). The gateway passes the AI's requests along to your site and applies rate limits. Sign-in happens on your own WordPress site, and your password is never shared with the AI app.

## Reporting a security issue

Please see [SECURITY.md](../SECURITY.md).
