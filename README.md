# Andock plugins

Skills and plugin bundles for [Andock](https://andock.app). Andock connects any mailbox (GMX, WEB.DE,
Yahoo, iCloud, IONOS, Hostpoint, Bluewin and other web hosts) to Claude, ChatGPT and Notion AI, and
does the mail work: what came in, who is waiting for your reply, who hasn't answered you, drafts and
free slots. Drafts come first; sending needs your OK.

Andock is free. Sign up and connect your mailbox at [andock.app](https://andock.app) first.

## Claude

```
/plugin marketplace add amini-x/andock-plugins
/plugin install andock@andock
```

The plugin adds the Andock connector (`https://mcp.andock.app/mcp`) and these skills:
inbox-briefing, reply-zero, follow-up, find-and-answer, house-rules, onboarding, schedule-meeting,
contact-brief.

## ChatGPT

Download `andock-openai.zip` from the [latest release](https://github.com/amini-x/andock-plugins/releases/latest).

## Layout

| Path | What |
|---|---|
| `skills/` | The skills, shared by both bundles |
| `claude/` | Claude plugin: manifest, connector config, skills, icon |
| `openai/` | OpenAI plugin source |
| `.claude-plugin/marketplace.json` | Claude marketplace manifest |

Source of truth lives in the private Andock repo; this repo is a published copy.

## License

MIT, see [LICENSE](LICENSE). Support: info@andock.app
