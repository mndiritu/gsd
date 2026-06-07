# Agent Instructions: Governed Spec-Driven Development

This repository uses Governed Spec-Driven Development.

AI agents may assist with inspection, specification, planning, task decomposition, implementation, validation, and documentation. They must not make uncontrolled code changes.

## Required reading order

Before changing code or project structure, inspect:

1. `README.md`
2. `AGENTS.md`
3. `docs/GOVERNED_SPEC_DRIVEN_DEVELOPMENT.md`
4. `docs/DOCUMENTATION_POLICY.md`
5. `docs/ROADMAP.md`
6. `docs/PROJECT_MAP.md`
7. `docs/IMPLEMENTATION_LOG.md`
8. `docs/RESUME_MARKER.md`
9. `docs/TESTING_VALIDATION_POLICY.md`
10. `docs/RISK_REGISTER.md`

If these files are missing, propose or create the missing governance scaffold before changing functional code.

## Required work classification

Every work item must be classified as:

```text
Project:
Phase:
Component:
Workstream:
Tranche:
Task:
Branch:
Risk level:
Files likely to change:
Tests required:
Documentation updates required:
Rollback plan:
Resume marker:
```

Use tranche names in this format:

```text
PHxx-Cx-Txx — Short human-readable tranche name
```

Example:

```text
PH05-C5-T02 — Verify S3 archive existence before local cleanup
```

## Implementation rules

Do not begin implementation until:

- the current resume marker has been read;
- the work is mapped to the project map;
- the tranche is named;
- risk level is assigned;
- tests or validation checks are defined;
- documentation updates are identified;
- rollback considerations are stated for high-risk work.

Implement only the approved tranche.

## Anti-sprawl rule

Do not expand scope casually.

If a new issue is discovered:

1. Decide whether it blocks the current tranche.
2. If it does not block the current tranche, log it as future work.
3. Do not fix unrelated issues in the same tranche.

## Mission-critical safety rule

For clinical, financial, infrastructure, deletion, backup, sync, authentication, authorization, schema, production-service, or personally identifiable data changes, treat work as high risk unless proven otherwise.

High-risk work requires:

- explicit scope;
- rollback plan;
- dry run where possible;
- test evidence;
- implementation log update;
- resume marker update.

## End-of-tranche closeout

At the end of every tranche, update:

- `docs/IMPLEMENTATION_LOG.md`
- `docs/RESUME_MARKER.md`
- affected spec files;
- affected project documentation.

The closeout must state:

- what was done;
- why it was done;
- files changed;
- commands run;
- tests run;
- what passed;
- what failed or remains uncertain;
- current safe state;
- next natural tranche.
