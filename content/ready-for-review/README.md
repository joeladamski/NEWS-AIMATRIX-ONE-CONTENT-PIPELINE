# Ready for Review

Articles prepared for human reviewer evaluation.

## Promotion Into This Folder
A file may be moved from `content/drafts/` to `content/ready-for-review/` only when:

1. Filename matches `YYYY-MM-DD__topic-slug__vNN.md`.
2. Required front matter fields are present.
3. Draft `status` is `draft-ready-for-review`.
4. `templates/article-seo-checklist.md` is completed and attached/linked.
5. `templates/article-review-record.md` is created and initialized.

## Review Promotion Rules (to Approved)
Human reviewer may promote to `content/approved/` only when all are true:

- `status` is updated to `review-approved`.
- Facts/sources were checked by a human.
- Canonical URL field is resolved or explicitly approved as a placeholder exception.
- WordPress taxonomy fields pass mapping rules in `wordpress/post-status-lifecycle.md`.
- Review record includes reviewer name, timestamp (UTC), and decision notes.

## Rejection / Revision Handling
If changes are needed:
- Set `status` to `review-changes-requested`.
- Return file to `content/drafts/` with incremented version (`vNN`).
- Preserve prior review record for auditability.

## Guardrails
- No publishing automation is executed from this folder.
- No credentials, tokens, or secrets are stored in content files.
