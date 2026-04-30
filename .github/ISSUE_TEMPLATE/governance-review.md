---
name: Governance Review
description: Request governance review for a proposed repository change.
title: "Governance review: <short title>"
labels: ["governance", "review"]
assignees: []
---

## Summary
Describe the change request and why it is needed.

## Change Type
- [ ] Documentation/process update
- [ ] AI behavior update
- [ ] Prompt/model-behavior update
- [ ] Automation/workflow update
- [ ] Security-sensitive update

## Governance Mapping

### System Purpose
What system purpose does this affect?

### User Role
Who are the intended users/operators?

### Authority Boundary
What can AI decide? What requires human approval?

### Input Sources
What sources are used, and what is the trust hierarchy?

### Output Type
What outputs are produced?

### Human Oversight / Override
How can humans review, override, or stop this?

### Auditability Path
Where is evidence logged (files, PRs, workflow logs)?

## Risk and Controls
- Risk level: **Low / Medium / High**
- Failure mode:
- Mitigation:

## Validation Plan
How will this be tested and verified before merge?

## Rollback Plan
How can this be reverted safely if needed?
