# Security and Privacy Policy

## Core rule

Do not place secrets, credentials, tokens, patient-identifiable data, client-identifiable data, or production-sensitive details in prompts, logs, screenshots, examples, tests, or documentation.

## Prohibited content

- API keys
- passwords
- private SSH keys
- database URLs with credentials
- access tokens
- PHI/PII
- real patient identifiers
- confidential production hostnames unless required and approved

## Template examples

Use fake values only.

Good:

```text
patient_id: EXAMPLE_PATIENT_001
database_url: postgres://example_user:example_password@example-host/example_db
```

Bad:

```text
real names, real IDs, real credentials, real clinical records
```

## Agent rule

Agents must stop and ask for sanitization if user-provided content appears to contain secrets or identifiable clinical information.
