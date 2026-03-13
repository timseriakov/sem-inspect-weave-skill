# sem-inspect-weave-skill

Portable Agent Skill that teaches a semantic version control workflow:

sem -> inspect -> weave

Roles:
- sem: structural truth (entity-level diff/graph/impact)
- inspect: review prioritization (risk/blast radius/dependents)
- weave: coordination + merge semantics

This repository contains a single skill directory:

- `sem-inspect-weave/`

## Prerequisites

- `sem` CLI
- `inspect` CLI
- `weave` CLI
- Optional: `gh` (required for `inspect pr`)

## Install

Agent-skill hosts (OpenCode, Codex CLI, Gemini CLI, etc.) typically discover skills under:

- `~/.agents/skills/<skill-name>/SKILL.md`

Since this repo name is not the same as the skill name, install by copying the skill folder:

```bash
git clone https://github.com/timseriakov/sem-inspect-weave-skill.git /tmp/sem-inspect-weave-skill
rm -rf ~/.agents/skills/sem-inspect-weave
cp -R /tmp/sem-inspect-weave-skill/sem-inspect-weave ~/.agents/skills/sem-inspect-weave
```

Verify:

```bash
test -f ~/.agents/skills/sem-inspect-weave/SKILL.md && echo "ok"
```

## Usage

Read `sem-inspect-weave/SKILL.md` for the reasoning model, trigger phrases, and typical workflows.

Helper scripts are available under:

- `sem-inspect-weave/scripts/skill-preflight`
- `sem-inspect-weave/scripts/sem-json`
- `sem-inspect-weave/scripts/inspect-review-target`
- `sem-inspect-weave/scripts/weave-preview-safe`

Safety note:
- never run `weave setup` unless explicitly requested (it mutates repo merge-driver configuration)

## License

MIT
