# Hardware Portfolio — Arham Amir

**Electronics Engineering @ NED University, Karachi** · Class of 2028

Multi-layer PCB designs taken from schematic capture to fabrication-ready output.
All boards designed in **KiCad 9** with DRC/ERC compliance, BOM, and 3D renders.

📫 [LinkedIn](https://linkedin.com/in/arham-amir-bb06a936b)

---

## Projects

| # | Project | Layers | Key Focus | Status |
|---|---------|--------|-----------|--------|
| 01 | [LattePanda Mu Carrier Board](./01-LattePanda-Mu-Carrier-Board) | 4 | USB 3.0 · HDMI · Gigabit Ethernet, controlled impedance | Design complete |
| 02 | [BGA Smart USB Drive](./02-BGA-Smart-USB-Drive) | 4 | RP2040 + 64GB eMMC, 153-ball 0.5mm BGA escape | Design complete |
| 03 | [Industrial APFC System](./03-Industrial-APFC-System) | 4 | 5kW single-phase, mains isolation, mixed-signal | In progress |
| 04 | [STM32WB USB + RF Board](./04-STM32WB-USB-RF) | 4 | 2.4GHz RF + USB, dual-ground stackup | Design complete |
| 05 | [USB-C PD Power Supply](./05-USBC-PD-Power-Supply) | 2 | CH224K PD negotiation, 90Ω diff pairs | Gerbers ready |
| 06 | [ESP32 Power Monitor](./06-ESP32-Power-Monitor) | 4 | 5-channel relay + current sensing, web dashboard | Design complete |
| 07 | [Hearing Assist DSP](./07-Hearing-Assist-DSP) | — | Real-time NLMS noise cancellation on ESP32 | Built & tested |
| 08 | [8-bit CPU in Verilog](./08-CPU-8bit-Verilog) | — | Full CPU, module-by-module, no IP cores | Simulated |
| 09 | [MCU Board Collection](./09-MCU-Board-Collection) | 2–4 | ESP32 / STM32 / MSPM0 variants | Mixed |

---

## Technical Focus

**PCB Design** — controlled-impedance routing · differential pairs · fine-pitch BGA 
fanout (via-in-pad, dogbone) · multi-layer stackup planning · PDN design across 
multiple rails · length matching · DFM/DRC verification

**Embedded** — ESP32 · STM32 · RP2040 · TI MSPM0 · FreeRTOS · real-time DSP

**Digital Design** — Verilog RTL · FSM design · testbench simulation (ModelSim)

**Power** — mains-side isolation · protection (MOV, TVS, fusing) · SSR switching · 
boost/LDO regulation

---

## Repository Structure

Each project folder contains:
