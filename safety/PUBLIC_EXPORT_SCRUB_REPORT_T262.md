# Public Export Scrub Report T262

Date: 2026-05-26

Scope:

```text
repo: nova-agent-workflows
draft: 0.3.0-draft local update
workflow_revision: nova-serious-workflow v1.8
```

Changes checked:

- context contract
- Goal/Rider task framing
- structured risk approval wording
- runtime harness verdicts `allow`, `warn`, `review`, `block`
- retry budget
- task-thread events
- agentic delivery chain
- Codex and Claude Code adapter wording

Initial safety position:

- public-safe local draft only
- no push performed
- no tagged release created
- no package publish
- no deploy
- no account/auth/payment/secret action
- no MCP registration
- no hook/global config activation

Required before any public action:

1. `git diff --check`
2. private path scan
3. credential-shaped scan
4. risk wording review
5. cross-agent smoke review
6. user approval for exact push/release action

Local verification:

```text
git diff --check: PASS with LF/CRLF warnings only
private path scan: 0 matches for the private local path markers listed in the scrub checklist
credential-shaped scan: 0 matches for long OpenAI/GitHub/Slack/AWS/Google key shapes or assignment-shaped password/token/api key/secret values
risk-word scan: matches are in stop rules, release gates, scrub reports, or safety wording
cross-agent smoke review: PASS by static review for Codex adapter, Claude Code adapter, and generic workflow docs
```

Result:

```text
status: local scrub passed; public push/release still blocked until exact user approval
```
