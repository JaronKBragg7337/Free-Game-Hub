# WORKLOG — Claude Code

## 2026-07-02 — TWIST build session

**Context.** First Claude Code contribution. Read README / CONTRIBUTING /
`shared/standards/*`. Surveyed existing games (TRACE, Roll & Reach, The Loop,
FLUX, DRIFT, SENTINEL) and confirmed the only unfilled genre was a word game —
also the best fit for a language model's strengths.

**Decision.** Build TWIST: a TextTwist-style anagram arcade, fully self-contained
(one HTML file, offline, no deps) so it drops straight onto GitHub Pages.

**Engineering.**
- Built the dictionary offline with a Python helper: normalized a large curated
  word list to lowercase 3–7 letter words (~10,600 unique), then scored every
  7-letter word by sub-word depth and kept the 256 seeds with ≥14 sub-words.
- Generation-over-validation: the game reveals words drawn from its own list, so
  every accepted word is real and every revealed word is reachable — no risk of
  rejecting a word it "should" know or accepting garbage.
- Single running clock (time is the currency) instead of per-round timers, for a
  true endless time-attack loop with a speed-vs-completion trade-off.
- Tile-id + used-flag input model so duplicate letters behave correctly for both
  tap and keyboard.

**Verification.** Headless Chromium (Playwright) smoke tests: start screen, word
scoring, full-word round advance (+25s, new rack), duplicate detection, MIX, and
game-over → Play Again. No page or console errors. Screenshots reviewed for the
in-game board and the restart state.

**Registered.** `games/twist/` folder + `games.json`, homepage `index.html`,
`creators/index.json`, `creators/index.html`, and all contributor notes.
