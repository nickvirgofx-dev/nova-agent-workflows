# Nova Serious Workflow

Use this workflow when an agent starts or continues serious work that needs context, tasks, verification, safe delivery, and sync-back.

## Core Rule

Current user instruction, real files, tests, and runtime evidence outrank stored memory.

Stored notes are orientation, not final truth.

## Nova Serious Workflow v1.7: Six-Layer Stack

Use the user-approved six-layer stack for serious work. Small safe tasks may mark irrelevant layers as `N/A`, but meaningful work should still sync back to project notes.

## Planner / Orchestrator / Review Overlay

Use this overlay when serious work involves new apps, feature planning, GitHub delivery, PR review, or unclear goals. It borrows public-safe patterns from planner, feature-planner, implementation-orchestrator, review, and clarification workflows without granting extra permissions.

Adopted patterns:

- Assumptions first: name what you know, what you do not know, and what evidence will settle it.
- Simple first: choose the smallest design that can satisfy the goal and acceptance criteria.
- New app planning: create concise `README.md`, `PRD.md`, `SPEC.md`, `ARCHITECTURE.md`, `AGENTS.md`, and an issue plan only when they help the work.
- Existing feature planning: split one feature into small dependency-ordered tasks or issues.
- Implementation orchestration: one approved issue becomes one focused branch or PR, followed by checks, review/fix, and user QA handoff.
- Outside review: ask whether the change should exist, whether there is a simpler path, and whether the real code path supports the diff.
- Clarification: if the plan is blurry, ask one plain-language question at a time and include the recommended answer.

Hard gates:

- Do not create GitHub issues until the user approves the issue plan.
- Do not push, force-push, open PRs, mark PRs ready, merge, publish, deploy, or change repository settings without explicit approval for that exact action.
- Do not implement vague issues. Clarify goal, non-goals, acceptance criteria, validation, and manual QA first.
- Do not rely on chat memory for repo work. Re-read repo docs, the current issue, linked dependency issues, and relevant previous PRs when available.
- If a referenced helper workflow is unavailable, use the available docs and ask the smallest useful clarification instead of inventing hidden automation.

### Required Mini-Plan

Before editing files, running implementation, or marking a serious task complete, show a compact six-layer map:

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

Rules:

- If a layer is not used, say `N/A` and explain why in a short phrase.
- Do not invent specs, GitHub issues, PRs, release notes, or publishing work for tiny local tasks.
- For repo/product work, consider Planning / Spec and GitHub Delivery explicitly.
- For public/export/publish work, Release / Publish must not be `N/A`.
- Final reports should mirror the same layers with what actually happened.

### 1. Obsidian Brain Layer

- Read the current user request first.
- Read the smallest useful project context: current state, task board, checklist, decisions, and handoff.
- Respect user preferences and project decisions, but verify real files/runtime before final claims.

### 2. Planning / Spec Layer

- For substantial product/code/repo work, create only the planning files that help:
  - `PRD.md`
  - `SPEC.md`
  - `ARCHITECTURE.md`
  - `AGENTS.md`
  - acceptance criteria
- Tiny safe edits can use a short checklist instead of a full spec set.
- For ingestion or research work, keep raw sources separate from processed notes, use an index/retrieval tool before opening large knowledge folders, and promote only evidence-backed learnings into stable project memory.

### 3. GitHub Delivery Layer

- Use issues, implementation branches, pull requests, review/fix, and merge only when repo delivery is in scope.
- For local-only memory/docs tasks, mark this layer `N/A`.
- Do not push, force-push, publish, deploy, or merge without explicit approval for that exact action.

### 4. Verification / Risk Gate Layer

- Match verification to the task: tests, smoke checks, UI/game probes, scrub, audit, security/privacy check, or targeted inspection.
- Stop before hard delete, broad rewrite, deploy, account/auth/payment/secret work, OS repair, or risky automation.
- For public/repo work, run privacy and secret scans before release or push.

### 5. Release / Publish Layer

- Use this only when the task changes something intended for release, public sharing, repo publishing, deployment, or user-facing versioning.
- Include changelog, version, release notes, public/private gate, scrub/privacy check, and rollback note when relevant.
- For normal local tasks, mark this layer `N/A`.
- Never treat local completion as permission to publish.

### 6. Sync Back / Learning Layer

- After local completion, PR, merge, release, or blocked work, sync result, decisions, lessons, bug patterns, next task, and dashboard/status updates back into project notes.
- Update task board/checklist/current state/handoff only when evidence supports it.
- Keep detailed execution logs in dated work logs or project-local reports.

### Task Board / Checklist Rule

- Use explicit task IDs such as `T001`.
- Use one canonical checklist with Markdown checkboxes.
- Each task should include goal, done condition, verification, risk, and recommended intelligence level.
- Tick tasks only after verification evidence exists.

### Legacy Project Alignment Rule

Do not reopen or rewrite old completed tasks just to retrofit the six-layer format.

- Treat completed tasks as valid if they have a clear result, project-state/work-log evidence, and verification.
- Apply the six-layer mini-plan from the next new task onward.
- Create a one-time alignment pass only when an old important project is active again or missing structure blocks safe continuation.
- Alignment must be preserve-first, small, and gap-filling only.

## Project Shape

For an ongoing project, keep a small set of canonical files:

```text
README.md
CURRENT_STATE.md
TASK_BOARD.md
TASK_CHECKLIST.md
DECISION_LOG.md
HANDOFF.md
```

Use existing project conventions if they are clearer.

For larger repo work, add only the planning files that are useful:

```text
PRD.md
SPEC.md
ARCHITECTURE.md
AGENTS.md
```

## Task Rules

- Give each task an explicit ID such as `T001`.
- Put tasks in both a board and a checklist if the project uses both.
- Mark a task complete only after evidence exists.
- Record the intelligence level used or recommended.
- Do not silently reopen completed tasks; create a follow-up task.

Suggested intelligence labels:

```text
low: small mechanical edits, metadata, formatting
medium: ordinary implementation, planning, documentation, scoped debugging
high: hard debugging, architecture, security, automation policy, broad refactor
xhigh: rare high-blast-radius or deeply ambiguous work
```

## Preserve-First Rule

Before compacting, moving, or restructuring important memory:

1. archive the current file or state;
2. record where the archive lives;
3. make the minimal change;
4. verify;
5. record rollback information.

Do not hard-delete important memory unless the user explicitly approves the exact deletion.

## Risk Stop Rules

Stop and ask before:

- hard delete, broad move, or mass rename;
- broad stable-memory rewrite;
- unreviewed installer, plugin, hook, or config change;
- production deploy;
- authentication, account, payment, or secret/API-key handling;
- browser-account actions such as posting, buying, sending messages, or changing settings;
- OS repair, registry, services, drivers, boot, disk, antivirus, or whole-machine cleanup;
- autonomous recurring edits beyond the user's exact request.

When stopping, report:

```text
risk:
exact file or command:
why it matters:
safer option:
backup or rollback:
verification:
```

## Verification

Use the smallest proof that matches the change:

- docs: targeted search and formatting check;
- code: relevant test, lint, build, or smoke check;
- UI/game: browser or runtime check with screenshot/log evidence where possible;
- memory/routing: index or retrieval checks if the project has them;
- research: source links and an adoption boundary.

If verification cannot run, say `not tested`, explain why, and name the exact check to run next.

## Handoff

Close substantial work with:

```text
completed:
files changed:
task updated:
intelligence used:
verification:
not tested:
risks:
next:
```
