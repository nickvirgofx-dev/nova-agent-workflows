# Nova Serious Workflow

Use this workflow when an agent starts or continues serious work that needs memory, tasks, verification, and safe handoff.

## Core Rule

Current user instruction, real files, tests, and runtime evidence outrank stored memory.

Stored notes are orientation, not final truth.

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

