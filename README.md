# Roadster Drop

A cartoon landing game in a single HTML file: a Tesla Roadster falls out of the sky, and you land it on cold-gas thrusters without bending it. The softer the touchdown, the more stars.

## Play

Play it at https://michalnawrot.github.io/tesla-roadster-drop/ or open `index.html` locally in a browser. There's no build step and nothing to install (the only external resource is Google Fonts).

## Controls

| Key | Action |
| --- | --- |
| <kbd>Space</kbd> (hold) or touch | Open the cold-gas nozzles |
| <kbd>A</kbd> | Toggle autopilot |
| <kbd>Enter</kbd> | Drop it (from the menu) |
| <kbd>R</kbd> | Restart the run |
| <kbd>N</kbd> | Next level (after landing) |
| <kbd>Esc</kbd> | Back to settings |

The menu also has an optional stopping-point predictor ("where would I stop if I burn now"), a sound toggle and autopilot.

## Levels

| Level | Height |
| --- | --- |
| Semi hop | 7 m |
| Ramp top | 21 m |
| Crane drop | 40 m |
| Tower drop | 70 m |
| Skydive | 120 m |

Pick a car weight anywhere from 300 kg to 2,400 kg, or use a preset:

| Preset | Weight | |
| --- | --- | --- |
| Hollow RC shell | 300 kg | a hollow body, no batteries |
| Tesla's target | 1,700 kg | lightest trim, "under 1,700 kg" |
| Typical EV | 2,000 kg | a full battery pack |
| Rocket, heavy | 2,400 kg | 600 L of tanks + 250 kg of air |

Difficulty follows the weight: heavier cars need almost the whole tank to stop from lower heights.

## Scoring

Rated on peak g-load at touchdown:

| Peak g | Result |
| --- | --- |
| ≤ 1.0 | ★★★ Feather landing |
| ≤ 2.0 | ★★ Clean landing |
| ≤ 3.5 | ★ Rough landing |
| > 3.5 | Wrecked |

## Physics

The simulation runs at 240 Hz with these numbers:

- Up to **80 kN** of thrust with all nozzles pointed straight down
- One 250 kg fill of compressed air gives about **80 kN·s** of total impulse
- Thrust fades to 30% as the tank empties and cools
- Valves take about 0.3 s to open and 0.04 s to close
- Aerodynamic drag on a car falling belly-first (Cd·A ≈ 8 m²)
- 20 cm of suspension travel absorbs the touchdown
