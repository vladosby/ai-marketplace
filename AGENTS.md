# ai-marketplace — Agent Guide

Personal marketplace of agent plugins. Each plugin lives in `plugins/<name>/` and must stay
**harness-agnostic at its core**: skills follow the open Agent Skills format (`SKILL.md` with `name` and
`description` frontmatter, optional `references/`) and describe browser/tool *capabilities*, not
vendor-specific tool names. Claude Code packaging (`.claude-plugin/`, `.mcp.json`) is a thin wrapper.

Rules:
1. Register every plugin in `.claude-plugin/marketplace.json`.
2. Bump `version` in the plugin's `plugin.json` when its behaviour changes.
3. Pin MCP package versions in `.mcp.json`.
4. Never commit browser profiles, cookies, tokens or exported personal data.
5. Work on a feature branch; `main` is protected by CI and is what users install from.
