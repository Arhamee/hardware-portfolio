# Real-Time Hearing Assist System

Three clinical-grade DSP modes running on an ESP32. Total hardware cost: **$12.50**.

**Status:** Built and tested (module-based, custom PCB planned)

## Modes

**1 — Adaptive Noise Cancellation**
Two INMP441 MEMS mics on a single I2S bus running differential NLMS in real time.
A normalised gain ceiling computed from the RMS ratio of both channels prevents
over-subtraction artefacts. **12–18 dB reduction at 100–3000 Hz**, measured against
a broadband fan source.

**2 — Alert Detection**
No FFT. Zero-Crossing Rate analysis on 256-sample blocks (16ms windows) classifies
signals by frequency band. Siren detection tracks ZCR direction reversals to catch
the characteristic pitch sweep; alarm detection uses an EMA to catch pulsed energy
at 1–8 Hz. Tested to 2m with zero false positives on music or speech.

**3 — Tinnitus Masking**
2nd-order IIR biquad bandpass (Audio EQ Cookbook, Direct Form I) shaping LFSR white
noise to a 500–1000 Hz window centred on one of six clinically relevant frequencies
from 3–7 kHz. Coefficients computed analytically on every frequency change; filter
state zeroed to prevent transient pops.

## System Architecture
FreeRTOS, four tasks pinned across two cores — `audioTask` on Core 1 at priority 5
handles all DSP uninterrupted while Core 0 manages OLED, touch input, and alert
beeps. **End-to-end latency: 18ms**, within the ITU-T G.711 voice threshold.

## Context
Equivalent functionality to hearing aids retailing at $2,500–$4,000.

## Roadmap
Migrate to ESP32-S3 MINI-1 (LX7 core, PIE vector DSP extensions) for a full 64-tap
NLMS, plus a custom 4-layer behind-the-ear PCB. Projected v3.0 BOM with LiPo: $7.60.

## Note
Current build uses off-the-shelf modules rather than a custom board. Firmware and
DSP algorithm work are the substance here; PCB integration is the next step.
