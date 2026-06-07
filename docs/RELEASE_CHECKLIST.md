# Release Checklist

Use this checklist before any tagged release, packaged artifact, or public distribution of the GSD toolkit.

## 1. Release identity

- [ ] Release version selected.
- [ ] Release type identified:
  - [ ] documentation-only;
  - [ ] CLI/tooling;
  - [ ] template or scaffold;
  - [ ] adapter or integration;
  - [ ] domain preset;
  - [ ] security/privacy hardening.
- [ ] Release tranche recorded in `docs/IMPLEMENTATION_LOG.md`.
- [ ] `docs/RESUME_MARKER.md` updated.
- [ ] `CHANGELOG.md` updated.

## 2. Governance preflight

- [ ] Current resume marker reviewed.
- [ ] Release work mapped to `docs/PROJECT_MAP.md`.
- [ ] Risk level assigned.
- [ ] Files changed are limited to the approved tranche.
- [ ] New discovered issues are logged as future work unless they block release.
- [ ] No unrelated fixes included.

## 3. Validation evidence

For documentation-only releases:

- [ ] Documentation readback completed.
- [ ] Internal links and paths checked where applicable.
- [ ] Examples reviewed for consistency.

For CLI/tooling releases:

- [ ] Shell tests run.
- [ ] CLI help/status smoke tests run.
- [ ] Dry-run behavior verified where applicable.
- [ ] Existing files are not overwritten unless explicitly forced.
- [ ] Generated scaffold behavior is idempotent or exceptions are documented.

For high-risk or mission-critical presets:

- [ ] Security/privacy policy reviewed.
- [ ] No real PHI/PII, credentials, hostnames, or confidential production details included.
- [ ] Rollback or recovery notes documented.
- [ ] Human review completed where required.

## 4. Security and privacy review

- [ ] No API keys, tokens, passwords, private SSH keys, or database URLs with credentials.
- [ ] No patient-identifiable, client-identifiable, or confidential production data.
- [ ] Example values are fake and clearly marked as examples.
- [ ] Documentation screenshots, logs, and examples are sanitized.

## 5. Release artifacts

- [ ] Git tag planned or created.
- [ ] GitHub release notes drafted if releasing publicly.
- [ ] Packaged artifact produced only if packaging is part of the approved tranche.
- [ ] Generated scaffold reviewed.
- [ ] Known risks reviewed and either accepted or converted into blocking work.

## 6. Stop conditions

Do not release if any of the following apply:

- governance files are missing or internally inconsistent;
- resume marker is stale;
- implementation log does not describe the release tranche;
- validation evidence is missing for the risk level;
- examples contain sensitive or real-world confidential data;
- CLI behavior is changed without tests or smoke validation;
- release notes claim capability that is not implemented.

## 7. Closeout

- [ ] Implementation log updated.
- [ ] Resume marker updated.
- [ ] Changelog updated.
- [ ] Release policy reviewed.
- [ ] Risk register reviewed.
- [ ] Next natural tranche identified.
- [ ] Explicit `Do not proceed to` boundary recorded.
