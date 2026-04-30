# AI Constitution Operational Policy

## 1) Repository Source Doctrine
All governance implementation in this repository must map back to documents inside `docs/source-framework/`.

## 2) Required Governance Artifacts
The following artifacts are required before production release:
- `CHANGE_AUTHORITY.md` updated for ownership
- `DECISION_LOG.md` updated for architectural/governance choices
- `RISK_REGISTER.md` updated for known and accepted risks
- `.github/PULL_REQUEST_TEMPLATE.md` checklist completed

## 3) Human Oversight Requirements
Human approval is required for:
- policy changes
- security-sensitive feature changes
- production workflow changes
- agent/autonomous behavior changes

## 4) Drift Prevention
Repository outputs must remain governance-first. Avoid:
- generic hype content
- framework-irrelevant changes
- undocumented autonomous behaviors
- unexplained architectural deviations

## 5) Auditability
Every pull request must provide:
- intent
- impacted systems
- risk impact
- rollback plan (if operationally relevant)
