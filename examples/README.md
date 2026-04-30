# Examples Directory Notice

Files in `examples/` are **demonstration artifacts only**.

## Rules
- **Never push files from `examples/` to WordPress.**
- **Never treat `examples/` content as publishable production content.**
- Use these files only for structure validation, onboarding, and workflow demonstrations.

## Safety Expectation
Any sample content should explicitly include non-publishable safeguards such as:
- `status: "sample"`
- `wordpress_push: false`
- `review_status: "sample_only"`
- `post_status: "none"`
- `canonical_url: "SAMPLE_DO_NOT_PUBLISH"`
