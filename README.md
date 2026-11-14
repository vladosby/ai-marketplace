# ai-marketplace

Personal marketplace of agent plugins.

## Plugins

### linkedin-profile
Skill + [Playwright MCP](https://github.com/microsoft/playwright-mcp) to read your full LinkedIn profile,
edit its sections and create, read, edit and delete posts through a browser. Every save/publish needs your approval.

> **Risk notice.** Automating LinkedIn is against its terms of service and can get an account restricted.
> Use it only on your own account, at low volume, and only when you ask for it.

#### Install in Claude Code
```
/plugin marketplace add vladosby/ai-marketplace
/plugin install linkedin-profile@vladosby-ai
```
The first run opens a browser; sign in to LinkedIn once. The session is kept in
`~/.linkedin-playwright` (never commit or share it).

#### Other agent harnesses
The skill is plain Agent Skills format, so any tool that reads `SKILL.md` can use it:
1. Copy `plugins/linkedin-profile/skills/linkedin-profile/` into that tool's skills directory
   (check the tool's docs for the location).
2. Add a Playwright MCP server to its MCP config:
```json
{ "mcpServers": { "playwright": {
    "command": "npx",
    "args": ["@playwright/mcp@0.0.85", "--user-data-dir=/home/you/.linkedin-playwright"] } } }
```
Any browser tool that can open pages, read them, click and type works in place of Playwright MCP.

## Contributing
See `AGENTS.md`. Work on a feature branch and open a PR into `main`.

## License
MIT
