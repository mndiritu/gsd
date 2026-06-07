# Governed Spec-Driven Development

Governed Spec-Driven Development, or GSD, is a governance-first workflow for AI-assisted software development in mission-critical environments.

GSD is not a replacement for Spec Kit. It is a mission-specific extension and companion pattern for specification-driven development. Spec Kit helps move from intent to specification, planning, tasks, and implementation. GSD adds the controls required when AI agents are working on clinical, financial, infrastructure, public-health, or other high-accountability systems:

- project map;
- phase/component/tranche classification;
- explicit risk rating;
- validation evidence;
- implementation log;
- resume marker;
- anti-sprawl controls;
- agent-readable instructions.

The short rule:

> No AI coding action may begin until it is specified, located in the project map, scoped into a tranche, risk-rated, tied to validation evidence, and assigned a resume marker.

## Repository status

Current phase:

```text
PH00-C1-T01 — Create foundational GSD repository scaffold
```

This repository is being initialized as the canonical home for reusable GSD doctrine, templates, prompts, agent instructions, and future CLI tooling.

## Core files

```text
AGENTS.md
docs/
  GOVERNED_SPEC_DRIVEN_DEVELOPMENT.md
  WHY_GSD.md
  SPEC_KIT_RELATIONSHIP.md
  GREENFIELD_WORKFLOW.md
  BROWNFIELD_WORKFLOW.md
  DOCUMENTATION_POLICY.md
  ROADMAP.md
  PROJECT_MAP.md
  IMPLEMENTATION_LOG.md
  RESUME_MARKER.md
  TESTING_VALIDATION_POLICY.md
  RISK_REGISTER.md
  SECURITY_PRIVACY_POLICY.md
  RELEASE_POLICY.md
templates/
  base/
  specs/
  agents/
  domains/
specs/
  README.md
bin/
  gsd
```

## Intended usage

Greenfield project:

```bash
gsd init --mode greenfield --domain clinical --agent codex
```

Brownfield project:

```bash
gsd inspect --mode brownfield --agent codex
```

Feature workflow:

```bash
gsd new-feature "Verify S3 archive existence before cleanup" --risk high
gsd tranche specs/001-verify-s3-archive-existence-before-cleanup
gsd preflight PH05-C5-T02
gsd close PH05-C5-T02
```

The first version of this repository focuses on doctrine and templates. The CLI will initially scaffold and guide work; later versions may orchestrate AI agents directly.
