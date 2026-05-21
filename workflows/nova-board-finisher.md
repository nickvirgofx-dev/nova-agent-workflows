# Nova Board Finisher

Use this workflow when the user asks an agent to continue through a task board or checklist until no safe actionable task remains.

This is not permission to bypass risk gates.

## Entry

1. Identify the canonical board and checklist.
2. Read current state, board, checklist, decision log, and handoff if present.
3. Build a short queue from open tasks only.
4. Skip complete, withdrawn, archived, or blocked tasks.
5. Announce the first slice with the required Nova Serious Workflow mini-plan and stop rules.

## Required Mini-Plan

Before editing files, running implementation, or marking a task complete, show:

```text
Nova Serious Workflow mini-plan
1. Obsidian Brain Layer: read/update <exact files>
2. Planning / Spec Layer: <PRD/SPEC/ARCHITECTURE/AGENTS/acceptance criteria or N/A because ...>
3. GitHub Delivery Layer: <issues/branch/PR/review/merge or N/A because local-only ...>
4. Verification / Risk Gate Layer: <tests/smoke/Sentinel/scrub/audit/security/stop rules>
5. Release / Publish Layer: <changelog/version/release notes/public-private/rollback or N/A because not publishing ...>
6. Sync Back / Learning Layer: <result/decision/lesson/bug/next/status files>
Recommended intelligence: <low|medium|high|xhigh>
Stop rules: <exact risky actions that will pause>
```

If a layer is not used, mark it `N/A` with a short reason. Do not create specs, GitHub issues, PRs, releases, or publishing work just to fill the template.

## Task Selection

Priority:

1. user-named task IDs or task range;
2. board's explicit next task;
3. lowest-numbered safe pending task;
4. cleanup/audit tasks after active project work.

Do not create a new task ID unless new work appears.

## Legacy Project Alignment

Do not reopen or rewrite old completed tasks just to retrofit the six-layer format.

- Treat completed tasks as valid if they have a clear result, project-state/work-log evidence, and verification.
- Apply the six-layer mini-plan from the next new task onward.
- Create a one-time alignment pass only when an old important project is active again or missing structure blocks safe continuation.
- Alignment must be preserve-first, small, and gap-filling only.

## Completion Loop

For each safe task:

1. read task-local context;
2. confirm allowed files and systems;
3. implement or document the smallest complete slice;
4. run task-specific verification;
5. update checklist, board, current state, and handoff;
6. continue only if verification passed and no risk gate is hit.

## Stop Conditions

Stop and report `blocked` when:

- explicit approval is required;
- credentials, external accounts, API keys, payment, auth, or production deploy are needed;
- OS repair, registry, service, driver, boot, disk, or whole-machine cleanup is requested;
- hard delete or broad stable-memory rewrite is required;
- verification fails twice with the same root cause;
- task truth is ambiguous or conflicting;
- no safe pending tasks remain.

## Final Report

```text
completed:
blocked:
not tested:
files changed:
verification:
next safe task:
```
