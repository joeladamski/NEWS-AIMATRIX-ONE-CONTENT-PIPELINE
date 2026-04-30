# Scripts (Planned)

This directory will contain automation scripts for governed content workflows.

Current status:
- No publishing automation script is implemented yet.
- Future scripts must follow `wordpress/publishing-rules.md` and enforce `draft`-only posting.

Implementation guardrails for future scripts:
- Use environment variables for all sensitive configuration.
- Support audit logging and explicit failure reporting.
- Require human approval gates before publication actions.
