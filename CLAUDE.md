# CLAUDE.md

Training materials, demos and infrastructure for Advanced Angular Development. It is a **teaching repository**, not a production application, designed to demonstrate Angular concepts through hands-on examples.

Author with the global `create-class` skill, build slides with the global `create-pptx` skill, and run the `brand-voice-code` skill after writing or editing a readme or guide.

## Layout

```text
demos/readme.md                      class readme: Duration, Audience, Prerequisites, Modules, Schedule
demos/NN-<module>/readme.md          module teaching overview
demos/NN-<module>/<app>/             the module's Angular demo app: db.json, public/markdown/, src/app/demos/
demos/NN-<module>/pptx/              slide specs NN-MM-<slug>.md, images/, topics.json, NN-<module>.pptx
demos/pptx/                          00 class deck, modules.json, days.json, images/
labs/readme.md                       lab index: module, Angular focus, what gets built
labs/lab-NN/                         readme.md, lNN-secrets-vault-starter/, lNN-secrets-vault-solution/
labs/secrets-vault-mcp/              the given Secrets and Document Vault API
db/secrets-vault-mcp/                its schema, data and delta scripts
design-system/                       the workbench design tokens
setup/                               prerequisites and install
tasks/                               lessons.md, todo.md for a running plan
```

Module and lab numbers are two-digit and gapless, in teaching order: 13 modules from `demos/01-agentic-dev` to `demos/13-oauth`, 12 labs from `labs/lab-01` to `labs/lab-12`.

## Brand Voice

Every `readme.md` and guide under `demos/` and `labs/` follows `.claude/skills/brand-voice-code/references/rules.md`. Check a file against it after writing or significantly editing it.

## Where the detail lives

| Topic | Lives in |
| --- | --- |
| Angular deviations from `angular-conventions`, demo app structure | `.claude/rules/angular.md` |
| Secrets and Document Vault lab workbench | `.claude/rules/lab-workbench.md` |

## Harness

Orchestration runs in the integrations-marketplace mods (`D:\git-projects\integrations-marketplace`), and the house rules in `~/.claude/CLAUDE.md` apply as they stand; this file repeats neither.

- `subagent-delegation-plugin`: routes work to the owning agent (owners in `.claude/rules/`), sends fact gathering to the Haiku fact-gatherer, bounds every brief, keeps the agent ledger.
- `learn-loop-plugin`: runs `claude-learn` once a session goes idle.
- `report-plugin`: starts a status cron when an agent or workflow runs long.
- `intent-guard-plugin`: holds destructive commands nobody asked for.
- `ask-check-plugin`: stops questions the conversation already settled and unrequested findings.
- `write-gate-plugin`: holds a writer's finish until the humanize and marketing-psychology passes ran.
- `harness-plugin`: guards this file's shape, halts a run on `AGENT_STOP`, redirects it with `STEER.md`; `fix-constitution` realigns the repo.

## Hard Rules

- Never edit anything under `labs/secrets-vault-mcp/` or `db/secrets-vault-mcp/`: the backend is given.
- Write clean code. No comments. Do not over-engineer.
- Docs, when asked for, are concise and to the point.

## Working Method

- **Plan first** for anything non-trivial (3+ steps or an architectural decision): write it to `tasks/todo.md`, check in, then track progress there.
- **Verify before reporting done.** Run the check, show the command and its output. A claim is not a receipt.
- **Review `tasks/lessons.md`** at session start; `claude-learn`'s `instruction-audit` gate prunes it and this file.
- **Simplicity first**: minimal diff, root causes over patches, no rewrite to fix a typo.
