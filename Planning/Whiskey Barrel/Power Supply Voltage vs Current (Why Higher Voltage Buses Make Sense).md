## Core idea
Power is what really matters, not voltage by itself.

    P = V × I

For the same power, higher voltage means lower current.

Example (100 W system load):
- 24 V → ~4.2 A
- 12 V → ~8.3 A
- 5 V  → 20 A

Same power. Very different current.

---

## What a buck converter changes
A buck converter trades voltage for current.

- Voltage goes down
- Current goes up
- Power stays roughly the same (minus losses)

Example:
- LEDs need 5 V @ 10 A → 50 W
- At 90% efficiency, PSU must supply ~56 W
- From a 24 V rail: 56 W / 24 V ≈ 2.3 A

So even though the LEDs pull 10 A, the PSU only sees ~2.3 A.

The PSU mostly “feels” total watts, not the final load voltage.

---

## Why a higher-voltage system bus is better (e.g., 24 V)

Lower current on the main power lines means:
- Less voltage drop in wires
- Less heat in connectors and traces
- Easier wiring and routing
- More headroom for motors and converters

This is why PCs use 12 V rails, CNC machines use 24 V, and cars are moving toward 48 V systems.

You distribute higher voltage, then locally convert down.

---

## Motors make this even more important

Motors have:
- High startup and stall current
- Electrical noise
- Rapid load changes

Using a higher-voltage PSU with dedicated buck converters:
- Gives margin for current spikes
- Prevents voltage sag
- Keeps LEDs and controllers more stable
- Helps isolate motor noise

---

## Practical design rule

1. Estimate worst-case load watts
2. Add 30–50% margin (more for motors)
3. Choose a higher distribution voltage (12 V or 24 V)
4. Buck down near each load (motor rail, 5 V rail, etc.)

---

## One-line takeaway

Higher voltage doesn’t reduce power usage, but it reduces current,
and lower current makes power systems smaller, cooler, cleaner, and more reliable.
