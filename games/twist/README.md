# TWIST

**A word anagram arcade**

Created by **Claude Code**
Company: **Anthropic**
Spark: **Jaron K. Bragg**

Play it: open `index.html`, or visit
`https://jaronkbragg7337.github.io/Free-Game-Hub/games/twist/`

---

## What is TWIST?

TWIST gives you seven scrambled letters and a ticking clock. Spell as many
valid words (3–7 letters) as you can. Every word banks a little time; finding
the **full seven-letter word** banks a big chunk of time and jumps you to a
fresh set of letters. Keep the clock alive as long as you can and chase a high
score.

It is fully self-contained — one HTML file, no build step, no network calls, no
accounts, no ads. The dictionary (~10,600 common English words) and every
puzzle live inside the page, so it works offline and loads instantly.

## Why this game?

The hub already has a daily puzzle, 3D puzzle, systems strategy, sandbox,
arcade, and tower defense — but no **word game**. Anagram hunting is endlessly
replayable (every round is a fresh rack), it plays to a language model's
strengths, and it is naturally mobile-first: big tappable letter tiles, no
precise timing or dragging required.

## How to play

1. **Tap** a letter tile (or **type** it on a keyboard) to add it to your word.
2. Press **ENTER** to submit. Valid new words score points and add time.
3. **MIX** reshuffles the rack when you're stuck; **DEL** removes the last
   letter; **CLEAR** empties your current word.
4. Find the **7-letter word** to bank **+25s** and advance to a new rack.
5. Find **every** word in a rack for a **PERFECT** bonus.
6. When the clock hits zero, the game ends and shows the words you missed.

## Controls

**Touch**
- Tap rack tiles to build a word, tap a placed tile to take it back.
- On-screen **DEL / CLEAR / MIX / ENTER** buttons.

**Keyboard**
- Letter keys — add that letter from the rack
- `Enter` — submit · `Backspace` — delete last · `Space` — mix · `Esc` — clear

## Scoring

| Word length | Base points |
|---|---|
| 3 | 100 |
| 4 | 300 |
| 5 | 600 |
| 6 | 1000 |
| 7 | 2000 |

- **Combo:** each consecutive valid word raises a multiplier up to **×2**. A
  wrong guess resets the combo.
- **Full-word bonus:** finding the seven-letter word adds `500 + 100·round`
  points and `+25s`.
- **Perfect bonus:** clearing every word in a rack adds `1500 + 250·round`
  points and extra time.
- Best score and furthest round are saved locally (`localStorage`).

## Technical notes

- Single file: `index.html` (HTML + CSS + vanilla JS, no dependencies).
- Dictionary embedded as a space-joined string, loaded into a `Set` for O(1)
  validation. Seeds are pre-filtered 7-letter words with rich sub-word depth so
  every round has plenty to find and at least one full-length answer.
- Solutions per rack are computed by letter-count containment
  (`countLetters` + `canForm`), grouped by length for the board.
- Optional WebAudio blips with a persisted mute toggle. Everything is guarded so
  audio failures never affect gameplay.

## Provenance

```text
Created by: Claude Code
Company:    Anthropic
Spark:      Jaron K. Bragg
```

Part of [Free Game Hub](../../) — free forever, no ads, no tracking.
