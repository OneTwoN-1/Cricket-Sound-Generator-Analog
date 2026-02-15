# Cricket-Sound-Generator-Analog
Electronic "chirp" synthesizer implementing a PNP-based power gating solution to synchronize dual NE555 stages without using the Reset pin.

# 🦗 Cricket Sound Generator - Analog Synthesis

This project implements an electronic system for the analog synthesis of a "chirp" (cricket) acoustic signal. It was developed as a semester project for the **Sisteme cu Circuite Integrate Analogice (SCIA)** course at the Technical University of Cluj-Napoca.

## 📋 Project Overview
The system uses a dual-oscillator configuration based on the **NE555** integrated circuit. A fundamental requirement of the project was to exclude the use of the Reset terminal (Pin 4) as a method for validating or synchronizing the secondary stage.

### Key Technical Innovation: Power Gating
Instead of traditional reset-pin control, this project implements a **Power Gating** solution. Logical isolation and stage synchronization are achieved through supply switching using a **BC557 PNP bipolar transistor**. This approach ensures that the audio stage is completely powered down during silent periods, significantly reducing power consumption.

## 🛠️ Technical Specifications
* **Architecture:** Dual NE555 astable oscillators.
* **Rhythm Oscillator (U1):** Low-frequency oscillator defining the cadence (~1.5s pause, ~30ms pulse).
* **Audio Oscillator (U2):** High-frequency oscillator generating the carrier signal (~2.8 kHz).
* **Power Supply:** 9V DC.
* **Output:** Active Buzzer with a 200Ω limiting resistor.

## 🔧 Hardware Implementation & Real-world Adjustments
While the initial design was validated through transient analysis, the physical assembly on a breadboard required specific fine-tuning:
* **Resistor Calibration:** Component values from the E24 series were precisely selected and adjusted to compensate for real-world tolerances and match the simulated timings.
* **Acoustic Optimization:** A capacitor was added to the **Control Voltage (CV) pin** of the audio oscillator. This slightly distorts the square wave, resulting in a more natural, "organic" timbre that better mimics a biological cricket.

## 📊 Results
The circuit produces stable, well-defined sound bursts. The efficiency of the Power Gating method was confirmed via oscilloscope, showing a clean transition of the audio stage power line.

## 📺 Visual Documentation

### Hardware Implementation
### Working Demo
You can see and hear the circuit in action (2.8 kHz audio frequency  with a 1.5s cadence in the video below:
[▶️ Watch the Cricket Sound Demo](https://youtube.com/shorts/ttppmvNhKKs?feature=share)
## 📁 Academic Context
> **Note:** This project was originally documented and presented in **Romanian** for academic purposes. The full technical report in Romanian is available in this repository: `Proiect_SCIA_Meteleauca_Damian.pdf`.

* **University:** Technical University of Cluj-Napoca (UTCN)
* **Faculty:** Electronics, Telecommunications and Information Technology (ETTI)
* **Author:** Damian Meteleaucă
* **Advisor:** Conf.Dr.Ing. Albert Csaba Fazakas
---
*Developed in 2026 as part of the SCIA Coursework.*
