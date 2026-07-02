# TWIST — Design Notes

## Goal

A word game that is instantly understandable, endlessly replayable, mobile-first,
and completely self-contained (no build, no network, works offline). It fills the
"word game" gap in Free Game Hub.

## Core loop

```
pick rich 7-letter seed
   -> compute all 3..7 letter sub-words (grouped by length)  -> the board
   -> player spells words against a shared countdown clock
        valid word     : +points (length-based x combo), +2s, reveal on board
        7-letter word  : +big bonus, +25s, load a NEW seed
        every word      : PERFECT bonus, +extra time, load a new seed
   -> clock hits 0 -> game over, reveal missed words, save best
```

One continuous clock (not a per-round timer) makes it a true arcade
time-attack: skilled play literally buys more time, so a good run can go on for
many rounds.

## Why a running clock instead of per-round timers

- Rewards speed and vocabulary directly (time is the currency).
- Removes "dead" downtime — there is always pressure.
- Creates a natural risk/reward: grab the full word fast for time, or linger to
  clear the rack for a PERFECT bonus and even more time.

## Dictionary & seeds

- ~10,600 curated common English words (3–7 letters), embedded as a
  space-joined string and loaded into a `Set` for O(1) lookup.
- Seeds are the 7-letter dictionary words that yield **≥ 14** sub-words, so every
  round is dense and always has at least one full-length answer. 256 qualify.
- Solutions are computed at round start by letter-count containment
  (`canForm(word, rackCounts)`), then grouped by length for the board.

Trade-off: a curated list (not a full tournament lexicon) keeps the game fair,
offline, and small. Building generation instead of validation guarantees every
accepted word is real and every revealed word is discoverable.

## Input model

Rack tiles carry a stable `id` and a `used` flag. Typing a letter consumes the
first unused tile of that character; tapping consumes a specific tile. The entry
row stores tile ids, so removing a letter frees exactly the right tile — this
handles duplicate letters correctly.

## Feel

- Scrabble-style raised tiles, `pop` animation on reveal, `shake` on invalid.
- Combo multiplier surfaces in the HUD and messages.
- Low-time state flips the clock bar and timer to a pulsing red.
- Tiny WebAudio blips (distinct tones for word / big word / error), fully muteable
  and guarded so audio never blocks gameplay.

## Verification

Smoke-tested in headless Chromium (Playwright):
- Start screen, word scoring, full-word round advance with `+25s`, duplicate
  detection, MIX, and the game-over screen + "Play Again" restart.
- No page errors, no console errors.
