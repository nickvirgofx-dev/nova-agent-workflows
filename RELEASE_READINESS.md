# Release Readiness

Status: v0.2.0-draft is pushed to `main`. Tagged release remains approval-gated.

## Current State

```text
version: 0.2.0-draft
workflow_revision: nova-serious-workflow v1.5
repo_state: local branch tracks origin/main
remote: https://github.com/nickvirgofx-dev/nova-agent-workflows
published: repository exists
push_performed_for_v0.2.0: yes
release_performed: no
license: MIT, Copyright (c) 2026 Nova Agent Workflows
current_commit: 74e497d Upgrade serious workflow to v1.5
```

## Required Before Public Release

- Run `safety/PUBLIC_EXPORT_SCRUB_CHECKLIST.md`.
- Run `safety/PRE_PUBLISH_RELEASE_GATE.md`.
- Run cross-agent smoke review for Codex, Claude Code, and generic coding-agent use.
- Update `CHANGELOG.md` and `VERSIONING.md` for the release candidate.
- Confirm GitHub authentication and repository target before any future push.

## Current Blockers

- T056 local scrub passed for the v0.2.0-draft edits; see `safety/PUBLIC_EXPORT_SCRUB_REPORT_T056.md`.
- Fresh cross-agent smoke review is required after the v0.2.0-draft edits.
- Tagged release has not been approved for v0.2.0-draft.
- Any push, publish, release, force-push, or remote rewrite requires explicit approval for the exact action.

## Safe Local Prep

It is safe to inspect, edit, scrub, and commit locally in this folder.

It is not safe to push again, publish a package, create a tagged release, force-push, rewrite remote history, authenticate, or handle secrets without explicit approval for that exact action.
