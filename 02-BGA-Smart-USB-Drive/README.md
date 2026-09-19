# Smart USB Thumb Drive — RP2040 + eMMC

4-layer board packing an RP2040, USB2244 bridge, and 64GB eMMC in a
153-ball 0.5mm-pitch BGA into a thumb-drive footprint.

**Status:** Design complete · DRC-clean · manufacturing-ready · not yet fabricated

## Specs
| | |
|---|---|
| Layers | 4 |
| MCU | RP2040 |
| Bridge | USB2244 |
| Storage | 64GB eMMC — 153-ball BGA, 0.5mm pitch |
| Power path | LM66100 dual ideal-diode OR-ing |

## Design Challenges
- **Fine-pitch BGA escape** — via-in-pad and dogbone fanout strategies; took
  several iterations before clearances resolved cleanly
- **90Ω USB 2.0 differential pair** — held by planning the stackup deliberately
  rather than accepting defaults
- **eMMC parallel bus length-matching** — tighter tolerances than any previous design
- **Dual-port power** — two independent USB ports sharing power duty without backfeeding
- **Documented design intent** — scoped DRC exceptions rather than blanket
  rule suppression

## Background
Built following Peter Dalmaris's *KiCad Advanced: Design a Smart USB Thumb Drive* (26 hrs).

If you've routed fine-pitch BGAs and something here looks wrong — open an Issue.
I'd rather be corrected now than after boards come back from fab.
