# Versioning

Nova Agent Workflows should improve over time without confusing existing users.

## Version Format

Use semantic versions:

```text
MAJOR.MINOR.PATCH
```

- `MAJOR`: breaking workflow or adapter changes.
- `MINOR`: new workflow, template, adapter, or substantial non-breaking capability.
- `PATCH`: wording fixes, safety clarifications, small template corrections.

Draft versions may use:

```text
0.1.0-draft
```

## Current Line

```text
0.1.x: safety-first core workflows
```

Included in v0.1:

- `nova-serious-workflow`
- `nova-debug-review-gate`
- `nova-board-finisher`
- Codex skill adapter
- Claude Code skill adapter
- basic task/checklist/work-log/handoff templates
- synthetic examples only

## Future Upgrade Track

Potential v0.2 additions:

- HTML planning artifact workflow
- public-safe postmortem template
- graph/link hygiene workflow
- token/context budget workflow
- optional release checklist automation that only scans local files

Potential v0.3 additions:

- browser-game verification adapter
- Obsidian librarian adapter
- cross-agent handoff examples
- public test fixtures

Do not add account automation, deployment automation, secret handling, OS repair, or hooks that run by default.

## Upgrade Rule

Every upgrade should update:

1. `VERSIONING.md`
2. `CHANGELOG.md`
3. affected workflow files
4. affected adapters
5. examples or templates if behavior changed
6. public scrub checklist result before release
7. pre-publish release gate result before release
8. cross-agent smoke review result before release

## Permanent Release Gate

Every release candidate must pass the release gate in the same work session as the public action.

Required release-gate files:

```text
safety/PUBLIC_EXPORT_SCRUB_CHECKLIST.md
safety/PRE_PUBLISH_RELEASE_GATE.md
safety/RISK_GATES.md
RELEASE_READINESS.md
```

The release gate expires after any edit to public files.

Do not create a GitHub repository, add a remote, push, publish, release, authenticate, or handle secrets as part of version alignment. Those actions require explicit approval for the exact action after the gate result is shown.

## Nova Alignment Rule

When private Nova workflows improve, decide whether the public pack should change too.

Update the public pack only when the improvement is reusable outside the private brain. Do not export private project memory, local runtime logs, account material, or machine-specific paths.

For each reusable upgrade, check:

```text
workflows/*.md
adapters/codex/skills/*/SKILL.md
adapters/claude-code/skills/*/SKILL.md
adapters/claude-code/CLAUDE.md.example
templates/*.md
examples/*.md
safety/*.md
CHANGELOG.md
VERSIONING.md
```

If the change improves Nova's overall brain capability, also update the Nova Brain Evolution Dashboard in the private runtime.

Never publish, push, create a remote repository, or run account/auth/payment/secret actions as part of version alignment.

## Compatibility Rule

Keep the core workflow files agent-agnostic. Put tool-specific details in `adapters/`.

If a workflow requires a feature only one agent supports, mark it as adapter-specific rather than changing the core workflow.
