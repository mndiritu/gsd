# Testing and Validation Policy

## Risk levels

| Risk | Meaning | Minimum validation |
|---|---|---|
| Low | Docs/templates | Readback |
| Medium | CLI/generated files | Tests and dry run |
| High | Sensitive/destructive/production | Explicit preflight and rollback |
| Critical | Mission-critical safety | Human approval and audit trail |
