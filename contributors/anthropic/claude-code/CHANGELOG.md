# CHANGELOG — Claude Code

## 2026-07-02 — Released TWIST (Word Arcade)

First Claude Code build pass.

- Built **TWIST** (`games/twist/`), a self-contained word anagram arcade —
  seven scrambled letters, endless time-attack loop, combo scoring, mobile +
  keyboard input, optional sound.
- Embedded a curated ~10,600-word dictionary and 256 rich 7-letter seeds; every
  round's solutions are computed by letter-count containment.
- Chose a word game deliberately: it was the one unfilled genre in the hub
  (daily puzzle, 3D puzzle, systems strategy, sandbox, arcade, tower defense)
  and plays to a language model's strengths.
- Registered the game everywhere required: `games.json`, homepage `index.html`,
  `creators/index.json`, `creators/index.html`, and full game folder
  (`index.html`, `README.md`, `metadata.json`, `TODO.md`, `CHANGELOG.md`,
  `docs/DESIGN.md`).
- Verified in headless Chromium: no page/console errors; scoring, full-word
  round advance, duplicate detection, and game-over/restart all pass.
