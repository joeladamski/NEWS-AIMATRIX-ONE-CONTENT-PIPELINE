# WordPress Draft Publisher Requirements (Future Runtime Specification)

## Intent
Define the required runtime behavior for a **future** GitHub Action that posts approved markdown content to WordPress as drafts.

This file is a requirements/specification document only. It does not implement automation.

## Required Inputs
1. Approved markdown content from repository-controlled approval path.
2. Runtime secrets from GitHub Actions:
   - `WP_SITE_URL`
   - `WP_USERNAME`
   - `WP_APP_PASSWORD`
   - `WP_AUTHOR_EMAIL`

## Secret Handling Rules
- Secrets are read only at workflow runtime from GitHub Actions secrets.
- Secrets are never committed to this repository.
- Secrets are never printed in logs.
- Workflow debugging must mask secret-bearing variables.

## Future Runtime Flow
1. GitHub Action is triggered for approved content.
2. Action reads approved markdown file and validates required metadata.
3. Action loads WordPress credentials/configuration from GitHub Actions secrets.
4. Action calls WordPress REST API endpoint for posts.
5. Action creates post with `status` set to `draft`.
6. Human reviewer opens WordPress admin, reviews content, and publishes manually.

## Functional Requirements
- Must reject execution if required secret is missing.
- Must fail closed (no post creation) on authentication or validation errors.
- Must support idempotency guardrails to reduce duplicate drafts.
- Must emit auditable, non-sensitive logs (file, title, response ID, timestamp).
- Must not include any code path that sets `status=publish`.

## Non-Functional Requirements
- Reliability: clear error handling and deterministic exit codes.
- Security: least-privilege credentials and masked logging.
- Auditability: traceable run logs and run IDs in GitHub Actions.
- Maintainability: modular script/action design with explicit interfaces.

## Authority Boundary
- AI/automation authority: prepare and submit **draft only**.
- Human authority: final editorial review, legal/compliance checks, and publish decision.

## Out of Scope (Current Phase)
- Live API connectivity setup.
- Scheduled or event-driven production publishing automation.
- Any direct publishing to production WordPress.
