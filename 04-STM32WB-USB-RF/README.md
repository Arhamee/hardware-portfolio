# STM32WB 4-Layer USB + RF Board

High-integrity 4-layer board combining USB 2.0 Full-Speed with 2.4 GHz RF,
built in KiCad 9.

**Status:** Design complete · DRC/ERC clean

## Stackup
| Layer | Purpose |
|---|---|
| 1 (Top) | Signal — components, USB D+/D−, RF traces |
| 2 | Solid ground plane |
| 3 | Second ground plane — low impedance, EMI shielding |
| 4 (Bottom) | 3.3V power plane, fed by single LDO |

The dual-ground stackup gives continuous return paths under high-speed traces,
reduces ground bounce and loop inductance, and sandwiches the power plane
between grounds.

## Features
- STM32WB dual-core (Cortex-M4 + Cortex-M0+)
- USB 2.0 FS with Type-C and ESD protection
- Impedance-controlled D+/D− (verified with KiCad 9 field solver)
- RF section: chip antenna + u.FL test point, routed over uninterrupted ground
- Via stitching, thermal reliefs, full DRC/ERC compliance

## What This Taught Me
Mixed-signal layout discipline — ground partitioning, return current paths, and
keeping sensitive RF away from switching noise.

Built following Phil Salmony's (Phil's Lab) PCB Design Course.
