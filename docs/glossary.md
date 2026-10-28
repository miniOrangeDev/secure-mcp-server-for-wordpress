# Glossary

Plain-language meanings of the terms you'll see in the plugin and these guides.

| Term | What it means |
|---|---|
| **AI app / AI client** | The AI assistant you chat with, such as Claude, ChatGPT or Cursor. |
| **MCP (Model Context Protocol)** | An open standard that lets AI assistants use tools in other apps. Think of it as a universal plug between AI apps and software like WordPress. |
| **MCP server** | Software that offers tools to AI apps over MCP. This plugin turns your WordPress site into one. |
| **Connector** | What many AI apps call a connection to an MCP server. "Add a connector" means "connect a new MCP server". |
| **Tool / Ability** | One action the AI can take, such as "create a post" or "update a product price". WordPress calls these *abilities*, and AI apps call them *tools*. This plugin has 464. |
| **Agent** | A set of rules in the plugin that says which tools each WordPress role is allowed to use. You need at least one enabled agent before the AI can do anything. |
| **Agent Registry** | The **AI Agents** page in the plugin, where you create agents, set permissions and revoke access. |
| **Role** | A WordPress user role, such as Administrator, Editor, Author or Shop Manager. Permissions are set per role. |
| **miniOrange Gateway** | The connection point AI apps use to reach your site: `https://gateway.miniorange.ai/v2/mcp`. It passes requests along to your site and applies rate limits. |
| **Connection URL** | The address you paste into your AI app: `https://gateway.miniorange.ai/v2/mcp`. It's the same for everyone. |
| **OAuth 2.1 / PKCE** | The secure sign-in method used to connect. It works like "Sign in with Google": you log in on your own site and approve access, and the AI app never sees your password. |
| **Revoke** | Cut off an AI app's access immediately. |
| **Activity Log** | The record of every action an AI took (or tried to take) on your site. |
| **REST API** | The standard way WordPress and its plugins share data with other software. With *Governed REST API access*, the AI can use other plugins' REST APIs under your permissions. |
| **Page lock** | A safety check that stops the AI from overwriting a page that was changed after the AI last read it. |
| **Prompt injection** | A trick where text (for example in a comment or web page) tries to make an AI do something its user didn't ask for. The plugin watches for this. |
| **Human-in-the-loop approval** | A Business-plan feature where sensitive AI actions wait for a person to approve them. |
| **Data rules / DLP** | A Business-plan feature that hides sensitive data such as emails, phone numbers or secrets from the AI. |
| **localhost** | A website running only on your own computer. AI apps can't reach it, because it isn't on the internet. |
