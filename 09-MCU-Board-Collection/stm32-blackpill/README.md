# STM32 "Black Pill" Board

First full PCB design completed end-to-end in KiCad 9 — schematic through
2-layer layout and routing.

## Included
- Power management (3.3V LDO)
- Reset circuitry and BOOT configuration
- USB Type-B Micro with proper D+/D− routing
- Careful component placement for signal integrity on a 2-layer board
- DRC passed — ready for prototype manufacturing

## What This Taught Me
MCU power requirements, decoupling strategy, and high-speed signal
considerations — even on a "simple" 2-layer board.

## Reference
Built following Phil Salmony's (Phil's Lab) PCB Design Course.

