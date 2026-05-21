# Public Export Scrub Report T104

Date: 2026-05-21

Scope:

- Upgrade public workflow pack to `0.2.2-draft`.
- Align `nova-serious-workflow` to v1.7 planner/orchestrator/review overlay.
- Add board-finisher GitHub delivery guard.
- Update Codex and Claude Code adapters.

Approval:

- User requested: `T104 ลุยๆ`
- Interpreted as approval to update, commit, and push `nickvirgofx-dev/nova-agent-workflows` for this exact T104 public-pack update only.

Commands run from repository root:

```text
git grep -n -E "<private path and known private project marker pattern>" -- .
git grep -n -E "(sk-[A-Za-z0-9]|ghp_[A-Za-z0-9]|xox[baprs]-|AKIA[0-9A-Z]{16}|AIza[0-9A-Za-z_-]{35}|password\s*[:=]|token\s*[:=]|api[_ -]?key\s*[:=]|secret\s*[:=]|bearer\s+[A-Za-z0-9._-]+)" -- .
git grep -n -E "(delete|deploy|publish|push|auth|payment|secret|OS repair|hard delete|broad rewrite|hook|plugin|installer|account|merge|force-push|PR)" -- .
git status --short --branch
```

Private path / project-name scan:

```text
RELEASE_READINESS.md:11:remote: https://github.com/nickvirgofx-dev/nova-agent-workflows
safety/PUBLIC_EXPORT_SCRUB_REPORT_T102.md:36:- Push to `main` is allowed only because the user explicitly requested updating `nickvirgofx-dev/nova-agent-workflows`.
```

Decision: PASS. These are public repository references, not private memory paths. No private vault path, runtime path, local drive path, private project memory, or copied archived-skill source path appears in public content.

Credential-shaped scan:

```text
safety/PUBLIC_EXPORT_SCRUB_REPORT_T047.md:30:note: one broad scan pattern matched normal words such as "task-local"; treated as false positive.
safety/PUBLIC_EXPORT_SCRUB_REPORT_T047.md:33:Risk-word scan:
workflows/nova-board-finisher.md:57:1. read task-local context;
workflows/nova-board-finisher.md:60:4. run task-specific verification;
```

Decision: PASS. Matches are false positives from ordinary words, not credentials.

Risk-word scan:

- Risk words appear in stop rules, release gates, scrub reports, or MIT license text.
- T104 additions keep GitHub issue creation, push, PR, merge, publish, deploy, account/auth/payment/secret, force-push, and repo-setting changes behind explicit approval.

Cross-agent smoke review:

- Codex adapter: PASS. Copied skill can operate alone and points to the canonical workflow when available.
- Claude Code adapter: PASS. Does not require hooks, plugins, startup automation, private paths, or external memory.
- Generic coding-agent use: PASS. README, workflow, and templates describe reusable patterns without depending on Nova's private brain.

Actions performed:

```text
local_edit: yes
local_scrub: yes
local_commit: yes, completed after this scrub report was staged
push_to_main: yes, completed after local commit
tagged_release: no
package_publish: no
deploy: no
force_push: no
remote_rewrite: no
account_auth_payment_secret_action: no
OS_repair: no
```

Result:

- Public-safe for T104 push to `main`.
- Tagged release and package publishing remain blocked until separately approved.
