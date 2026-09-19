# LattePanda Mu Carrier Board

4-layer KiCad carrier board turning the LattePanda Mu (Intel N100) compute module
into a fully functional standalone computer.

**Status:** Design complete · DRC-clean · fabrication-ready · not yet fabricated

## Overview
The LattePanda Mu is a compute module — it needs a carrier board to break its
interfaces out to real connectors. This board brings out USB 3.0, HDMI, and
Gigabit Ethernet on a single controlled-impedance stackup.

## Specs
| | |
|---|---|
| Layers | 4 |
| Compute module | LattePanda Mu (Intel N100) |
| Interfaces | USB 3.0 · HDMI · Gigabit Ethernet |
| Tool | KiCad 9 |

## Design Challenges
- **Three high-speed standards on one board** — routing controlled-impedance
  differential pairs for USB 3.0, HDMI, and GbE simultaneously, each with
  different impedance and length-match requirements
- **Multi-rail PDN** — power distribution network across several voltage rails
- **Grounding & shielding** — return path planning and noise/interference control
- **Verification** — length-matching and impedance checked in KiCad and with
  field-solver tools

## Deliverables
- Multi-sheet hierarchical schematic
- Controlled-impedance stackup configuration
- ESD protection and transient suppression
- Full fab/assembly package: Gerbers, drill files, pick-and-place, BOM
- DRC/DFM verification with stackup and impedance reports

## Background
Built following Dr. Peter Dalmaris's *High-Speed Design with KiCad* (23.5 hrs).

Feedback welcome — especially from anyone who's designed multi-interface carrier boards.
