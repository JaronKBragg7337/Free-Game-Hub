# Free Game Hub

Free browser games that respect players.

**No ads. No accounts. No downloads. No tracking.**

**Play:** https://jaronkbragg7337.github.io/Free-Game-Hub/

Free Game Hub is a living collection of browser-first games built by people and AI. Every contributor owns its work, every game records its lineage, and the repository grows one playable experience at a time.

---

## Public pages

- **Hub:** https://jaronkbragg7337.github.io/Free-Game-Hub/
- **Creators:** https://jaronkbragg7337.github.io/Free-Game-Hub/creators/
- **Game catalog:** `games.json`
- **Creator catalog:** `creators/index.json`

---

## Current games

| Game | Path | Genre | Created by | Spark |
|---|---|---|---|---|
| TRACE | `/trace/` | Daily Puzzle | Claude Chat Sonnet 5 High | Jaron K. Bragg |
| Roll & Reach | `/games/roll-and-reach/` | 3D Puzzle | Claude Chat Fable 5 High | Jaron K. Bragg |
| The Loop | `/games/the-loop/` | Systems Strategy | ChatGPT Chat 5.5 | Jaron K. Bragg |
| FLUX | `/games/flux/` | Emergent Sandbox | Grok • Grok 4 | Jaron K. Bragg |

---

## Repository map

```text
/
├─ index.html                    # public hub page
├─ games.json                    # canonical game catalog
├─ creators/
│  ├─ index.html                 # public creator page
│  └─ index.json                 # canonical creator catalog
├─ games/                        # standard playable game folders
│  ├─ flux/
│  ├─ roll-and-reach/
│  └─ the-loop/
├─ trace/                        # legacy/root-level playable game folder
├─ contributors/                 # primary contributor workspaces
│  ├─ openai/
│  ├─ anthropic/
│  ├─ xai/
│  ├─ google/
│  ├─ perplexity/
│  └─ future-ai/
├─ shared/
│  ├─ standards/
│  ├─ game-template/
│  └─ assets/
├─ docs/
│  ├─ AI_WORKFLOW.md
│  └─ GAME_METADATA_SCHEMA.md
└─ ai/                           # legacy compatibility workspaces
```

`contributors/` is the primary structure going forward. `ai/` is retained for older handoff notes and compatibility.

---

## Contributor structure

Every AI model, person, or contributor should have a workspace under `contributors/`.

Recommended structure:

```text
contributors/<company-or-person>/<model-or-name>/
├─ README.md
├─ TODO.md
├─ CHANGELOG.md
├─ IDEAS.md
├─ WORKLOG.md
├─ SHARED/
└─ GAMES/
```

Examples:

```text
contributors/openai/chatgpt-5.5/
contributors/openai/codex-5.5/
contributors/anthropic/sonnet-5-high/
contributors/anthropic/fable-5-high/
contributors/anthropic/opus-4.8/
contributors/xai/grok-4/
contributors/perplexity/<model-name>/
contributors/google/<model-name>/
```

If an AI does not know its exact model name, it should ask for the model/folder name before creating a workspace.

---

## Game folder standard

Most games should live under:

```text
games/<game-slug>/
```

Recommended files:

```text
games/<game-slug>/
├─ index.html
├─ README.md
├─ metadata.json
├─ TODO.md
├─ CHANGELOG.md
└─ docs/
```

`index.html` should be playable directly from GitHub Pages.

---

## Provenance standard

Every game should record:

```text
Created by: <AI/model/person>
Spark: <originator>
```

Example:

```text
Created by: ChatGPT Chat 5.5
Spark: Jaron K. Bragg
```

This should appear in:

1. `games.json`
2. the game's `metadata.json`
3. the public hub card when practical
4. the game README or changelog when the build history matters

If a later model repairs or publishes another model's incomplete work, preserve the original creator and add the repair/publish pass as a contributor or note. Do not erase lineage.

---

## Ownership and continuation rule

Each contributor owns its own games.

A game may be continued by:

1. the same model,
2. another model from the same AI company/family,
3. or a different contributor only if explicitly requested.

Examples:

- OpenAI-created games may be continued by ChatGPT, Codex, or future OpenAI models.
- Anthropic-created games may be continued by Claude chat/code/cowork models.
- xAI-created games may be continued by Grok/xAI models.
- Human-created games may be continued according to the human creator's direction.

This is not a competition system. It is a provenance system.

---

## Add a new game

1. Pull the latest repository.
2. Confirm or create the contributor workspace under `contributors/`.
3. Create the game folder under `games/<slug>/`.
4. Add a playable `index.html`.
5. Add `README.md`, `metadata.json`, `TODO.md`, and `CHANGELOG.md`.
6. Add an entry to `games.json`.
7. Add or update the homepage card in `index.html`.
8. Add or update the creator entry in `creators/index.json` and `/creators/index.html`.
9. Update contributor `CHANGELOG.md` and `TODO.md`.
10. Verify the files exist on `main` before reporting success.

---

## Release checklist

Before reporting that a game is published, verify:

- The commit exists on `main`.
- The game folder exists.
- The game has a real playable `index.html`, not placeholder text.
- The game is listed in `games.json`.
- The homepage links to the game.
- Metadata records `Created by` and `Spark`.
- Mobile and desktop layouts are reasonable.
- There are no obvious console-breaking syntax errors.

See `shared/standards/REPOSITORY_VERIFICATION.md`.

---

## Ground rules

1. Free forever.
2. No ads.
3. No accounts unless explicitly required for a future feature.
4. No tracking or analytics by default.
5. Static/browser-first games are preferred.
6. Player data should stay local unless the game explicitly needs shared data.
7. Preserve creator/spark provenance.
8. Preserve handoff context when a game spans multiple sessions.
9. Use the simplest technology that can deliver the intended experience.
10. Leave the repository in a better state than you found it.

---

## Deployment

This repository is deployed through GitHub Pages from:

```text
main / root
```

Public URL:

```text
https://jaronkbragg7337.github.io/Free-Game-Hub/
```

No build step is required for the current hub.

---

## License

MIT unless a specific game folder states otherwise.
