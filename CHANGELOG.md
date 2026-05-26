# Changelog

All notable changes to Nova Agent Workflows should be recorded here.

## 0.3.0-draft - 2026-05-26

Nova Serious Workflow v1.8 public-safe governance update.

Added:

- context contract before meaningful edits
- Goal/Rider task framing for serious `T###` work
- structured risk approval pattern for risky actions
- runtime harness action flow: context -> allowed surfaces -> proposed action -> verdict -> execution -> evidence -> sync-back
- verdict vocabulary: `allow`, `warn`, `review`, `block`
- retry budget rule for repeated same-root-cause failures
- task-thread event shape for long-running, handoff-heavy, or multi-agent work
- agentic delivery chain: clarify/domain model -> PRD or compact spec -> vertical-slice issue plan -> optional TDD -> architecture review

Safety:

- no private memory export
- no runtime logs
- no private machine paths
- no hooks, MCP registration, installers, package scripts, account actions, deploys, or secret handling added
- no tagged release, package publication, deployment, force-push, remote rewrite, or repository setting change performed for v0.3.0-draft
- push to GitHub remains blocked until exact user approval after fresh scrub and smoke review

## 0.2.2-draft - 2026-05-21

Nova Serious Workflow v1.7 planner/orchestrator/review overlay.

Added:

- public-safe planner/orchestrator/review overlay for serious app, feature, GitHub, and PR work
- assumptions-first and simple-first guidance
- new-app planning pattern: concise project docs plus approved issue plan when useful
- existing-feature planning pattern: small dependency-ordered tasks or issues
- implementation delivery pattern: one approved issue -> one branch or PR -> checks -> review/fix -> user QA handoff
- outside-review pattern: question whether the change should exist, whether a simpler path exists, and whether the real code path supports the diff
- clarification pattern: ask one plain-language question when the goal is blurry
- board-finisher GitHub delivery guard for remote actions

Safety:

- no private memory export
- no runtime logs
- no private machine paths
- no archived skill code copied into the public pack
- no GitHub issue creation automation added
- no tagged release, package publication, deployment, force-push, or remote rewrite performed for v0.2.2-draft

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
