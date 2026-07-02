# CHANGELOG — Flux

## 2026-07-02 — v1.0 Initial Release

### Added
- Complete emergent matter simulation sandbox with 8 interacting elements (Sand, Water, Stone, Fire, Plant, Oil, Spark, Void)
- High-quality Canvas rendering at 160×120 resolution (4px cells) with glow effects on energetic elements
- Robust input system: mouse drag painting, touch support, interpolated strokes, wheel brush sizing, keyboard shortcuts
- 4 thoughtfully designed Challenges with custom starting worlds and progress validation:
  1. Contained Inferno
  2. Living Garden
  3. Stone Bridge
  4. Chain Reaction
- Full control suite: Pause/Resume, Clear, Randomize, Save/Load snapshot (persists in browser)
- Beautiful, accessible UI: cosmic dark theme, large touch targets, live stats, element descriptions
- Zero external runtime dependencies (Tailwind CDN only for styling)
- Full provenance visible in footer and README

### Technical
- Pure vanilla JavaScript, HTML5 Canvas, Tailwind via CDN
- Optimized single-pass simulation with careful in-place/buffer swapping
- Mobile-first responsive layout that works great on phones and tablets
- No console errors, clean separation of simulation / rendering / input

### Design Decisions
- Chose falling-sand style because it beautifully demonstrates emergence from simple local rules — core to Grok's interests in systems, complexity, and the universe.
- Challenges provide gentle onboarding and replay goals without turning the experience into a rigid puzzle game.
- Local-only persistence respects the "no tracking, player data stays in browser" principle of the hub.

---

Future versions will be appended here. This file is the complete engineering history of Flux.