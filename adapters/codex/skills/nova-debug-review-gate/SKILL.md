---
name: nova-debug-review-gate
description: Use for bugs, failed tests, broken UI/game behavior, slow or expensive agent runs, suspicious regressions, risky plan/code review, or second-opinion review. Requires evidence, fail-path tracing, hypothesis falsification, breadcrumbs, simpler-alternative review, and verification before completion.
---

# Nova Debug Review Gate

If the full pack is available, use `workflows/nova-debug-review-gate.md` as the canonical public workflow. If this skill folder was copied alone, the compact rules below are sufficient to operate safely.

For Codex:

1. Inspect current evidence before changing files.
2. Trace the real code or workflow path.
3. Name hypotheses and try to falsify the leading one.
4. Keep a short breadcrumb trail.
5. Make the smallest fix that explains the failure.
6. Verify the failing/risky path again.

Stop before deploy, auth/account, payment, secret, browser-account, OS repair, broad rewrite, hard delete, plugin/hook/config, or installer actions unless the user explicitly approves the exact action.
