# Foxli MCP

Connect your AI assistant to [Foxli](https://foxli.app), the social media scheduling and analytics tool. Plan, draft, schedule and publish posts to Instagram, Facebook, LinkedIn, X, Threads, YouTube and Pinterest, and read analytics, without leaving the chat.

This repository only contains client configuration (a Cursor plugin and a Gemini CLI extension) for Foxli's **hosted remote MCP server**. The server itself is a hosted service run by Foxli.

- **Server URL:** `https://mcp.foxli.app/mcp` (Streamable HTTP)
- **Auth:** OAuth 2.1 with PKCE and Dynamic Client Registration. You sign in with your Foxli account; no API key needed.
- **Requires:** a Foxli Creator or Team plan.
- **Docs:** https://foxli.app/developers/mcp
- **Official MCP Registry:** `app.foxli/foxli`

## Install

**Cursor:** install the Foxli plugin, or add this to `~/.cursor/mcp.json`:

```json
{
  "mcpServers": {
    "foxli": { "url": "https://mcp.foxli.app/mcp" }
  }
}
```

**Gemini CLI:**

```bash
gemini extensions install https://github.com/srpushpendar/foxli-mcp
```

**Claude, ChatGPT, VS Code and other MCP clients:** add a remote MCP server / custom connector with the URL `https://mcp.foxli.app/mcp` and sign in with Foxli.

## What it can do

- See your workspaces and connected channels.
- Check each platform's rules (character and media limits) before writing a post.
- Create posts as drafts, add them to your queue, or schedule them.
- Edit drafts and scheduled posts, import an image or video from a URL, and delete posts.
- Publish a draft right away, only after you confirm.
- Send a post for approval in team and client workspaces.
- Read your posts and an analytics overview for a date range.

The assistant always creates a draft first and shows you the text, channels and media. Nothing is published or scheduled until you say so.

## Example prompts

1. "What workspaces and channels do I have in Foxli?"
2. "Write a short LinkedIn post about our weekend sale and save it as a draft."
3. "Schedule that draft for tomorrow at 10 am."
4. "How did my posts do in the last 30 days? Which one did best?"
5. "Plan 5 posts for next week and add them to my queue."

## Privacy and support

- Privacy policy: https://foxli.app/privacy (section "AI Assistants & MCP Connections")
- Terms: https://foxli.app/terms
- Support: support@foxli.app · https://foxli.app/contact-us

Foxli never shares your social media passwords or tokens with the AI assistant. You can disconnect at any time from Foxli (Settings → Connected apps) or from your AI client.
