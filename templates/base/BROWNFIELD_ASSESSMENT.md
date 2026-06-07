# Brownfield Assessment Template

## Assessment identity

```text
Project:
Repository:
Mode: Brownfield governance assessment
Phase:
Component:
Workstream:
Tranche:
Risk level:
Assessment date:
Assessor:
```

## Purpose

State why this brownfield assessment is being performed.

At minimum, explain:

- what repository is being inspected;
- what prompted the assessment;
- whether functional changes are allowed yet;
- what safe resume point should exist after assessment.

## Brownfield rule

No functional code changes should occur until the repository has been inspected, mapped, risk-assessed, and assigned a safe resume point.

## Repository context

Describe the repository in plain terms:

```text
Primary purpose:
Primary users:
Runtime language/framework:
Deployment context:
Data sensitivity:
Production status:
```

## Required inspection checklist

Inspect and mark findings for:

```text
README.md
AGENTS.md
Existing docs/
Existing specs/
Build tools
Runtime language/framework
Tests
CI configuration
Deployment scripts
Data stores
Schemas/migrations
Backup/sync/cleanup logic
Authentication/authorization logic
Secrets and configuration handling
Production service definitions
Existing release process
Existing implementation history
```

## Repository structure assessment

| Area | Current finding | Status | Notes |
|---|---|---|---|
| Root README |  |  |  |
| AGENTS instructions |  |  |  |
| Governance docs |  |  |  |
| Project map |  |  |  |
| Implementation log |  |  |  |
| Resume marker |  |  |  |
| Risk register |  |  |  |
| Tests |  |  |  |
| CI |  |  |  |
| Deployment |  |  |  |
| Data stores |  |  |  |
| Schema/migrations |  |  |  |
| Backup/sync/cleanup |  |  |  |
| Security/privacy |  |  |  |
| Release process |  |  |  |

## Existing documentation

List existing documentation files and assess whether they are current, stale, missing, or inconsistent.

| Document | Present? | Current? | Notes |
|---|---:|---:|---|
| `README.md` |  |  |  |
| `AGENTS.md` |  |  |  |
| `docs/DOCUMENTATION_POLICY.md` |  |  |  |
| `docs/ROADMAP.md` |  |  |  |
| `docs/PROJECT_MAP.md` |  |  |  |
| `docs/IMPLEMENTATION_LOG.md` |  |  |  |
| `docs/RESUME_MARKER.md` |  |  |  |
| `docs/TESTING_VALIDATION_POLICY.md` |  |  |  |
| `docs/RISK_REGISTER.md` |  |  |  |
| `docs/SECURITY_PRIVACY_POLICY.md` |  |  |  |
| `docs/RELEASE_POLICY.md` |  |  |  |

## High-risk areas

Identify whether the repository contains any of the following:

| Risk area | Present? | Notes | Required control |
|---|---:|---|---|
| Destructive operations |  |  |  |
| Cleanup/deletion/retention logic |  |  |  |
| Database migrations |  |  |  |
| Clinical data handling |  |  |  |
| Financial data handling |  |  |  |
| PII/PHI handling |  |  |  |
| Authentication/authorization |  |  |  |
| Secrets/credentials |  |  |  |
| Backup/sync logic |  |  |  |
| Production services |  |  |  |
| Dashboards/reports |  |  |  |
| CI/CD deployment |  |  |  |

## Data and privacy assessment

Describe:

```text
Data types handled:
Sensitive data present:
Examples or fixtures containing real data:
Secret handling method:
Sanitization gaps:
```

## Test and validation assessment

Describe existing test coverage:

```text
Unit tests:
Integration tests:
Shell tests:
Golden-file tests:
Manual validation:
CI status:
Known test gaps:
```

## Operational assessment

Describe operational elements:

```text
Deployment method:
Runtime services:
Cron/systemd/background jobs:
External dependencies:
Backup and restore process:
Monitoring/logging:
Rollback process:
```

## Preliminary risk classification

Assign the repository or requested tranche an initial risk level:

```text
R0 — Documentation-only
R1 — Low-risk code
R2 — Moderate-risk code
R3 — High-risk code
R4 — Critical-risk code
```

Explain why.

## Governance gaps

List gaps that must be addressed before functional work proceeds.

Examples:

- missing resume marker;
- missing project map;
- stale README;
- no risk register;
- no tests around destructive logic;
- production scripts undocumented;
- data flows not mapped;
- secrets handling unclear.

## Recommended first safe tranche

Propose exactly one first safe tranche.

```text
PHxx-Cx-Txx — Short tranche title
```

Include:

```text
Goal:
Risk level:
Files likely to change:
Tests/validation required:
Rollback notes:
Stop condition:
```

## Future work log

List discovered issues that do not block the first safe tranche.

| Future item | Reason deferred | Suggested tranche |
|---|---|---|
|  |  |  |

## Do not proceed to

State work that must not be attempted until governance or validation improves.

Examples:

- destructive cleanup changes;
- schema migrations;
- production deployment changes;
- authentication changes;
- agent orchestration;
- release automation.

## Assessment closeout

Record:

```text
Assessment completed:
Files changed:
Commands run:
Validation performed:
Known limitations:
Next natural tranche:
Resume marker updated:
```
