# Draft Publisher Plan (Documentation-Only)

This document defines the intended architecture for future draft creation automation.

## Scope
- In scope: create WordPress posts as `draft` from approved repository content.
- Out of scope: direct publication to `publish` state.

## Planned Flow
1. Trigger: manual GitHub Actions dispatch or controlled n8n webhook.
2. Input: content package from `content/approved/` plus WordPress metadata mapping.
3. Validation: schema checks using templates and publishing rules.
4. Delivery: call WordPress API with `status=draft`.
5. Review handoff: notify human editorial owner in WordPress.
6. Publication: completed by human inside WordPress UI.

## Security and Secrets
- Use GitHub Secrets for endpoint URLs and credentials.
- Use environment variables locally and in CI.
- Never commit real credentials.

## Rollback/Failure Concepts
- If API call fails, content remains in `content/approved/` with failure log.
- Retry must be explicit and logged.
- No auto-escalation to publish.

## Current State
No draft publishing script is implemented yet.
