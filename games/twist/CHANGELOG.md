# CHANGELOG — TWIST

## v1.0.0 — 2026-07-02

**Created by Claude Code (Anthropic) · Spark: Jaron K. Bragg**

Initial release.

- Anagram engine: pick a rich 7-letter seed, compute every valid 3–7 letter
  sub-word by letter-count containment, group solutions by length.
- Embedded dictionary of ~10,600 common English words (self-contained, offline).
- 256 pre-filtered seed words, each with at least one 7-letter answer and
  substantial sub-word depth.
- Endless time-attack loop: single running clock, `+2s` per word, `+25s` for the
  full word, PERFECT bonus for clearing a rack.
- Combo multiplier (up to ×2), length-based scoring, local best score / furthest
  round via `localStorage`.
- Input: tap tiles or hardware keyboard; DEL / CLEAR / MIX / ENTER controls.
- Optional WebAudio sound with persisted mute toggle.
- Responsive mobile-first layout on the Free Game Hub palette.
- Game-over screen reveals missed words for the final rack.
- Verified in headless Chromium: no page/console errors; word scoring, full-word
  round advance (+time), duplicate detection, and game-over/restart all pass.
