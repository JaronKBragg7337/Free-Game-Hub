# Free Game Hub

Free browser games that respect you. **No ads. No accounts. No downloads. No tracking.** Open source, forever.

**Play:** https://jaronkbragg7337.github.io/Free-Game-Hub/

---

## Current structure

```text
/
├─ index.html
├─ trace/
│  └─ index.html
└─ games/
   └─ roll-and-reach/
      ├─ index.html
      └─ README.md
```

---

## Games

### TRACE — a daily path puzzle
`/trace/`

A path of six connected squares hides in a 6×6 chart. You know where it starts. Trace a guess, hit **Ping**, and read the echoes.

Features:
- Daily deterministic puzzle
- Five guesses
- Streaks, stats, archive, and practice mode
- Single HTML file
- No backend, accounts, ads, analytics, or tracking

### Roll & Reach — a daily 3D block puzzle
`/games/roll-and-reach/`

Roll a 1×1×2 block across a generated board and stand it on the glowing goal tile in as few moves as possible.

Features:
- Daily generated 3D puzzle
- Practice mode
- Streak tracking and daily lock
- Undo, reset, mute, share result
- Three.js from CDN; no build step
- Local-only save data

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
3. Add a card to the root `index.html`:
   ```html
   <a class="card" href="games/new-game-slug/">
     <div class="top">
       <h2>NEW GAME</h2>
       <span class="genre">GENRE</span>
     </div>
     <p>One-sentence description.</p>
     <span class="play">▶ PLAY NEW GAME</span>
   </a>
   ```
4. Commit and push.

---

## Deploy with GitHub Pages

1. Push these files to the `main` branch.
2. Go to **Settings → Pages**.
3. Set **Source** to **Deploy from a branch**.
4. Set **Branch** to **main** and folder to **/(root)**.
5. Save.

The hub will publish at:

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

## License

MIT.
