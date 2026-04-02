# 2-Channel Audio Amplifier PCB

A production-ready 2-channel audio amplifier board designed, manufactured, 
assembled, and validated as part of EEE394 (Printed Circuit Design 
Fundamentals) at Arizona State University.

## Overview

Each channel is driven by an **LM386N-1/NOPB** low-voltage audio amplifier IC. 
A shared **10K dual-gang potentiometer (PDB182-K420K-103A2)** controls the 
volume of both channels simultaneously. The board includes a **1N4001 reverse 
polarity protection diode** on the power input and a **green power indicator LED** 
so you always know when the board is live. Audio input is accepted via a 
**PRT-08032 3.5mm stereo jack** and output is delivered through two 
**TMM-102-04-G-S** 2-pin headers per channel.

## Schematic Highlights

| Block | Components |
|---|---|
| Amplifier ICs | 2× LM386N-1/NOPB |
| Volume Control | PDB182-K420K-103A2 (10K dual-gang pot) |
| Input Connector | PRT-08032 (3.5mm stereo jack) |
| Output Connectors | 3× TMM-102-04-G-S (2-pin headers) |
| Power Protection | 1N4001-E3/73 reverse polarity diode |
| Power Indicator | WP7113SGD green LED + 470Ω resistor |
| Decoupling | 100µF × 4, 10µF × 2, 50nF × 2 bulk + bypass caps |
| Gain Filter | 1.2KΩ + 10µF RC network per channel |
| Supply | Battery (VCC) |
| PCB Layers | 2 |

## How It Works

The stereo audio signal enters through the 3.5mm jack and is split into left 
and right channels. Each channel feeds the non-inverting input (IN+) of its 
LM386. The dual-gang potentiometer sits between the input and the amplifier 
to control gain before amplification. Bulk decoupling capacitors (100µF) on 
each VCC rail suppress supply noise, while the output RC network (1.2KΩ + 
10µF) filters the amplified signal before it reaches the output headers. The 
250µF output coupling capacitor blocks DC from the speaker load.

## Validation Results

- Powered from battery — supply rails confirmed with DMM
- Audio output confirmed on both channels — first try, no rework required
- Volume control verified across full pot range
- Power indicator LED functional
- Reverse polarity protection verified

## Status

✅ Designed · ✅ Manufactured · ✅ Assembled & Soldered · ✅ Tested & Validated

## Tools Used

Altium Designer · DMM · Oscilloscope · Soldering Station · Battery Supply

## Key Skills Demonstrated

Schematic capture · Dual-channel analog layout · Decoupling network design · 
SMD & TH component assembly · Board bring-up & electrical validation · 
Gerber/BOM/NC drill generation · DFM
