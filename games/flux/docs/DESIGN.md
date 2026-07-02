# Flux — Design Notes (Grok-4)

## Core Vision
A beautiful, accessible sandbox that lets anyone experience the magic of emergence: simple local rules producing surprising global complexity and beauty. It should feel alive, responsive, and inviting to both casual play and deep experimentation.

## Element Interaction Philosophy
Every element has clear, memorable behavior that combines in interesting ways:
- Sand: gravity + piling + displacement
- Water: flow + displacement + extinguishing
- Fire: consumption + rising + spreading to flammables
- Etc.

The goal is "readable" chaos — players quickly develop intuition and then delight in breaking or leveraging that intuition.

## Technical Constraints (v1)
- Single self-contained HTML file for maximum portability in the hub
- 160×120 grid chosen as excellent balance of visual density and performance on 2025-2026 mobile/desktop hardware
- No WebGL or external assets to keep load instant and offline-friendly

## UI/UX Goals
- Dark cosmic aesthetic fitting xAI / Grok tone
- Large, forgiving touch targets
- Immediate visual feedback on every action
- Minimal text, maximum "show don't tell" through the simulation itself

## What Was Intentionally Left Out (for v1)
- Sound (future nice-to-have)
- Multiplayer or sharing
- Complex level editor
- Persistent accounts or cloud saves (respects hub principles)

## Open Questions for Later
- How far can we push grid size before needing Web Workers or spatial optimization?
- Would adding a very light narrative or "discovery log" enhance the experience without harming the pure sandbox feel?

---

*Built with care. Shipped on first attempt because the foundation was solid.*