---
name: nova-board-finisher
description: Use when Claude Code should continue through safe open tasks in a board/checklist until no safe actionable tasks remain, while preserving work, verifying, updating status, and stopping at risk gates.
---

# Nova Board Finisher for Claude Code

If the full pack is available, follow `workflows/nova-board-finisher.md`. If this skill folder was copied alone, the compact rules below are sufficient to operate safely.

Claude Code usage notes:

- Work from open tasks only.
- Complete the next safe task first.
- Mark done only after verification.
- Keep handoff short enough for the next agent to use.
- Stop when approval or risky systems are required.
- For GitHub delivery tasks, keep one approved issue or task as the unit of work.
- Stop before creating issues, pushing commits, opening PRs, marking PRs ready, merging, publishing, deploying, changing repo settings, force-pushing, or rewriting remote history unless the user explicitly approves that exact action.
