# Analog Process Automation Controller

Fully analog automation system — no microcontroller, no firmware — built
entirely from discrete logic.

## Function
Automates a liquid-filling process: turns on a pump at regular intervals,
checks for flow, detects tank-full state, and safely controls AC appliances.

## How It Works
| IC | Role |
|---|---|
| NE555 #1 | 30-minute interval timer (astable) |
| NE555 #2 | Intermediate latch/controller based on flow detection |
| NE555 #3 | Final appliance state control based on sensor feedback |
| BC547 stage | Tank-full detection via probe contact sensing |
| 5× relays | Sequencing and isolation for safe AC control |

## Why This Project
A deliberate exercise in analog system design — showing what's achievable
with discrete components and timing logic alone, no code or bootloader
involved.
