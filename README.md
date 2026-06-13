# krossto-plugins

A Claude Code plugin marketplace by krossto.

## Plugins

| Plugin | Description |
|---|---|
| [codex-design-review](https://github.com/krossto/codex-design-review) | Cross-model review of design documents by OpenAI Codex CLI. Built for the Superpowers spec/plan workflow. |
| [rcd](https://github.com/krossto/rcd) | Lifecycle management for per-project Claude Code remote-control systemd instances. |

## Install

```
/plugin marketplace add krossto/claude-plugins
/plugin install codex-design-review@krossto-plugins
/plugin install rcd@krossto-plugins
```

## Update

Plugins track each repo's default branch (SHA-driven), so any push is a new version.

```
/plugin marketplace update krossto-plugins
/plugin update codex-design-review@krossto-plugins
/plugin update rcd@krossto-plugins
```

## Adding a plugin

Append an entry to `.claude-plugin/marketplace.json`:

```json
{
  "name": "<plugin-name>",
  "source": { "source": "github", "repo": "krossto/<repo>" },
  "description": "<one line>",
  "author": { "name": "krossto" },
  "homepage": "https://github.com/krossto/<repo>",
  "repository": "https://github.com/krossto/<repo>",
  "category": "<category>"
}
```

Omit `version`/`ref`/`sha` to keep SHA-driven tracking. Then run `claude plugin validate .`.

## License

MIT — see [LICENSE](LICENSE).
