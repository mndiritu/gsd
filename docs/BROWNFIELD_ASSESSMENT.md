# Brownfield Assessment

## Assessment identity

```text
Project: Governed Spec-Driven Development
Repository: mndiritu/gsd
Mode: Brownfield governance assessment
Phase: PH00 — Governance Baseline
Component: C10 — Examples / Brownfield Reference Patterns
Workstream: Brownfield assessment scaffold
Tranche: PH00-C10-T01 — Add brownfield assessment scaffold
Risk level: Low
Assessment date: 2026-06-07
```

## Purpose

This document records the brownfield assessment scaffold for applying Governed Spec-Driven Development (GSD) to an existing repository.

It serves two purposes:

1. It closes the current governance gap in the GSD repository, where the brownfield workflow requires `docs/BROWNFIELD_ASSESSMENT.md`.
2. It provides a reference pattern for future brownfield inspections of other repositories.

## Brownfield rule

No functional code changes should occur in a brownfield repository until the repository has been inspected, mapped, risk-assessed, and assigned a safe resume point.

## Repository context

This repository is itself an early-stage GSD toolkit repository.

Current known state:

- foundational governance scaffold exists;
- release-management scaffold exists;
- placeholder CLI exists at `bin/gsd`;
- templates and specs directories exist;
- release policy and release checklist exist;
- implementation log and resume marker are active;
- CLI implementation remains minimal;
- shell test suite is not yet implemented;
- agent orchestration is not implemented;
- Spec Kit bridge is not implemented.

## Required inspection checklist

When applying this assessment to a brownfield repository, inspect:

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

| Area | Current finding | Status |
|---|---|---|
| Root README | Present | Satisfactory for PH00 |
| AGENTS instructions | Present | Satisfactory for PH00 |
| Governance docs | Present | Satisfactory for PH00 |
| Project map | Present | Satisfactory for PH00 |
| Implementation log | Present | Satisfactory for PH00 |
| Resume marker | Present | Satisfactory for PH00 |
| Risk register | Present | Satisfactory for PH00 |
| Release policy | Present and expanded | Satisfactory for PH00 |
| Release checklist | Present | Satisfactory for PH00 |
| Changelog | Present | Satisfactory for PH00 |
| Brownfield assessment | Present after this tranche | Satisfactory for PH00 |
| CLI | Placeholder only | Known limitation |
| Tests | Not yet implemented | Known limitation |
| CI | Not yet assessed or implemented | Future work |
| Packaging | Not yet implemented | Future work |
| Agent orchestration | Not implemented | Future work |
| Spec Kit bridge | Not implemented | Future work |

## Existing documentation

Core documentation expected in a GSD-compliant repository includes:

```text
AGENTS.md
README.md
docs/GOVERNED_SPEC_DRIVEN_DEVELOPMENT.md
docs/DOCUMENTATION_POLICY.md
docs/ROADMAP.md
docs/PROJECT_MAP.md
docs/IMPLEMENTATION_LOG.md
docs/RESUME_MARKER.md
docs/TESTING_VALIDATION_POLICY.md
docs/RISK_REGISTER.md
docs/SECURITY_PRIVACY_POLICY.md
docs/RELEASE_POLICY.md
```

This repository now has the required brownfield assessment artifact as well:

```text
docs/BROWNFIELD_ASSESSMENT.md
```

## Risk areas to identify in future brownfield repositories

A brownfield assessment must explicitly look for:

- destructive operations;
- cleanup, deletion, retention, or archival logic;
- database schema migrations;
- clinical, financial, or personally identifiable data handling;
- production service behavior;
- authentication and authorization;
- secrets and credential handling;
- data synchronization;
- backup verification;
- dashboard/reporting assumptions;
- CI/CD behavior;
- deployment scripts;
- undocumented scripts or cron jobs;
- hidden operational dependencies.

## Preliminary risk assessment for this repository

| Risk area | Current assessment | Action |
|---|---|---|
| Functional code risk | Low at present; CLI is placeholder | Keep CLI changes tranche-scoped |
| Documentation drift | Moderate as doctrine expands | Keep implementation log and resume marker current |
| Release overclaiming | Moderate | Use release policy and checklist |
| Missing shell tests | Moderate before CLI work | Add tests when CLI behavior expands |
| Brownfield process incompleteness | Reduced by this tranche | Maintain this document and template |
| Sensitive data exposure | Low in current docs, but important for examples | Continue fake examples only |

## Governance gaps remaining

Known gaps after this tranche:

- CLI remains a placeholder.
- Shell tests are not yet present.
- CI is not yet implemented.
- Packaging and release automation are not yet implemented.
- Agent orchestration is not implemented.
- Spec Kit bridge is not implemented.
- Brownfield assessment command behavior is not yet implemented in `bin/gsd`.

## Recommended first safe tranches after this assessment

Recommended implementation tranche:

```text
PH01-C6-T01 — Implement minimal gsd init/status CLI commands
```

Possible follow-on governance/tooling tranches:

```text
PH01-C6-T02 — Add gsd inspect command skeleton
PH05-C9-T01 — Add shell smoke tests for gsd CLI
PH00-C10-T02 — Add brownfield example repository scaffold
```

## Do not proceed to

Do not proceed to any of the following until the minimal CLI contract and validation approach are defined:

- agent orchestration;
- Spec Kit bridge implementation;
- package publishing;
- public release automation;
- destructive or high-risk workflow automation.

## Assessment closeout

This assessment is documentation-only.

No functional code was changed.

Validation consists of:

- confirming this required brownfield artifact now exists;
- confirming the assessment is aligned with the brownfield workflow;
- updating the implementation log;
- updating the resume marker.
