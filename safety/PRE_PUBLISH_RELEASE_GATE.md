# Pre-Publish Release Gate

Run this gate before any public share, GitHub repository creation, remote setup, push, publish, release, or package distribution.

This gate is mandatory even if an older scrub report passed. The gate expires after any edit to public files.

## Required Status

```text
status: blocked until all checklist items pass
release_action: not approved by default
remote_setup: not approved by default
push_publish_release: not approved by default
```

## Scrub Evidence

Record the exact result for each scan:

- private paths and machine-specific paths;
- credential-shaped strings;
- account/auth/payment/secret/browser-account terms;
- deploy/publish/push wording;
- copied external text or unlicensed content;
- private project names, logs, screenshots, or personal examples.

All risky terms must appear only as stop rules, blockers, or scrub checklist items.

## Cross-Agent Smoke Review

Review the release candidate from these perspectives:

- Codex adapter: copied skill folders make sense without private local memory.
- Claude Code adapter: `CLAUDE.md.example` and skills do not require hooks, plugins, private paths, or startup automation.
- Generic coding agent: README, core workflows, templates, and examples are usable without Codex- or Claude-only features.

Smoke review is documentation-level by default. Do not install plugins, create hooks, authenticate accounts, create remotes, push, publish, or release during smoke review.

## Release Blockers

Block release if any item is true:

- `LICENSE` still has placeholder author/year.
- License choice is not final.
- Any private path or credential-shaped string appears outside a scrub checklist or stop rule.
- Examples are not synthetic.
- README overclaims capability or implies autonomous unsafe action.
- Risk gates are missing or weakened.
- User has not explicitly approved the exact public action.

## Final Approval Prompt

Before any public action, ask the user with exact wording similar to:

```text
I can now perform this exact public action: <ACTION>.
Risk: this may publish files publicly or create remote history.
Backup: local repo path is <REPO_PATH>.
Verification already passed: <REPORT_PATHS>.
Do you approve this exact action?
```

If the answer is not explicit approval, stop.
