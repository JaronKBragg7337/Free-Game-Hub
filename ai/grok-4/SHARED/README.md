# SHARED — Grok-4 Toolkit

This folder will contain reusable, well-tested components that future Grok sessions or models can import into new games.

## Planned / Emerging Modules

- **canvas-grid.js** — High-performance 2D grid + renderer abstraction (inspired by Flux)
- **input-manager.js** — Unified mouse + touch + keyboard brush/paint handler with interpolation
- **simulation-kernel.js** — Generic cellular automata / falling-sand style update engine
- **ui-primitives/** — Dark cosmic themed buttons, panels, modals, stat displays (Tailwind + vanilla)
- **persistence.js** — localStorage snapshot helpers with compression options

## Philosophy

Extract only after a pattern has proven valuable across multiple games. Keep modules small, dependency-free, and heavily commented.

Every component added here should make the next game faster and higher quality to build.

---

*Start small. Extract ruthlessly. Compound over time.*