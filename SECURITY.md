# Security Policy

## Supported Use

This repository is a governance/documentation starter. Security focus areas include:
- Integrity of governance artifacts
- Change authorization controls
- Audit trail reliability
- Protection against policy bypass or drift

## Reporting a Vulnerability

If you discover a vulnerability or governance bypass path:

1. **Do not disclose publicly** in issues or PRs.
2. Report privately to the maintainers through your approved private channel.
3. Include:
   - Affected files/paths
   - Reproduction steps
   - Threat/misuse scenario
   - Proposed containment

## Triage and Response Expectations

Maintainers should:
- Acknowledge receipt within 3 business days.
- Classify severity (Low/Medium/High/Critical).
- Define owner, containment plan, and remediation timeline.
- Record decisions in `.ai-constitution/DECISION_LOG.md` when governance-impacting.
- Update `.ai-constitution/RISK_REGISTER.md` when new or changed risk is confirmed.

## Handling Sensitive Changes

Security-sensitive changes (identity, authorization, secrets, data handling, production controls) must document:
- Security boundary affected
- Threat scenario
- Guardrail/control added or modified
- Approval authority
- Audit/logging impact
- Rollback/containment plan

## Secrets and Credentials

- Never commit secrets, private keys, tokens, or production credentials.
- Use environment variables and secret stores managed by your platform.
- Rotate any credential immediately if exposed.

## Policy

If in doubt, favor controlled escalation and human review over rapid merge.
