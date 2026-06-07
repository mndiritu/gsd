# Testing and Validation Policy

## Purpose

GSD requires validation evidence proportional to risk.

## Risk levels

| Risk | Meaning | Minimum validation |
|---|---|---|
| Low | Docs/templates only | Readback, lint where applicable |
| Medium | CLI behavior, generated files | Shell tests, dry run, idempotency check |
| High | Destructive actions, production, sensitive data | Explicit preflight, rollback, dry run, test evidence |
| Critical | Clinical/financial/infrastructure safety impact | Human approval, staged rollout, audit trail |

## Required checks for this repo

- Shell scripts must use `set -Eeuo pipefail`.
- CLI commands must support dry run before destructive behavior.
- Existing files must not be overwritten unless forced.
- Generated templates must be idempotent.
- Agent instructions must prohibit uncontrolled implementation.

## Future validation

Add shell tests under:

```text
tests/shell/
tests/golden-files/
```
