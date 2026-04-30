# AI-CONSTITUTION-REPO-STARTER

Governance-first repository starter for building AI systems, automations, agents, and platform integrations under the AI Constitution Framework.

## Core Doctrine Source
Canonical source documents are stored in:

- `docs/source-framework/`

These files are preserved as the doctrine layer and should be referenced when creating governance or architecture decisions.

## Starter Structure

```text
.ai-constitution/
.github/
docs/source-framework/
templates/
README.md
```

## Using This Template

Use this repository as the starting point for future governed AI projects.

When creating a new repository from this template:

1. Create the new repository from the `AI-CONSTITUTION-REPO-STARTER` template.
2. Review the source doctrine in `docs/source-framework/`.
3. Review the operational governance controls in `.ai-constitution/`.
4. Assign a human owner for governance, security, and release decisions.
5. Use the files in `templates/` for decision records, audit notes, and governance checklists.
6. Keep AI behavior, prompt policy, automation, and system boundaries documented before implementation.
7. Ensure pull requests pass the governance workflow before merging.

The `docs/source-framework/` directory is the canonical doctrine layer.

The `.ai-constitution/` directory is the operational control layer.

Do not rewrite source doctrine casually. If doctrine changes are needed, document the reason, risk, authority, and approval path.

## Governance-First Workflow
1. Start from doctrine in `docs/source-framework/`.
2. Apply controls in `.ai-constitution/`.
3. Use templates in `templates/` to keep changes auditable and reviewable.
4. Enforce governance checks in pull requests via `.github/PULL_REQUEST_TEMPLATE.md`.

## Core Thesis
AI does not become trustworthy because it is powerful.
AI becomes trustworthy when it is governed.

## Draft Publishing Workflow for news.aimatrix.one

Codex writes article drafts → GitHub stores reviewed content → GitHub Actions or n8n sends posts to WordPress as draft → human reviews in WordPress → human publishes.

### Workflow Stages
1. **Drafting:** AI-generated article drafts are created in `content/drafts/`.
2. **Review Prep:** Drafts move to `content/ready-for-review/` with required templates and metadata.
3. **Approval:** Human reviewers approve and move content to `content/approved/`.
4. **Draft Delivery:** A future governed automation (GitHub Actions or n8n) submits approved content to WordPress with `status=draft` only.
5. **Human Publication:** Human editors review and publish manually in WordPress.

### Governance Constraints
- No direct auto-publishing to WordPress.
- WordPress post creation is draft-only.
- Human review is mandatory before publication.
- Secrets are managed via environment variables and GitHub Secrets; no real credentials in repo.
