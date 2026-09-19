<div align="center">

# ⚡ Hardware Portfolio
### Arham Amir

**Electronics Engineering @ NED University, Karachi** · Class of 2028

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/arham-amir-bb06a936b)
[![KiCad](https://img.shields.io/badge/KiCad-9.0-blue?style=flat&logo=kicad&logoColor=white)](https://kicad.org)
[![License](https://img.shields.io/badge/License-MIT-green?style=flat)](./LICENSE)

Multi-layer PCB designs — schematic capture to fabrication-ready output.  
Every board includes the full KiCad source, renders, and DRC verification.

</div>

---

## 📂 Projects

| # | Project | Layers | Key Focus | Status |
|:---:|---|:---:|---|:---:|
| 01 | **[LattePanda Mu Carrier Board](./01-LattePanda-Mu-Carrier-Board)** | 4 | USB 3.0 · HDMI · GbE, controlled impedance | 🟡 In Progress |
| 02 | **[BGA Smart USB Drive](./02-BGA-Smart-USB-Drive)** | 4 | RP2040 + 64GB eMMC, 0.5mm BGA escape | 🟢 Complete |
| 03 | **[Industrial APFC System](./03-Industrial-APFC-System)** | 4 | 5kW single-phase, mains isolation | 🟡 In Progress |
| 04 | **[STM32WB USB + RF Board](./04-STM32WB-USB-RF)** | 4 | 2.4GHz RF + USB, dual-ground stackup | 🟢 Complete |
| 05 | **[USB-C PD Power Supply](./05-USBC-PD-Power-Supply)** | 2 | CH224K PD negotiation, 90Ω diff pairs | 🟢 Complete |
| 06 | **[ESP32 Power Monitor](./06-ESP32-Power-Monitor)** | 4 | 5-channel relay + current sensing | 🟢 Complete |
| 07 | **[Hearing Assist DSP](./07-Hearing-Assist-DSP)** | — | Real-time NLMS noise cancellation | ✅ Built & Tested |
| 08 | **[8-bit CPU in Verilog](./08-CPU-8bit-Verilog)** | — | Full CPU, module-by-module | ✅ Simulated |
| 09 | **[MCU Board Collection](./09-MCU-Board-Collection)** | 2–4 | ESP32 / STM32 / MSPM0 variants | 🟢 Mixed |

---

## 🛠️ Technical Focus

<table>
<tr>
<td valign="top" width="50%">

**PCB Design**
- Controlled-impedance routing
- Differential pair matching
- Fine-pitch BGA fanout (via-in-pad, dogbone)
- Multi-layer stackup planning
- PDN design across multiple rails
- DFM / DRC verification

</td>
<td valign="top" width="50%">

**Embedded & Digital**
- ESP32 · STM32 · RP2040 · TI MSPM0
- FreeRTOS · real-time DSP
- Verilog RTL · FSM design
- ModelSim simulation

</td>
</tr>
<tr>
<td valign="top" colspan="2">

**Power Electronics**
- Mains-side isolation
- Protection: MOV, TVS, fusing
- SSR switching · boost/LDO regulation

</td>
</tr>
</table>
---
project-name/
├── README.md — design overview, challenges, decisions
├── kicad-project/ — full KiCad source (.kicad_pro/.sch/.pcb)
├── schematic.pdf — exported schematic view
├── pcb-layout-top.png — routed board, top view
├── 3d-render-top.png — 3D render
├── drc-report.png — DRC/ERC verification result
└── gerbers.zip — fabrication-ready Gerbers + drill files
---

> Every board ships with its **raw KiCad files** — not just images — so the
> design can be opened, checked, and verified directly rather than taken on faith.


<div align="center">

### 🔍 Fabrication Status

Some boards here are complete, verified designs that haven't been physically
built yet. Status is marked honestly on every project — closing the gap between
DRC-clean and physically validated is the current priority.

</div>

---

<div align="center">

*Feedback and corrections welcome — open an Issue on any project you'd improve.*

</div>

## 📁 Repository Structure

Each project folder follows the same layout:
