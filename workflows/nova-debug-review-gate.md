# Nova Debug Review Gate

Use this workflow for bugs, failed checks, suspicious regressions, slow or expensive runs, risky plans, and code reviews.

## Debug Gate

Before fixing:

1. Reproduce or inspect evidence.
2. Trace the real fail path or workflow path.
3. Name the likely hypotheses.
4. Try to falsify the leading hypothesis.
5. Keep breadcrumbs of experiments and outcomes.
6. Make the smallest change that explains the failure.
7. Verify the failing path again.

Report:

```text
evidence:
fail path:
hypotheses:
change:
verification:
breadcrumbs:
next:
```

## Review Gate

Before accepting a risky plan or code change:

1. State the goal in one sentence.
2. Ask whether a smaller approach solves the same goal.
3. Trace the real code or workflow path, not only the diff.
4. Look for edge cases, silent side effects, and missing tests.
5. Report findings first, ordered by severity.
6. Give a verdict.

Verdicts:

```text
ship
fix-then-ship
rework
reject
needs approval
```

## Risk Stop

Stop and ask before:

- hard delete or broad rewrite;
- unreviewed installer, plugin, hook, or config change;
- auth, account, payment, secret, API-key, or deploy action;
- browser-account action;
- OS repair or whole-machine cleanup.

Keep exact paths, commands, errors, and evidence in the report.

