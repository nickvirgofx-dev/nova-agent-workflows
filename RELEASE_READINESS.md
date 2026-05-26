# Release Readiness

Status: v0.3.0-draft is prepared locally. Push and tagged release remain approval-gated.

## Current State

```text
version: 0.3.0-draft
workflow_revision: nova-serious-workflow v1.8
repo_state: local branch tracks origin/main
remote: https://github.com/nickvirgofx-dev/nova-agent-workflows
published: repository exists
push_performed_for_v0.2.0: yes
push_performed_for_v0.2.1: yes, after local scrub and commit
push_performed_for_v0.2.2: yes, after T104 local scrub and commit
push_performed_for_v0.3.0: no
release_performed: no
license: MIT, Copyright (c) 2026 Nova Agent Workflows
current_commit: local working tree contains v0.3.0-draft edits until commit/push is explicitly approved
```

## Required Before Public Release

- Run `safety/PUBLIC_EXPORT_SCRUB_CHECKLIST.md`.
- Run `safety/PRE_PUBLISH_RELEASE_GATE.md`.
- Run cross-agent smoke review for Codex, Claude Code, and generic coding-agent use.
- Update `CHANGELOG.md` and `VERSIONING.md` for the release candidate.
- Confirm GitHub authentication and repository target before any future push.

## Current Blockers

- T056 local scrub passed for the v0.2.0-draft edits; see `safety/PUBLIC_EXPORT_SCRUB_REPORT_T056.md`.
- T102 local scrub passed for the v0.2.1-draft edits; see `safety/PUBLIC_EXPORT_SCRUB_REPORT_T102.md`.
- T104 local scrub passed for the v0.2.2-draft edits; see `safety/PUBLIC_EXPORT_SCRUB_REPORT_T104.md`.
- Fresh local scrub is required for v0.3.0-draft before any push.
- Fresh cross-agent smoke review is required before any tagged release.
- Tagged release has not been approved for v0.3.0-draft.
- Any publish, release, force-push, or remote rewrite requires explicit approval for the exact action.

## Safe Local Prep

It is safe to inspect, edit, and scrub locally in this folder.

It is not safe to commit, push, publish a package, create a tagged release, force-push, rewrite remote history, authenticate, or handle secrets without explicit approval for that exact action.
