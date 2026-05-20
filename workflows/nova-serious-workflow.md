# Nova Serious Workflow

Use this workflow when an agent starts or continues serious work that needs context, tasks, verification, safe delivery, and sync-back.

## Core Rule

Current user instruction, real files, tests, and runtime evidence outrank stored memory.

Stored notes are orientation, not final truth.

## Nova Serious Workflow v1.5: Six-Layer Stack

Use the layers that fit the task. Small safe tasks may use a compact path, but meaningful work should still sync back to the project notes.

### 1. Brain / Context Layer

- Read the current user request first.
- Read the smallest useful project context: current state, task board, checklist, decisions, and handoff.
- Respect user preferences and project decisions, but verify real files/runtime before final claims.

### 2. Ingestion / Knowledge Layer

- Keep raw source material separate from processed notes.
- Use an index or retrieval tool before opening large knowledge folders.
- Do not scan raw or wiki folders wholesale.
- Promote only evidence-backed learnings into stable project memory.

Suggested generic shape:

```text
knowledge/
  ingestion/
    raw/
    wiki/
    index.md
    log.md
```

### 3. Planning / Spec Layer

- For substantial product/code/repo work, create only the planning files that help:
  - `PRD.md`
  - `SPEC.md`
  - `ARCHITECTURE.md`
  - `AGENTS.md`
  - acceptance criteria
- Tiny safe edits can use a short checklist instead of a full spec set.

### 4. Task Board / Checklist Layer

- Use explicit task IDs such as `T001`.
- Use one canonical checklist with Markdown checkboxes.
- Each task should include goal, done condition, verification, risk, and recommended intelligence level.
- Tick tasks only after verification evidence exists.

### 5. Verification / Risk Gate Layer

- Match verification to the task: tests, smoke checks, UI/game probes, scrub, audit, or targeted inspection.
- Stop before hard delete, broad rewrite, deploy, account/auth/payment/secret work, OS repair, or risky automation.
- For public/repo work, run privacy and secret scans before release or push.

### 6. Delivery + Sync-Back Layer

- Use issues, implementation branches, pull requests, review/fix, and merge only when repo delivery is in scope.
- Release/publish work needs changelog, version, release notes, public/private gate, and rollback note.
- After local completion, PR, merge, release, or blocked work, sync result, decisions, lessons, bug patterns, next task, and dashboard/status updates back into project notes.

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
