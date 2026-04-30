# Approved

Human-approved content awaiting WordPress draft creation.

## Approval Requirements
Content may exist in this folder only if:

1. A human reviewer explicitly approved it.
2. Draft `status` is `approved-for-wp-draft`.
3. `templates/article-review-record.md` contains:
   - reviewer identity
   - approval timestamp (UTC)
   - approval decision
   - any conditional notes
4. SEO fields are complete and reviewed.
5. WordPress category/tag assignments follow repository mapping rules.

## Human Approval Gate Before WordPress Draft Push
A **human approval is mandatory** before any WordPress draft push is initiated.

Minimum gate criteria:
- [ ] Human approver is named in review record.
- [ ] Approval timestamp recorded.
- [ ] Content status is `approved-for-wp-draft`.
- [ ] Intended WordPress post status is `draft` only.

## Status and Publishing Boundary
- Content here is approved for WordPress **draft creation only**.
- Publication (`publish`) remains a human-only action in WordPress.
- No automatic publication is permitted.
