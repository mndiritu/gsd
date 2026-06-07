# Governed Spec-Driven Development

## Definition

Governed Spec-Driven Development, or GSD, is a mission-critical extension of specification-driven development for AI-assisted software projects.

It uses AI agents to help inspect, specify, plan, implement, validate, and document software, but it constrains that work inside a governance structure:

```text
Project
└── Phase
    └── Component
        └── Workstream
            └── Tranche
                └── Task / Commit / Test / Documentation update
```

## One-sentence rule

No AI coding action may begin until it is specified, located in the project map, scoped into a tranche, risk-rated, tied to validation evidence, and assigned a resume marker.

## Why GSD exists

AI-assisted development has made software creation faster than traditional governance habits can safely absorb.

In ordinary projects, this creates maintainability problems.

In mission-critical systems, it creates safety, privacy, operational, legal, financial, and accountability risks.

GSD preserves the speed and creativity of AI-assisted development while adding:

- project mapping;
- phased work;
- tranche boundaries;
- risk classification;
- validation evidence;
- implementation logging;
- resume markers;
- anti-sprawl controls.

## Relationship to Spec Kit

GSD is not a replacement for Spec Kit.

Spec Kit is a specification engine. GSD is a mission-critical governance wrapper.

Spec Kit helps move from:

```text
constitution → specify → clarify → plan → tasks → analyze/checklist → implement
```

GSD adds:

```text
project map → phase → component → workstream → tranche → risk gate → validation evidence → implementation log → resume marker
```

GSD can run standalone, wrap Spec Kit, generate Spec Kit-compatible artifacts, or feed any AI coding agent.

## Greenfield mode

For a new project, GSD should:

1. create the governance scaffold;
2. draft project constitution;
3. define initial project map;
4. define phases and components;
5. create testing and validation policy;
6. create risk model;
7. create the first feature specification;
8. clarify ambiguities;
9. create plan;
10. generate tasks;
11. convert tasks into tranches;
12. implement only the first approved tranche;
13. validate;
14. log;
15. update resume marker.

## Brownfield mode

For an existing repository, GSD should:

1. inspect the repository;
2. identify existing docs, tests, CI, deployment scripts, data flows, and risk areas;
3. determine whether a documentation policy exists;
4. determine whether a project/component map exists;
5. determine whether implementation logs and resume markers exist;
6. create a brownfield assessment;
7. propose governance scaffold changes;
8. refuse functional code changes until the resume point and risk map are clear.

## Tranche naming

Use:

```text
PHxx-Cx-Txx — Short human-readable tranche name
```

Example:

```text
PH05-C5-T02 — Verify S3 archive existence before local cleanup
```

## End-of-tranche closeout

Every tranche must end with:

- implementation log update;
- resume marker update;
- validation evidence;
- next natural step;
- known risks or unresolved issues.
