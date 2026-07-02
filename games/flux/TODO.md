# TODO — Flux (Grok-4)

## v1.0 Status (2026-07-02)

- [x] Core falling-sand simulation with 8 elements and physically-inspired interactions
- [x] Full desktop + mobile touch support with smooth brush painting
- [x] Polished cosmic dark UI with Tailwind + responsive layout
- [x] 4 guided Challenges with interesting starting seeds and progress validation
- [x] Pause/Resume, Clear, Randomize, Save/Load snapshot (localStorage)
- [x] Keyboard shortcuts, brush size control, right-click erase
- [x] Performance tuned (160×120 grid, optimized JS loop)
- [x] Zero console errors, clean code structure
- [x] Embedded provenance and attribution

## Next Steps / Polish

- [ ] Add subtle particle glow / bloom post-effect for fire & spark (CSS filter or offscreen canvas)
- [ ] Improve water displacement of sand and sideways flow logic for more natural feel
- [ ] Add 2-3 more element interactions or a 9th element (e.g. Lava or Electricity)
- [ ] Better win-condition feedback + confetti / celebration for completed challenges
- [ ] Optional "relaxed" mode with slower simulation and more growth-focused plant behavior
- [ ] Export current world as image (PNG) button
- [ ] Mobile: better brush preview / finger cursor indicator

## Known Issues

- None critical. Fire spread can sometimes feel slightly aggressive in open areas (intentional for drama, tunable).
- Very large brush sizes on slow devices can cause brief jank (rare).

## Future Experiments

- Web Worker offload for simulation step (for 256×192+ grids)
- Simple reactive audio (Web Audio) — crackle for fire, flow for water
- "Theory" mode that shows underlying rules as player experiments
- Integration with future SHARED/ components (e.g. reusable grid engine)

---

*Flux v1.0 is a strong, complete, enjoyable first contribution. Ready for players.*