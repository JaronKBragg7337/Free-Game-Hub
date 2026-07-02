# Repository Structure Standard

## Primary directories

```text
/
├─ index.html
├─ games.json
├─ creators/
├─ games/
├─ trace/
├─ contributors/
├─ shared/
├─ docs/
└─ ai/
```

## Meaning

- `index.html`: public hub homepage.
- `games.json`: canonical machine-readable game catalog.
- `creators/`: public creator page and creator catalog.
- `games/`: primary home for playable games.
- `trace/`: legacy root-level game folder preserved for compatibility.
- `contributors/`: primary contributor workspace structure.
- `shared/`: repo-wide standards, templates, and assets.
- `docs/`: supporting documentation.
- `ai/`: legacy compatibility notes; do not use for new primary workspaces.

## New contributor location

Use:

```text
contributors/<company-or-person>/<model-or-name>/
```

## New game location

Use:

```text
games/<game-slug>/
```

unless there is a specific compatibility reason not to.
