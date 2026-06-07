# Why GSD Exists

AI coding agents are fast. That is useful. It is also dangerous when speed outruns context, governance, testing, and operational memory.

GSD exists to prevent AI-assisted development from becoming uncontrolled implementation by chat transcript.

## Problems GSD addresses

- AI agents may make plausible local changes that violate broader architecture.
- Agents may implement before ambiguity is resolved.
- Work may sprawl into unrelated files or components.
- Risk may be hidden until after code is changed.
- Test evidence may be vague or absent.
- Important reasoning may remain trapped in a chat session.
- The next human or AI agent may not know where to resume.

## What GSD requires

Before work begins:

- locate the work in the project map;
- define phase, component, workstream, tranche, and task;
- assign risk level;
- define expected files affected;
- define tests or validation;
- identify documentation updates;
- state rollback considerations where relevant.

After work ends:

- log what changed;
- record commands and tests;
- state what passed and failed;
- update the resume marker;
- identify the next natural tranche.

## Target domains

GSD is especially useful for:

- clinical systems;
- public health systems;
- financial systems;
- infrastructure software;
- data pipelines;
- backup and archive systems;
- systems involving deletion, sync, schema changes, or confidential data.
