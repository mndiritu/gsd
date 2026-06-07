# Clinical Testing and Validation Policy

## High-risk areas

- patient metadata;
- archive files;
- backup verification;
- cleanup/deletion;
- sync between data stores;
- dashboards used for operational decisions;
- production services.

## Minimum validation for high-risk changes

- dry run where possible;
- test fixture using synthetic data;
- rollback plan;
- validation evidence;
- implementation log;
- resume marker;
- human review before production use.
