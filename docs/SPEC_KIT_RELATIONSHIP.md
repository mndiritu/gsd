# Relationship to Spec Kit

GSD is not a replacement for Spec Kit.

Spec Kit is useful because it structures AI-assisted work around specifications, plans, and tasks rather than one-shot prompting.

GSD adopts that premise and adds mission-critical governance.

## Division of responsibility

| Concern | Spec Kit | GSD |
|---|---|---|
| Specification workflow | Strong | Compatible |
| Feature planning | Strong | Compatible |
| Task generation | Strong | Compatible |
| Project governance | Limited by default | Strong |
| Risk classification | Requires customization | Core requirement |
| Tranche boundaries | Not central | Core requirement |
| Implementation logs | Not central | Core requirement |
| Resume markers | Not central | Core requirement |
| Mission-critical controls | Requires customization | Core requirement |

## Integration principle

Use Spec Kit as the specification engine.

Use GSD as the governance wrapper.

A mature GSD workflow may call or emulate:

```text
constitution → specify → clarify → plan → tasks → analyze/checklist → implement
```

But implementation remains constrained by:

```text
Project → Phase → Component → Workstream → Tranche → Task
```

## Safety catch

No automated implementation command may proceed beyond the approved tranche.

For high-risk work, implementation requires explicit risk acknowledgement, rollback notes, and validation evidence.
