# Clinical Privacy and Safety Rules

## Never include

- real patient names;
- real IDs;
- real dates of birth;
- real clinical records;
- real credentials;
- real production secrets.

## High-risk clinical changes

Treat these as high risk:

- data deletion;
- backup/archive logic;
- database schema migration;
- synchronization;
- patient metadata parsing;
- authentication/authorization;
- production deployment;
- dashboard metrics that may create false reassurance.
