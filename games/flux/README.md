# Flux

**An emergent matter simulation sandbox**

Created by **Grok**  
Model: **Grok 4**  
Company: **xAI**  
Spark: **Jaron K. Bragg**

## What is Flux?

Flux is a living canvas where you paint with fundamental "elements" that obey simple physical rules. Sand falls. Water flows. Fire spreads and consumes. Plants grow when nourished. Watch order emerge from chaos — or chaos from order. 

It is both a creative toy and a gentle game of discovery and mastery.

## Why This Game?

Simple rules → complex, surprising, beautiful behavior. This is the same principle that builds galaxies, ecosystems, and minds. Flux is a tiny, playable model of that truth.

Replayability comes from:
- Endless free experimentation
- 4 distinct Challenges that test understanding of the rules
- The joy of discovering stable patterns, "machines", or accidental art you didn't intend

## Controls

**Desktop**
- Left-click + drag: Paint with selected element
- Right-click + drag: Erase (or use Void)
- Mouse wheel or +/- : Adjust brush size
- Space: Pause / Resume simulation
- C: Clear canvas
- R: Randomize / fill with mixed elements

**Mobile / Touch**
- Tap and drag with finger to paint
- Use the big element buttons (large touch targets)
- Pause/Play, Clear, and Challenge buttons are prominent

**Universal**
- All interactions are instant and responsive
- Simulation continues smoothly at ~60fps (or best your device allows)
- State is saved automatically to your browser (localStorage) — refresh safely

## Elements (8 types)

1. **Sand** — Falls down, piles realistically, displaced by water
2. **Water** — Flows down and sideways, puts out fire, nourishes plants, can be blocked by stone
3. **Stone** — Solid, immovable barrier. Good for building structures and containing reactions
4. **Fire** — Burns upward and spreads to flammable materials (Plant, Oil). Dies without fuel or in water
5. **Plant** — Grows slowly when touching water + space above. Burns easily
6. **Oil** — Flammable liquid, floats on water, spreads and burns intensely
7. **Spark** — Short-lived electrical arc. Ignites oil and plants, can jump gaps
8. **Void** — Eraser. Removes anything it touches (use to correct or sculpt)

## Challenges (Guided Play)

Complete these to truly understand the system:

1. **Contained Inferno** — Build a stone enclosure and start a self-sustaining fire inside without letting it escape.
2. **Living Garden** — Create a stable ecosystem where plants continue growing for a long time with minimal intervention.
3. **Bridge Builder** — Use stone and other elements to create a stable "bridge" or platform across a body of water.
4. **Reaction Chain** — Trigger a beautiful multi-stage reaction (e.g. oil fire that interacts with water and plants in interesting ways).

Press the **Challenge** button in the UI to load a starting scenario for the current challenge and see the goal description.

## Technical Notes

- Pure HTML + CSS + JavaScript (Tailwind CDN for rapid beautiful UI)
- Canvas 2D rendering with optimized cell updates
- Grid size tuned for performance on phones and laptops (160×120 cells)
- Fully open source under the repo license
- No accounts, no tracking, no ads, no data leaves your device

## Provenance

Created by **Grok**  
Model: Grok 4  
Company: xAI  
Spark: Jaron K. Bragg  
First added: 2026-07-02

Part of the Free Game Hub — free forever, respectful of you.

---

*Play. Experiment. Discover what emerges when you stop trying to control everything.*