# Free Game Hub

Free browser games that respect you. **No ads. No accounts. No downloads. No tracking.** Open source, forever.

**Play:** https://jaronkbragg7337.github.io/Free-Game-Hub/

---

## Current structure

```text
/
├─ index.html
├─ games.json
├─ docs/
│  ├─ AI_WORKFLOW.md
│  └─ GAME_METADATA_SCHEMA.md
├─ ai/
│  ├─ chatgpt-chat-5-5/
│  ├─ chatgpt-codex-5-5/
│  ├─ external-ai-sonnet-high/
│  ├─ external-ai-fable-high/
│  ├─ external-ai-opus-4-8/
│  ├─ external-ai-code/
│  └─ external-ai-cowork/
├─ trace/
│  ├─ index.html
│  ├─ metadata.json
│  ├─ TODO.md
│  └─ LOG.md
└─ games/
   ├─ roll-and-reach/
   │  ├─ index.html
   │  ├─ README.md
   │  ├─ metadata.json
   │  ├─ TODO.md
   │  └─ LOG.md
   └─ the-loop/
      ├─ index.html
      ├─ README.md
      ├─ metadata.json
      ├─ TODO.md
      └─ LOG.md
```

---

## Games

### TRACE — a daily path puzzle
`/trace/`

A path of six connected squares hides in a 6×6 chart. You know where it starts. Trace a guess, hit **Ping**, and read the echoes.

**Created by:** Claude Chat Sonnet 5 High  
**Spark:** Jaron K. Bragg

### Roll & Reach — a daily 3D block puzzle
`/games/roll-and-reach/`

Roll a 1×1×2 block across a generated board and stand it on the glowing goal tile in as few moves as possible.

**Created by:** Claude Chat Fable 5 High  
**Spark:** Jaron K. Bragg

### The Loop — systems strategy prototype
`/games/the-loop/`

Balance energy, industry, research, society, and ecology for as long as the loop can hold.

**Created by:** ChatGPT Chat 5.5  
**Spark:** Jaron K. Bragg

---

## Provenance standard

Every game should record:

```text
Created by: <AI/model/person>
Spark: <originator>
```

This is recorded in:

1. `games.json`
2. each game's `metadata.json`
3. the hub card when appropriate
4. each game's README/log when the build history matters

See:

- `docs/GAME_METADATA_SCHEMA.md`
- `docs/AI_WORKFLOW.md`

---

## Add another game

1. Create a new folder:
   ```text
   games/new-game-slug/
   ```
2. Put the game at:
   ```text
   games/new-game-slug/index.html
   ```
3. Add:
   ```text
   metadata.json
   TODO.md
   LOG.md
   ```
4. Add a card to the root `index.html`.
5. Add an entry to `games.json`.
6. Update the relevant AI workspace under `ai/`.
7. Commit and push.

---

## Deploy with GitHub Pages

1. Push these files to the `main` branch.
2. Go to **Settings → Pages**.
3. Set **Source** to **Deploy from a branch**.
4. Set **Branch** to **main** and folder to **/(root)**.
5. Save.

The hub publishes at:

```text
https://jaronkbragg7337.github.io/Free-Game-Hub/
```

---

## Ground rules

1. Free forever.
2. No ads.
3. No accounts.
4. No tracking or analytics.
5. Static files only where possible.
6. Player data stays in the player's browser.
7. Preserve creator/spark provenance.
8. Preserve handoff context when a game spans multiple AI sessions.

## License

MIT.
