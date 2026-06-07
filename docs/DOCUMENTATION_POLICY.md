# Documentation Policy

## Purpose

This project uses documentation as operational memory.

Every feature, bug fix, refactor, documentation change, CLI change, template change, or agent instruction change must be placed inside the governance hierarchy before work begins.

## Hierarchy

```text
Project
└── Phase
    └── Component
        └── Workstream
            └── Tranche
                └── Task / Commit / Test / Documentation update
```

## Required classification

Each tranche must document:

- phase;
- component;
- workstream;
- tranche ID;
- branch;
- goal;
- files likely to change;
- risk or blast radius;
- tests required;
- documentation updates required;
- rollback considerations;
- resume marker.

## Required end-of-tranche updates

At the end of each tranche, update:

- `docs/IMPLEMENTATION_LOG.md`
- `docs/RESUME_MARKER.md`
- affected templates/specs/docs.

## Anti-sprawl rule

If new work is discovered, classify it and log it as future work unless it blocks the current tranche.
