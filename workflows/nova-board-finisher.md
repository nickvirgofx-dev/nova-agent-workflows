# Nova Board Finisher

Use this workflow when the user asks an agent to continue through a task board or checklist until no safe actionable task remains.

This is not permission to bypass risk gates.

## Entry

1. Identify the canonical board and checklist.
2. Read current state, board, checklist, decision log, and handoff if present.
3. Build a short queue from open tasks only.
4. Skip complete, withdrawn, archived, or blocked tasks.
5. Announce the first slice and stop rules.

## Task Selection

Priority:

1. user-named task IDs or task range;
2. board's explicit next task;
3. lowest-numbered safe pending task;
4. cleanup/audit tasks after active project work.

Do not create a new task ID unless new work appears.

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

