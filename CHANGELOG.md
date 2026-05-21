# Changelog

All notable changes to Nova Agent Workflows should be recorded here.

## 0.2.1-draft - 2026-05-21

Nova Serious Workflow v1.6 mini-plan alignment.

Updated:

- required a visible six-layer mini-plan before serious `T###` work
- aligned the six layers to:
  - Obsidian Brain Layer
  - Planning / Spec Layer
  - GitHub Delivery Layer
  - Verification / Risk Gate Layer
  - Release / Publish Layer
  - Sync Back / Learning Layer
- clarified that unused layers should be marked `N/A` instead of inventing GitHub, release, or spec work
- added a legacy project alignment rule: do not rewrite old completed tasks just to retrofit the new format
- updated Codex, Claude Code, board-finisher, and project guidance wording

Safety:

- no private memory export
- no runtime logs
- no private machine paths
- no tagged release, package publication, deployment, force-push, or remote rewrite performed for v0.2.1-draft

## 0.2.0-draft - 2026-05-20

Nova Serious Workflow v1.5 alignment.

Added:

- six-layer serious workflow stack:
  - Brain / context layer
  - Ingestion / knowledge layer
  - Planning / spec layer
  - Task board / checklist layer
  - Verification / risk gate layer
  - Delivery / sync-back layer
- planning templates:
  - `templates/PRD.md`
  - `templates/SPEC.md`
  - `templates/ARCHITECTURE.md`
  - `templates/AGENTS.md`
- Codex and Claude Code adapter wording for the six-layer workflow
- release-readiness update for the existing public repository state

Safety:

- no private memory export
- no runtime logs
- no private machine paths
- v0.2.0-draft was pushed to `main` after local scrub
- no tagged release, package publication, deployment, or remote rewrite performed for v0.2.0-draft
- release gate remains required before any tagged release or future risky public action

## 0.1.0-draft - 2026-05-20

Initial local draft.

Added:

- core workflow: `nova-serious-workflow`
- core workflow: `nova-debug-review-gate`
- core workflow: `nova-board-finisher`
- Codex skill adapters
- Claude Code skill adapters
- `CLAUDE.md.example`
- task board, checklist, work log, and handoff templates
- synthetic game-project and Obsidian-brain examples
- public export scrub checklist
- risk gates
- versioning policy

Safety:

- no private memory export
- no runtime logs
- no account, deploy, payment, secret, browser-account, or OS repair automation
- no hooks that run by default
- no public repository created
- no publish or push performed

Smoke review update:

- clarified all Codex and Claude Code adapter skills so they can operate safely even when copied without the full `workflows/` folder
- added T048 scrub report

Version routine update:

- added Nova alignment rule to `VERSIONING.md`
- added stable private routine note reference for future workflow-pack upgrades
- updated Nova Brain Evolution Dashboard privately as Ver 1.4*

Permanent release gate update:

- added `safety/PRE_PUBLISH_RELEASE_GATE.md`
- added `RELEASE_READINESS.md`
- added `.gitignore`
- made fresh scrub plus cross-agent smoke review mandatory before any public release
- clarified that GitHub repository creation, remote setup, push, publish, and release require explicit approval for the exact action
- added `safety/PUBLIC_EXPORT_SCRUB_REPORT_T051.md`

Release prep update:

- finalized MIT license copyright as `2026 Nova Agent Workflows`
- release remains gated on final scrub, local commit, GitHub repository creation, and push verification
- added `safety/PUBLIC_EXPORT_SCRUB_REPORT_T052.md`
