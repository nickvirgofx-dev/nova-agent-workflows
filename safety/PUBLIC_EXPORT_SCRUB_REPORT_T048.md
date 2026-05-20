# Public Export Scrub Report - T048

Date: 2026-05-20
Status: local draft smoke review passed with release blockers still open.

## Scope

Checked only the local draft under:

```text
<RUNTIME_ROOT>/public_exports/nova-agent-workflows
```

No publish, push, GitHub repository creation, remote setup, deployment, account action, authentication, payment action, secret handling, browser-account action, hook install, plugin install, or OS repair was performed.

## Required File Check

All expected v0.1 draft files were present:

```text
README.md
VERSIONING.md
CHANGELOG.md
LICENSE
workflows/nova-serious-workflow.md
workflows/nova-debug-review-gate.md
workflows/nova-board-finisher.md
adapters/codex/skills/nova-serious-workflow/SKILL.md
adapters/codex/skills/nova-debug-review-gate/SKILL.md
adapters/codex/skills/nova-board-finisher/SKILL.md
adapters/claude-code/CLAUDE.md.example
adapters/claude-code/skills/nova-serious-workflow/SKILL.md
adapters/claude-code/skills/nova-debug-review-gate/SKILL.md
adapters/claude-code/skills/nova-board-finisher/SKILL.md
templates/TASK_BOARD.md
templates/TASK_CHECKLIST.md
templates/WORK_LOG.md
templates/HANDOFF.md
examples/game-project-example.md
examples/obsidian-brain-example.md
safety/PUBLIC_EXPORT_SCRUB_CHECKLIST.md
safety/RISK_GATES.md
safety/PUBLIC_EXPORT_SCRUB_REPORT_T047.md
```

## Scrub Checks

Private path scan:

```text
command pattern: local drive paths, home-directory paths, private vault names, private runtime names
result: no file-content matches
```

Credential-shaped scan:

```text
patterns: sk-..., ghp_..., xox..., AKIA..., AIza...
result: no matches
```

Trailing whitespace scan:

```text
result: no matches
```

Adapter validation:

```text
Codex nova-serious-workflow: pass
Codex nova-debug-review-gate: pass
Codex nova-board-finisher: pass
Claude Code nova-serious-workflow: pass
Claude Code nova-debug-review-gate: pass
Claude Code nova-board-finisher: pass
```

## Cross-Agent Smoke Review

Codex path:

```text
README points to adapters/codex/skills/.
All 3 Codex SKILL.md files have valid frontmatter.
All 3 Codex SKILL.md files now say the skill can operate safely even when copied without the full workflows folder.
```

Claude Code path:

```text
README points to adapters/claude-code/skills/.
CLAUDE.md.example exists and clearly states that user instruction, real files, tests, and runtime evidence outrank stored workflow notes.
All 3 Claude Code SKILL.md files have valid frontmatter.
All 3 Claude Code SKILL.md files now say the skill can operate safely even when copied without the full workflows folder.
```

Templates:

```text
TASK_BOARD.md and TASK_CHECKLIST.md contain explicit T-number checkbox structure.
WORK_LOG.md stays compact.
HANDOFF.md includes completed, verification, not tested, risks, and next sections.
```

Versioning:

```text
VERSIONING.md defines semantic versioning and future upgrade tracks.
CHANGELOG.md records 0.1.0-draft and the T048 smoke-review clarification.
```

## Issues Found And Fixed

Issue:

```text
Adapter skills referenced workflows/... as canonical guidance. If users copied only a skill folder, that path might not exist.
```

Fix:

```text
Updated all 6 adapter SKILL.md files to say: if the full pack is available, use workflows/...; if the skill folder was copied alone, the compact rules below are sufficient to operate safely.
```

## Release Blockers

Still blocked before public release:

- replace the license author/year placeholder in `LICENSE` before release;
- choose final license and author/org identity;
- perform a fresh scrub after any final edits;
- run a clean check in the export folder;
- get explicit user approval before any GitHub repository creation, push, publish, or remote setup.
