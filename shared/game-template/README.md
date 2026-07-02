# Game Template

Use this folder as the standard checklist for future games.

## Recommended game folder

```text
games/<slug>/
├─ index.html
├─ README.md
├─ metadata.json
├─ TODO.md
├─ CHANGELOG.md
└─ docs/
```

## Minimum metadata

```json
{
  "title": "Game Title",
  "slug": "game-slug",
  "path": "games/game-slug/",
  "genre": "Genre",
  "description": "One-sentence description.",
  "created_by": "Creator / model",
  "spark": "Jaron K. Bragg"
}
```

## Minimum release checklist

- Playable from `index.html`.
- Linked from root `index.html`.
- Added to `games.json`.
- Metadata exists.
- Creator attribution exists.
- Mobile and desktop checked.
