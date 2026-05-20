# Nova Agent Workflows

Safe, evidence-first workflows for Codex, Claude Code, and long-running AI agents.

Status: public draft v0.2.0-draft on `main`. Do not publish a tagged release until the public scrub checklist, pre-publish release gate, and cross-agent smoke review pass in the same work session.

## What This Is

Nova Agent Workflows is a small set of reusable operating patterns for AI coding agents. It helps an agent:

- keep task boards and checklists clear;
- preserve existing work before cleanup;
- verify before claiming completion;
- stop before risky actions;
- hand off work concisely;
- use a six-layer serious-work stack for larger projects;
- continue work across Codex, Claude Code, or similar tools.

## What This Is Not

This pack does not include a private memory vault, runtime logs, account automation, deployment automation, OS repair, browser-account actions, or hidden hooks.

It is guidance for safer agent work. It is not permission for an agent to delete files, deploy software, authenticate accounts, handle payments, use secrets, or run broad automation.

## Workflows

- `workflows/nova-serious-workflow.md`
- `workflows/nova-debug-review-gate.md`
- `workflows/nova-board-finisher.md`

## Adapters

Codex:

- Copy the relevant folder from `adapters/codex/skills/` into your Codex skills directory.
- Restart or reload Codex if your environment requires skill discovery refresh.

Claude Code:

- Copy the relevant folder from `adapters/claude-code/skills/` into your Claude Code skills area.
- Optionally adapt `adapters/claude-code/CLAUDE.md.example` into your project root guidance.

## Templates

Start a governed project with:

- `templates/TASK_BOARD.md`
- `templates/TASK_CHECKLIST.md`
- `templates/PRD.md`
- `templates/SPEC.md`
- `templates/ARCHITECTURE.md`
- `templates/AGENTS.md`
- `templates/WORK_LOG.md`
- `templates/HANDOFF.md`

Use placeholders such as `<PROJECT_ROOT>`, `<VAULT_ROOT>`, `<RUNTIME_ROOT>`, `<TASK_BOARD>`, `<TASK_CHECKLIST>`, and `<WORK_LOG>`.

## Versioning

This project is designed to evolve. See `VERSIONING.md`.

Current draft:

```text
version: 0.2.0-draft
date: 2026-05-20
scope: Nova Serious Workflow v1.5 six-layer stack, Codex adapter, Claude Code adapter, planning templates, synthetic examples
```

## Safety

Before public release, run through:

- `safety/PUBLIC_EXPORT_SCRUB_CHECKLIST.md`
- `safety/PRE_PUBLISH_RELEASE_GATE.md`
- `safety/RISK_GATES.md`
- cross-agent smoke review for Codex, Claude Code, and generic coding-agent usage

Release only when examples are synthetic, local paths are removed, no secrets are present, and risky actions are written as stop rules rather than permissions.

## Release Readiness

See `RELEASE_READINESS.md`.

This draft may be used from the public `main` branch for review. Future pushes, tagged releases, force-pushes, or repository/account setting changes require explicit approval for the exact action.
