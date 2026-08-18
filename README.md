# Tuist plugins for Claude Code

This marketplace packages Tuist agent skills and the hosted MCP server for [Claude Code](https://code.claude.com/). It lets Claude migrate to generated projects, debug generation, and inspect build, test, bundle, and cache data from the Tuist dashboard.

## Install

Add the marketplace and install the Tuist plugin:

```bash
claude plugin marketplace add tuist/claude-plugin
claude plugin install tuist@tuist-plugins
```

Most skills drive the Tuist command-line interface, so run `tuist auth login` once to grant access to your project's data. The bundled MCP server covers functionality that the command-line interface does not expose and prompts for sign-in from inside Claude Code.

## Layout

```text
.claude-plugin/marketplace.json  marketplace manifest
plugins/tuist/                    the Tuist plugin
```

## Skills come from tuist/tuist

`plugins/tuist/skills` mirrors [`skills/skills`](https://github.com/tuist/tuist/tree/main/skills/skills) in the Tuist monorepo, the same source that publishes [tuist/agent-skills](https://github.com/tuist/agent-skills). Edit skills there so every agent receives the change, not just Claude Code.

## License

MIT. See [LICENSE.md](LICENSE.md).
Tuist plugin marketplace for Claude Code
