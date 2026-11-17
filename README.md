# Andock plugins

Skills and plugin bundles for [Andock](https://andock.app). Andock connects any mailbox (GMX, WEB.DE,
Yahoo, iCloud, IONOS, Hostpoint, Bluewin and other web hosts) to Claude, ChatGPT and Notion AI, and
does the mail work: what came in, who is waiting for your reply, who hasn't answered you, drafts and
free slots. Drafts come first; sending needs your OK.

Andock is free. Sign up and connect your mailbox at [andock.app](https://andock.app) first.

## Claude

On claude.ai or in the Claude app (paid plans): open **Customize**, then **Plugins**, click **Add**, then
**Add marketplace** and **Add from a repository**. Enter `amini-x/andock-plugins` and add the Andock plugin.

In Claude Code:

```
/plugin marketplace add amini-x/andock-plugins
/plugin install andock@andock
```

The plugin adds the Andock connector (`https://mcp.andock.app/mcp`) and these skills: inbox-briefing,
reply-zero, reply-to-email, write-email, follow-up, find-and-answer, summarize-thread,
bills-and-deadlines, suspicious-mail-check, inbox-cleanup, promise-tracker, schedule-meeting,
contact-brief, onboarding, house-rules. In a chat, type "/" to pick one, or just ask.

## ChatGPT

Download `andock-openai.zip` from the [latest release](https://github.com/amini-x/andock-plugins/releases/latest).

## Cursor

This repo is a Cursor plugin marketplace (`.cursor-plugin/`). Add `amini-x/andock-plugins` as a plugin source
in Cursor and install Andock. It brings the same skills and the connector.

## Grok Build and GitHub Copilot

Both read Claude plugins. Add `amini-x/andock-plugins` as a plugin marketplace and install `andock`.

## Notion AI, Perplexity and Manus

1. Add the connector `https://mcp.andock.app/mcp` as a custom MCP server and sign in. In Notion this needs a
   Business or Enterprise plan, and an admin must allow custom MCP servers first.
2. Download `andock-single-skills.zip` from the [latest release](https://github.com/amini-x/andock-plugins/releases/latest)
   and unzip it. It holds one ZIP per skill.
3. Upload the skills you want. In Notion: Library, then Skills, then "More ways to add a skill", then "Upload skill".

## Meta Muse

In Muse, open Settings, then Connectors, then "Add custom connector", and paste `https://mcp.andock.app/mcp`.
Muse can't install outside skills yet; the connector tells Muse how to do each mail job.

For Muse Code, unzip `andock-skills.zip` into `~/.agents/skills/` and add the connector to
`~/.config/muse/settings.json`:

```json
{ "mcpServers": { "andock": { "url": "https://mcp.andock.app/mcp" } } }
```

## Other agents

Windsurf, opencode, Amp, Goose and Codex read skill folders. Unzip `andock-skills.zip` into the agent's skills
folder (for example `~/.agents/skills/`) and add `https://mcp.andock.app/mcp` as a remote MCP server.

## Layout

| Path | What |
|---|---|
| `skills/` | The skills, shared by both bundles |
| `claude/` | Claude plugin: manifest, connector config, skills, icon |
| `openai/` | OpenAI plugin source |
| `.claude-plugin/marketplace.json` | Claude marketplace manifest |
| `.cursor-plugin/marketplace.json` | Cursor marketplace manifest |

Source of truth lives in the private Andock repo; this repo is a published copy.

## License

MIT, see [LICENSE](LICENSE). Support: info@andock.app
