# Industrial Automatic Power Factor Correction System

Single-phase APFC system for loads up to 5kW, designed for real industrial
deployment in a DIN rail enclosure.

**Status:** In progress · 4-layer layout · to be open-sourced on OSHWLab
(OSHWLab Stars 2026)

## The Problem
Inductive loads — motors, compressors, welding machines — draw reactive current
that inflates bills and stresses wiring without doing useful work. Most affordable
solutions only *monitor*. This one corrects.

## Hardware
| Block | Part / Approach |
|---|---|
| MCU | ESP32-WROOM-32E (dual core, WiFi) |
| Voltage sensing | Isolated, via potential transformer |
| Current sensing | SCT-013 split-core CT (galvanic isolation) |
| Capacitor bank | Binary-weighted 60/120/240µF CBB65 — 7 steps, 1–7 kVAR |
| Switching | S216S02 solid state relays, zero-cross |
| Protection | MOV surge clamping · DIN rail EMI filter · fused mains · TVS |
| Display | SH1106 OLED |

## PCB
4-layer mixed-signal design:
- Mains-side isolated on bottom layer
- Analog sensing shielded by ground plane
- DIN rail form factor for direct panel installation

## Firmware / Dashboard
Live WiFi dashboard (no internet required) reporting Vrms, Irms, active/reactive/
apparent power, power factor, and capacitor bank status.

## Prior Version
Started as a Veroboard build with an Arduino Nano — calibrated sensors,
relay-switched capacitor bank, hysteresis-based correction algorithm.
