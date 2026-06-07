# Risk Register

| Risk ID | Risk | Impact | Mitigation | Status |
|---|---|---|---|---|
| R001 | Agents implement before governance scaffold exists | Scope drift, unsafe changes | Require AGENTS.md and resume marker | Open |
| R002 | Existing files overwritten by bootstrapper | Data loss | Default no-overwrite; require `--force` | Open |
| R003 | High-risk domains use generic templates | Missing safety controls | Domain presets | Open |
| R004 | Spec Kit integration treated as replacement for GSD | Governance gaps | Document relationship clearly | Open |
| R005 | Chat reasoning not captured in repo | Lost operational memory | Implementation log and resume marker | Open |
| R006 | Release made before CLI contract is stable | False assurance and premature adoption | Use pre-release versioning and require release checklist completion | Open |
| R007 | Version tags drift from documented release state | Confusion about implemented capability | Require changelog, implementation log, and resume marker alignment before tagging | Open |
| R008 | Templates or examples released with sensitive or real-world data | Privacy, confidentiality, or security exposure | Require security/privacy review and fake example values only | Open |
| R009 | Release notes overstate implemented capabilities | Users rely on non-existent functionality | Require explicit known limitations and validation evidence in release notes | Open |
| R010 | Brownfield repository changed before assessment is complete | Existing risks are missed and unsafe changes proceed | Require brownfield assessment, project map, risk register, implementation log, and resume marker before functional work | Open |
| R011 | Brownfield inspection misses destructive or production-sensitive logic | Data loss, service disruption, or unsafe automation | Require explicit inspection of deletion, cleanup, backup, sync, migration, auth, production, and sensitive-data paths | Open |
| R012 | Brownfield project map is guessed rather than grounded in repository evidence | Work is scoped to the wrong component or tranche | Require repository readback and evidence-based component mapping | Open |
