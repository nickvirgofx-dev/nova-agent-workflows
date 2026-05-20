# Risk Gates

These gates apply to all workflows and adapters.

## Stop Without Exact Approval

An agent must stop before:

- hard delete;
- broad move or mass rename;
- broad stable-memory rewrite;
- unreviewed installer, plugin, hook, or config change;
- production deploy;
- publishing or pushing to a public remote;
- authentication, account, payment, secret, token, API-key, OAuth, cookie, or bearer-token handling;
- browser-account actions such as posting, buying, sending messages, or changing settings;
- OS repair, registry, services, drivers, boot, disk, antivirus, or whole-machine cleanup;
- autonomous recurring edits beyond the user's exact request.

## Required Stop Report

```text
risk:
exact file or command:
why it matters:
safer option:
backup or rollback:
verification:
```

## Safer Defaults

- Prefer read-only inspection before mutation.
- Prefer local draft before public release.
- Prefer archive/quarantine before deletion.
- Prefer synthetic examples before real user data.
- Prefer small scoped changes before broad rewrites.

