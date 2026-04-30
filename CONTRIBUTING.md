# Contributing

Thank you for contributing to **AI-CONSTITUTION-REPO-STARTER**.

This repository is **governance-first**. Changes are accepted when they improve traceability, operational safety, and human oversight.

## Scope of Contributions

Accepted contribution areas:
- Governance framework clarity and maintainability
- Templates, review workflows, and audit readiness
- Documentation quality for policy, risk, and decision records

Out of scope unless explicitly authorized:
- Application/business feature code
- Doctrine rewrites under `docs/source-framework/` without approved authority

## Required Pre-Change Reading

Before opening a PR, review:
1. `README.md`
2. `AGENTS.md`
3. `docs/source-framework/04-AI-CONSTITUTION-CORE-FRAMEWORK.md`
4. `docs/source-framework/07-AI-CONSTITUTION-DO-NOT-DRIFT.md`
5. `.ai-constitution/CHARTER.md`
6. `.ai-constitution/POLICY.md`
7. `.ai-constitution/CHANGE_AUTHORITY.md`
8. `.ai-constitution/RISK_REGISTER.md`
9. `.ai-constitution/DECISION_LOG.md`
10. `.github/PULL_REQUEST_TEMPLATE.md`

## Contribution Process

1. **Open an issue first** for governance-sensitive work.
2. **State authority boundary**: what AI may do vs what humans must approve.
3. **Keep diffs small and auditable**; one decision domain per PR when possible.
4. **Map change to governance controls** in PR description.
5. **Run governance checks locally** and ensure CI passes.

## Pull Request Expectations

Every PR should include:
- What changed
- What did not change
- Why the change is needed now
- Risk level (Low/Medium/High)
- Failure mode and mitigation
- Human oversight and rollback path

If relevant, include mappings for:
- AI behavior changes
- Prompt/model-behavior changes
- Automation/workflow changes
- Security-sensitive changes

## Review and Approval

- Human reviewers are final decision-makers.
- Security, policy, access, and production-impacting changes require explicit human approval.
- If uncertainty exists, default to escalation rather than silent interpretation.

## Commit Hygiene

- Use descriptive commit messages.
- Avoid unrelated file churn.
- Do not commit secrets, credentials, or environment-specific tokens.

## Security Reporting

Please do not open public issues for sensitive vulnerabilities.
Follow `SECURITY.md` for responsible disclosure procedures.
