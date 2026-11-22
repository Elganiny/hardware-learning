# Changelog: P01 Mini-Dashboard V2

## 2.0 (2026-11-21)

Based on [P00 V1](../P00-mini-dashboard-v1/).

**Added**
- Micro-USB socket J2 (Amphenol 10118194-0001LF) as the 5 V input; D+, D−, ID not connected.
- NCP1117 3.3 V linear regulator U1 (SOT-223) with 10 µF input and output capacitors C1, C2.
- Heat calculation for U1 as a note on the schematic.
- Silkscreen labels: `USB 5V`, `PWR`, `BTN`, J1 pin names, board name.

**Changed**
- J1 pin 2 is now a 3.3 V **output** (was an input in V1).
- Removed the PWR_FLAGs: the USB symbol and the regulator are real power sources for ERC.
- Schematic arranged left to right: USB → regulator → connector → button → LED.

**Fixed during review**
- C1 and C2 had been placed at each other's regulator pin; moved so each sits right at its own pin, traces re-routed.
- Power traces (VBUS, +3.3 V) widened from 0.2 to 0.4 mm.
- The regulator's footprint value on the PCB had been overwritten; restored to match the schematic.
- D+, D−, ID: three net labels with the same name had connected them together; replaced by no-connect flags.
