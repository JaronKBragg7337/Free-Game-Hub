# Game Metadata Schema

Every game in Free Game Hub should include a `metadata.json` file beside its `index.html`.

## Required fields

```json
{
  "title": "The Loop",
  "slug": "the-loop",
  "path": "games/the-loop/",
  "genre": "Systems Strategy",
  "description": "Balance connected systems for as long as the loop can hold.",
  "created_by": {
    "type": "AI",
    "name": "ChatGPT Chat 5.5"
  },
  "spark": {
    "name": "Jaron K. Bragg",
    "role": "Original idea / direction"
  },
  "version": "0.2.0",
  "status": "prototype",
  "license": "MIT"
}
```

## Creator naming convention

Use the exact tool or person name whenever possible.

Examples:

- `ChatGPT Chat 5.5`
- `ChatGPT Codex 5.5`
- `Claude Chat Sonnet 5 High`
- `Claude Chat Fable 5 High`
- `Claude Chat Opus 4.8`
- `Claude Code`
- `Claude Cowork`
- `Jaron K. Bragg`
- `Kurtis Bragg`

## Spark field

The `spark` field records who originated the idea, prompt, mechanic, or creative direction. The creator field records who produced the current artifact.

A game can therefore be:

```text
Created by: ChatGPT Chat 5.5
Spark: Jaron K. Bragg
```

or:

```text
Created by: Hazel Bragg
Spark: Hazel Bragg
```

## Contributors

For multi-stage projects, add a contributors list:

```json
"contributors": [
  {
    "name": "ChatGPT Codex 5.5",
    "role": "Local implementation pass",
    "date": "2026-07-02"
  },
  {
    "name": "Claude Code",
    "role": "Refactor and bug fix pass",
    "date": "2026-07-04"
  }
]
```
