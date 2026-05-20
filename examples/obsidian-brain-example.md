# Synthetic Obsidian Brain Example

This is a synthetic example. Do not copy private notes or paths into a public pack.

## Task

```text
T022: Compact oversized work log preserve-first
```

## Board Entry

- [ ] T022: Compact oversized work log preserve-first
  - Goal: Keep the active work log readable and retrieval-friendly.
  - Done when: full pre-compact log is archived, active log keeps only current routing entries, and rollback is documented.
  - Verification: line count, archive hash, and retrieval/index check if available.
  - Risk: over-compaction could hide useful history.
  - Recommended intelligence: medium

## Preserve-First Pattern

```text
1. Copy current file to archive.
2. Record archive path and hash.
3. Replace active file with compact routing summary.
4. Record rollback command.
5. Verify.
```

