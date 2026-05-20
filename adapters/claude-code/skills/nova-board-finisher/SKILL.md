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
