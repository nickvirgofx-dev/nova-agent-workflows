---
name: nova-board-finisher
description: Use when the user asks Codex to finish remaining safe tasks in a task board, checklist, backlog, or T-number sequence. Continue through safe tasks only, preserve first, verify, update board/checklist/current state, and stop at risk gates.
---

# Nova Board Finisher

If the full pack is available, use `workflows/nova-board-finisher.md` as the canonical public workflow. If this skill folder was copied alone, the compact rules below are sufficient to operate safely.

For Codex:

1. Identify the canonical board/checklist.
2. Build a queue from open tasks only.
3. Complete the next safe task with evidence.
4. Update the board/checklist/current state.
5. Continue only while tasks are safe and verification passes.
6. Stop if approval, credentials, deployment, payment/auth, secrets, OS repair, hard delete, broad rewrite, or ambiguous task truth appears.
7. For GitHub delivery tasks, keep one approved issue or task as the unit of work.
8. Stop before creating issues, pushing commits, opening PRs, marking PRs ready, merging, publishing, deploying, changing repo settings, force-pushing, or rewriting remote history unless the user explicitly approves that exact action.
