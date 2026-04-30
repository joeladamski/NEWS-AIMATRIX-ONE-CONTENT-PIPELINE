# WordPress Secrets Configuration (Draft-Only Workflow)

## Purpose
This document defines how WordPress credentials and configuration must be handled for the **future draft-only publishing workflow**.

This repository must never store live credentials, tokens, or passwords in tracked files.

## Scope and Current Boundary
- This is documentation only.
- No WordPress connection is implemented from this document.
- No live publishing automation is implemented from this document.
- Any future automation must create WordPress posts with `status=draft` only.

## Required GitHub Actions Secrets
Create the following repository or organization secrets in GitHub Actions:

- `WP_SITE_URL`
  - Base URL of the target WordPress site (example format: `https://example.com`)
  - Must not include embedded credentials.
- `WP_USERNAME`
  - WordPress user account name used for API authentication.
- `WP_APP_PASSWORD`
  - WordPress Application Password generated for `WP_USERNAME`.
- `WP_AUTHOR_EMAIL`
  - Author email to map editorial ownership and audit references.

## Security Requirements
1. **Secrets must only be referenced through GitHub Actions secrets contexts** (for example, `${{ secrets.WP_SITE_URL }}`).
2. Secrets must **never** be committed into:
   - Markdown files
   - Workflow YAML in plaintext
   - Source code files
   - Shell scripts
   - Logs or debug output
3. Secrets must never be echoed, printed, or written to artifacts.
4. Local `.env` files containing real values must remain untracked.
5. Rotation and revocation must be handled by human operators through WordPress and GitHub settings.

## Usage Pattern (Documentation-Level)
In future workflows, non-sensitive configuration may be loaded from repository files, while sensitive values are loaded at runtime from GitHub Actions secrets.

Expected pattern:
- Workflow step receives secrets via environment variables.
- Runtime process builds authenticated request to WordPress REST API.
- Process sends draft post payload only.
- Output captures non-sensitive response metadata (for audit), not credentials.

## Governance and Oversight
- Human review remains mandatory before publishing any post.
- Automation authority boundary is limited to draft creation only.
- Publication to `status=publish` is a human decision in WordPress admin.
- Any change to this boundary requires governance review and approval.

## Prohibited Practices
- Hardcoding `WP_*` values in repository files.
- Creating direct auto-publish paths.
- Bypassing human editorial review.
- Using personal tokens outside managed secret stores.
