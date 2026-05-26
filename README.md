# Nova Agent Workflows

Safe, evidence-first workflows for Codex, Claude Code, and long-running AI agents.

Status: public draft v0.3.0-draft prepared locally. Do not push, publish, or create a tagged release until the public scrub checklist, pre-publish release gate, and cross-agent smoke review pass in the same work session and the user approves the exact public action.

## What This Is

Nova Agent Workflows is a small set of reusable operating patterns for AI coding agents. It helps an agent:

- keep task boards and checklists clear;
- preserve existing work before cleanup;
- verify before claiming completion;
- stop before risky actions;
- hand off work concisely;
- show a visible six-layer mini-plan for serious work;
- use a compact context contract before meaningful edits;
- frame serious tasks with Goal and Rider instead of vague prompts;
- borrow planner/orchestrator/review patterns without granting automatic GitHub permissions;
- classify meaningful actions with allow/warn/review/block verdicts;
- stop after repeated same-root-cause failures instead of looping;
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
version: 0.3.0-draft
date: 2026-05-26
scope: Nova Serious Workflow v1.8 context contract, Goal/Rider task framing, structured risk approval, error budget, task-thread events, runtime harness verdicts, agentic delivery chain, Codex adapter, Claude Code adapter, planning templates, synthetic examples
```

Nova Serious Workflow v1.8 uses this layer map:

1. Obsidian Brain Layer
2. Planning / Spec Layer
3. GitHub Delivery Layer
4. Verification / Risk Gate Layer
5. Release / Publish Layer
6. Sync Back / Learning Layer

v1.8 adds a public-safe execution layer:

- state a compact context contract before meaningful edits;
- write serious tasks with Goal, Rider, done condition, verification, stop rule, and recommended intelligence;
- plan new apps or features as small, reviewable specs and issue plans;
- implement one approved issue at a time on a branch or PR;
- review from the outside before accepting the change;
- ask one plain-language question when the goal is blurry;
- classify meaningful actions as `allow`, `warn`, `review`, or `block`;
- use a retry budget for repeated same-root-cause failures;
- record compact task-thread events for long-running or multi-agent work;
- keep every GitHub or publish action behind explicit user approval.

## Safety

Before public release, run through:

- `safety/PUBLIC_EXPORT_SCRUB_CHECKLIST.md`
- `safety/PRE_PUBLISH_RELEASE_GATE.md`
- `safety/RISK_GATES.md`
- cross-agent smoke review for Codex, Claude Code, and generic coding-agent usage

Release only when examples are synthetic, local paths are removed, no secrets are present, and risky actions are written as stop rules rather than permissions.

## Release Readiness

See `RELEASE_READINESS.md`.

This draft may be used locally for review. Future pushes, tagged releases, force-pushes, or repository/account setting changes require explicit approval for the exact action.
