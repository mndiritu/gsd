# Release Policy

## Current status

Pre-release.

The repository is still in governance and CLI bootstrap. Public releases should not claim production readiness, agent orchestration, or Spec Kit integration until those capabilities are implemented and validated.

## Release authority

A release may only be prepared inside an approved GSD tranche.

Release work must be classified by:

```text
Project
Phase
Component
Workstream
Tranche
Risk level
Files changed
Validation evidence
Resume marker
```

For this repository, release-management work belongs primarily under:

```text
PH00 — Governance Baseline
C11 — Release Management
```

Later implementation releases may belong under the relevant implementation component, but they must still satisfy this release policy.

## Versioning

Use semantic versioning once the CLI has a stable public contract:

```text
MAJOR.MINOR.PATCH
```

Before that point, use `0.x.y` pre-release versions.

Recommended interpretation:

```text
0.0.x  Governance scaffold and documentation-only milestones
0.1.x  Minimal local CLI bootstrap commands
0.2.x  Template generation and idempotent scaffold behavior
0.3.x  Brownfield inspection support
0.4.x  Agent adapter prototypes
1.0.0  Stable CLI contract, validated templates, and documented release process
```

## Changelog requirement

Every release must update `CHANGELOG.md`.

The changelog must distinguish:

- added capabilities;
- changed behavior;
- fixed defects;
- documentation-only updates;
- known limitations;
- unreleased work that must not be advertised as complete.

## Release checklist

Before any tagged release, use:

```text
docs/RELEASE_CHECKLIST.md
```

A release must not proceed unless the checklist is complete or any unchecked item is explicitly explained in the release notes.

## Release requirements

Before a release:

- implementation log updated;
- resume marker updated;
- changelog updated;
- release checklist completed;
- shell tests pass where tooling is involved;
- generated scaffold reviewed where templates are involved;
- documentation examples sanitized;
- known risks reviewed;
- stop conditions checked.

## Validation requirements by release type

### Documentation-only release

Minimum validation:

- readback verification;
- path/link review where applicable;
- consistency check against `AGENTS.md`, `docs/PROJECT_MAP.md`, `docs/RISK_REGISTER.md`, and `docs/RESUME_MARKER.md`.

### CLI or tooling release

Minimum validation:

- shell test or smoke command;
- dry-run verification where applicable;
- no unintended overwrite of existing files;
- idempotency check for scaffold generation;
- implementation log evidence.

### Template or scaffold release

Minimum validation:

- generated output reviewed;
- fake values only;
- no secrets, PHI/PII, private hostnames, or production-sensitive examples;
- templates align with the required GSD hierarchy.

### Agent adapter or orchestration release

Minimum validation:

- explicit scope boundary;
- stop conditions defined;
- agent instructions confirm no uncontrolled implementation;
- validation evidence recorded;
- high-risk actions disabled by default unless explicitly approved.

## Tagging policy

Use annotated tags for public releases once releases begin.

Recommended tag format:

```text
vMAJOR.MINOR.PATCH
```

Example:

```text
v0.1.0
```

A tag must point to a commit where:

- `CHANGELOG.md` includes the release entry;
- `docs/IMPLEMENTATION_LOG.md` records the release tranche;
- `docs/RESUME_MARKER.md` identifies the safe resume point;
- known release risks are reviewed.

## Release notes policy

Release notes must state:

- what changed;
- what is validated;
- what remains unimplemented;
- known risks or limitations;
- whether the release is documentation-only, pre-release, or stable;
- the next natural tranche.

Release notes must not claim capability beyond the repository state.

## Artifact policy

Do not publish packaged artifacts until packaging behavior is itself governed by a tranche.

When artifacts are introduced, each artifact must have:

- source commit SHA;
- version tag;
- generation command;
- validation evidence;
- rollback or replacement guidance.

## Stop conditions

Do not release if:

- governance files are missing or inconsistent;
- the resume marker is stale;
- the implementation log does not record the release tranche;
- validation evidence is missing for the risk level;
- examples contain secrets, credentials, PHI/PII, or confidential production data;
- CLI behavior changed without at least smoke validation;
- release notes overstate implemented capability.

## Current release posture

The project is not yet ready for a public stable release.

The next release-management target is to maintain a clean pre-release scaffold until the minimal CLI contract is defined and validated.
