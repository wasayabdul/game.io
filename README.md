# SKYBREAK — Flying Roadster

A premium 3D browser game: drive a futuristic Tesla-inspired electric supercar through a
neon city at night, launch into the sky on rocket thrusters, chain aerial stunts,
dodge traffic and drones, and race your own ghost.

Built with **Three.js + React + TypeScript + Vite**. All models, textures and audio are
generated procedurally at runtime — no asset downloads.

## Run it

```bash
npm install
npm run dev        # dev server (default http://localhost:5173)
```

Production build:

```bash
npm run build      # type-check + bundle into dist/
npm run preview    # serve the build locally
```

## How to play

| Action            | Desktop              | Mobile                        |
|-------------------|----------------------|-------------------------------|
| Steer             | A/D or ←/→           | ◀ ▶ buttons or drag           |
| Climb / dive      | W/S or ↑/↓ (airborne)| ▲ ▼ buttons or swipe          |
| Rocket boost      | Hold SPACE           | Hold BOOST                    |
| Stunt (airborne)  | SHIFT                | STUNT button                  |
| Pause             | ESC / P              | Pause button                  |

**Objective:** survive as long as possible. Collect cyan energy orbs to recharge boost,
pass golden rings (dead-center = PERFECT), graze obstacles for near-miss bonuses, and
chain everything into a combo multiplier up to x8. Ramps launch you into flight;
tunnels, rooftops and floating platforms reward aerial lines.

## Game modes

- **INFINITE RUN** — endless procedural city, rising difficulty, saved high score + ghost replay of your best run.
- **STUNT CHALLENGE** — 90 seconds to land flips, barrel rolls and ring passes.
- **TIME ATTACK** — hit checkpoint gates before the clock runs out.
- **SKYBREAK MISSIONS** — 8 missions across 4 districts (Neo-Cyan, Violet Pulse, Amber Grid, Crimson Circuit) with unlockables and credit rewards.

## Progression

Credits earned from runs, missions, dailies and achievements buy garage cosmetics
(paints, underglow, wheels, thruster effects) and permanent upgrades
(boost capacity, recharge rate, steering response, aerial stability).
Daily challenges, achievements, settings and high scores persist in `localStorage`.

## Tech notes

- Delta-time fixed-step physics (120 Hz accumulator), object-pooled obstacles/particles, chunked procedural city with per-chunk recycling.
- Procedural canvas textures (windows, road, signs, sky) and WebAudio-synthesized engine hum, wind, boost, SFX and a synthwave music loop — zero external assets.
- Graphics quality settings (low/med/high) control pixel ratio, shadows and fog; touch + keyboard input with drag steering option.
