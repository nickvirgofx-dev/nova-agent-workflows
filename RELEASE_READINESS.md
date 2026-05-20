# Release Readiness

Status: approved by user for public GitHub release after final scrub passes.

## Current State

```text
version: 0.1.0-draft
repo_state: local only
remote: none
published: no
push_performed: no
release_performed: no
license: MIT, Copyright (c) 2026 Nova Agent Workflows
local_commit: see latest `git log -1 --oneline`
```

## Required Before Public Release

- Run `safety/PUBLIC_EXPORT_SCRUB_CHECKLIST.md`.
- Run `safety/PRE_PUBLISH_RELEASE_GATE.md`.
- Run cross-agent smoke review for Codex, Claude Code, and generic coding-agent use.
- Update `CHANGELOG.md` and `VERSIONING.md` for the release candidate.
- Confirm GitHub authentication and repository target before push.

## Current Blockers

- Fresh final scrub is required after this license edit.
- Fresh cross-agent smoke review is required after this license edit.
- GitHub remote is not created yet.
- Push/publish/release has not happened yet.
- `gh` CLI is not available in this shell.
- Available GitHub connector can inspect repositories and write files to an existing repository, but does not expose repository creation.

## Safe Local Prep

It is safe to inspect, edit, scrub, and initialize a local git repository for this folder.

It is not safe to create a remote, push, publish, release, authenticate, or handle secrets without explicit approval for that exact action.
