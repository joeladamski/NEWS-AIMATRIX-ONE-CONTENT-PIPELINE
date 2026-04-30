# WordPress Publishing Rules

## Non-Negotiable Rules
1. Automation must never publish directly to WordPress.
2. All created WordPress posts must use `draft` status.
3. Human review in WordPress is required before publication.
4. Credentials, tokens, and secrets must never be committed to this repository.
5. Integrations must use environment variables and GitHub Secrets placeholders only.

## Governance Controls
- Source doctrine under `docs/source-framework/` is read-only unless governance authority approves changes.
- Approved content in this repository is authorization for draft creation only.
- Final publication authority remains with designated human operators.

## Audit Expectations
- Record who approved content and when.
- Record automation execution logs (workflow run IDs, timestamps).
- Record human publication events and resulting WordPress URL.
