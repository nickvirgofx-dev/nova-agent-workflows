# Public Export Scrub Report - T047

Date: 2026-05-20
Status: local draft check passed with release blockers noted.

## Scope

Checked local draft only. No publish, push, remote repository creation, deployment, account action, secret handling, hook install, plugin install, or OS repair was performed.

## Draft Root

```text
<RUNTIME_ROOT>/public_exports/nova-agent-workflows
```

## Checks

Private path scan:

```text
patterns: local drive paths, private vault names, private runtime names
result: no matches in file contents
```

Credential-like scan:

```text
patterns: common API key, GitHub token, Slack token, AWS key, Google key shapes
result: no real credential-shaped matches
note: one broad scan pattern matched normal words such as "task-local"; treated as false positive.
```

Risk-word scan:

```text
patterns: deploy, publish, push, auth, payment, secret, OS repair, hard delete, hook, plugin, installer, account
result: matches exist only as risk gates, stop rules, release blockers, or checklist items.
```

Adapter validation:

```text
Codex nova-serious-workflow: pass
Codex nova-debug-review-gate: pass
Codex nova-board-finisher: pass
Claude Code nova-serious-workflow: pass
Claude Code nova-debug-review-gate: pass
Claude Code nova-board-finisher: pass
```

## Release Blockers

Before public release:

- replace the license author/year placeholder in `LICENSE` before release;
- perform a fresh scrub after any edits;
- decide whether to keep MIT license;
- run a clean diff/format check in the export folder;
- have a fresh agent read `README.md` and confirm it can use the pack without private Nova memory.
