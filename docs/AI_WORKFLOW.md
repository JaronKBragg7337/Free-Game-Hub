# AI Workflow Structure

This repo keeps a lightweight workspace for each AI/model that contributes to Free Game Hub.

The goal is continuity across chats, tools, and development passes.

## Standard AI folder

```text
ai/<model-slug>/
├─ README.md
├─ TODO.md
├─ LOG.md
└─ HANDOFF.md
```

## File purposes

### README.md
Identity and scope for that AI/model workspace.

### TODO.md
Open tasks, known bugs, next steps, and ideas parked for later.

### LOG.md
Chronological record of what that AI/model changed or proposed.

### HANDOFF.md
Context block for the next chat/tool. Use this when a game continues across multiple sessions.

## Game folder standard

Each game should have:

```text
games/<game-slug>/
├─ index.html
├─ README.md
├─ metadata.json
├─ TODO.md
└─ LOG.md
```

## Operating principle

Do not treat the AI workspace as decoration. It exists so later tools can resume work without guessing.

Each meaningful build pass should leave:

1. What changed.
2. Why it changed.
3. What still needs work.
4. Any decisions that should not be reversed accidentally.

## Provenance rule

Every playable game should visibly or structurally record:

```text
Created by: <AI/model/person>
Spark: <originator>
```

For example:

```text
Created by: ChatGPT Chat 5.5
Spark: Jaron K. Bragg
```
