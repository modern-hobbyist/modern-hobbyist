---
title: CNC Machining
layout: home
nav_order: "3"
parent: Resources
---
# Choosing the right bit

# Feeds and Speeds
<img src="img/Pasted image 20250601111306.png" width="500px" />

---
## Cutting Aluminum

Assumptions:
- DIY CNC with Makita RT0701C trim router (10,000–30,000 RPM)
- 1-flute O-flute endmill (e.g., ZrN-coated or polished carbide)
- Aluminum 6061
- Air blast or mist coolant recommended
- Rigid fixturing and light cut strategy

### 1/8" Bit

| Parameter             | Value                            |
|----------------------|----------------------------------|
| **Spindle Speed**     | 20,000–22,000 RPM                |
| **Feed Rate**         | 25–35 in/min                     |
| **Depth of Cut (DOC)**| 0.010"–0.020" (0.25–0.5 mm)      |
| **Width of Cut (WOC)**| 0.0125"–0.025" (10–20% stepover) |
| **Chip Load**         | 0.0012–0.0018 in/tooth           |

### 1/4" Bit

| Parameter             | Value                           |
|----------------------|---------------------------------|
| **Spindle Speed**     | 18,000 RPM                      |
| **Feed Rate**         | 45–60 in/min                    |
| **Depth of Cut (DOC)**| 0.02"–0.04" (0.5–1.0 mm)        |
| **Width of Cut (WOC)**| 0.025"–0.050" (10–20% stepover) |
| **Chip Load**         | 0.0025–0.0035 in/tooth          |

### Tips for Success

- 💨 **Coolant**: Use compressed air or a mist coolant system to evacuate chips and reduce heat.
- 🧲 **Tool Coating**: ZrN or polished carbide helps prevent aluminum from welding to the cutter.
- 🧱 **Workholding**: Ensure aluminum is rigidly clamped to minimize vibration and deflection.
- 🛢️ **Lubrication**: Apply WD-40 or Tap Magic manually if mist is unavailable.
- ↪️ **Entry Strategy**: Use ramp or helical entry; avoid plunging directly into the material.
- 👂 **Listen and Watch**:
  - Squealing = spindle too fast or poor chip evacuation.
  - Gumming = aluminum welding to tool → reduce speed or add lubricant.
  - Chatter = machine flex → reduce DOC or WOC.
### Notes

- These are **conservative values** for DIY routers. Adjust incrementally once you're confident.
- Always prioritize **chip evacuation** — aluminum chips are your biggest enemy.

---