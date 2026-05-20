---
name: nova-debug-review-gate
description: Use when Claude Code is debugging, reviewing, investigating failed checks, validating risky plans, or handling suspicious regressions. Requires evidence, fail-path tracing, falsification, breadcrumbs, and verification.
---

# Nova Debug Review Gate for Claude Code

If the full pack is available, follow `workflows/nova-debug-review-gate.md`. If this skill folder was copied alone, the compact rules below are sufficient to operate safely.

Claude Code usage notes:

- Reproduce or inspect evidence before editing.
- Trace the real path through files and commands.
- Do not stop at the first plausible explanation.
- Report exact checks and remaining risk.
- Stop before deploy, auth, payment, secrets, browser-account actions, OS repair, broad rewrite, hard delete, installer, plugin, hook, or config changes unless explicitly approved.
