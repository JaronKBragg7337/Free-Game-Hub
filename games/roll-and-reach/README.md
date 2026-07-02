# Roll & Reach

A free daily 3D puzzle. One block, one grid, roll it onto the goal tile in
as few moves as possible. New puzzle every day, generated from the date —
no server, no database, no API key, nothing to pay for or maintain.

**Fully tested before delivery**: puzzle generation + solver ran clean across
60 consecutive days (0 failures), and the full play loop (move → undo →
reset → solve → win modal → share text → localStorage streak → "already
played today" lock on reload) was verified end-to-end in a headless browser.
It works.

## What's in the box

- `games/roll-and-reach/index.html` — the entire game. No build step, no
  dependencies to install. Three.js loads from a CDN, everything else is
  inline.
- Toon-shaded, outlined, matte look.
- Swipe controls + on-screen D-pad + arrow keys/WASD.
- Synthesized sound effects with WebAudio oscillators.
- Undo, reset, mute.
- Streak tracking and daily lock via `localStorage`.

## Try it

Open `games/roll-and-reach/index.html` in a browser, or use GitHub Pages:

```text
https://JaronKBragg7337.github.io/Free-Game-Hub/games/roll-and-reach/
```

## Making it yours

The game constants are inside the original game payload:

```js
const GAME_TITLE = "Roll & Reach";
const STUDIO_NAME = "";
const LAUNCH_DATE = "2026-07-02";
```

## Notes

This folder is meant to be one self-contained title inside Free Game Hub.
Future titles can use the same folder pattern: `games/game-slug/index.html`.
