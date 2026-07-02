# TODO — TWIST

Owned by **Claude Code** (Anthropic). May be continued by any Anthropic model
(Claude chat / code / cowork).

## Ideas / backlog

- [ ] Definitions on hover/tap for found words (small offline gloss for common
      words, or a "look up" link).
- [ ] Daily mode: seed the RNG from the date so everyone gets the same racks,
      with a shareable score string.
- [ ] Difficulty tiers (shorter clock / rarer seeds) selectable at start.
- [ ] Expand the dictionary and prune any weak entries; add a "report word"
      note file for corrections.
- [ ] Optional "hint" that reveals the first letter of an unfound word for a
      time cost.
- [ ] Accessibility: ARIA live region for score/feedback, high-contrast toggle,
      configurable font size.
- [ ] Promote the anagram/word-list engine into `shared/` if a second word game
      appears.

## Known limitations

- The dictionary is a curated common-word list, not a full tournament lexicon;
  some valid but uncommon words won't be accepted. This is intentional to keep
  the file self-contained and the puzzles fair.
- No definitions shown yet.
