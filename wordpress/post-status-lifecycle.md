# WordPress Post Status Lifecycle (Draft-Only Governance)

## Scope
Defines allowed status flow between repository content states and WordPress post states.

## Repository Status Values
Allowed content workflow values:
- `draft-in-progress`
- `draft-ready-for-review`
- `draft-needs-revision`
- `review-changes-requested`
- `review-approved`
- `approved-for-wp-draft`
- `wp-draft-created`

## Allowed Lifecycle
1. `draft-in-progress` (content/drafts)
2. `draft-ready-for-review` (move to content/ready-for-review)
3. `review-approved` OR `review-changes-requested`
4. `approved-for-wp-draft` (move to content/approved)
5. WordPress post created with `status=draft`
6. Repository status updated to `wp-draft-created`

## Prohibited Lifecycle Actions
- No automated transition to WordPress `publish`.
- No automated scheduling (`future`) or private publication.
- No bypass of human approval gate.

## WordPress Category/Tag Mapping Rules
Before WordPress draft creation:
- `wp_categories` must map to existing entries in `wordpress/category-map.md`.
- `wp_tags` must map to existing entries in `wordpress/tag-map.md`.
- New categories/tags require human editorial approval and map update before use.
- Use slug values (not display labels) in front matter for deterministic mapping.

## Human Oversight Rule
Human approval record is required before any draft push. Approved content authorizes `draft` creation only.
