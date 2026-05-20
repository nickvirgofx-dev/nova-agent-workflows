# Public Export Scrub Checklist

Run this before publishing or sharing the pack.

## Private Paths

Search for local or private paths:

```text
drive-letter paths
home-directory paths
private vault names
runtime directory names
absolute machine-specific paths
```

Only placeholders should remain:

```text
<PROJECT_ROOT>
<VAULT_ROOT>
<RUNTIME_ROOT>
<TASK_BOARD>
<TASK_CHECKLIST>
<WORK_LOG>
```

## Secrets And Accounts

Search for:

```text
api key
token
oauth
bearer
cookie
password
secret
email
discord
telegram
payment
auth
```

These terms may appear only as risk stop rules or scrub checklist items, not as credentials or action instructions.

## Risky Actions

Ensure all risky actions are written as stop rules:

- deploy
- publish
- push
- account actions
- payment
- authentication
- browser posting or buying
- OS repair
- hard delete
- broad rewrite
- plugin/hook/config install

## Examples

Examples must be synthetic and must not include private project names, screenshots, logs, customer data, personal notes, or real account details.

## License

Confirm the license has final author/year values before public release.

