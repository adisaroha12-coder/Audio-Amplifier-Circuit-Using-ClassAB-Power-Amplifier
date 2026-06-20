# Class-AB Audio Power Amplifier

## Overview

This project presents the design and simulation of a **Class-AB Audio Power Amplifier** in LTspice. The amplifier consists of a voltage amplification stage, a diode-based Class-AB bias network, and a complementary push-pull BJT output stage for efficient audio power delivery to an 8 Ω load.

## Features

- Three-stage amplifier architecture
- Op-amp based voltage amplification
- Diode-compensated Class-AB biasing
- Complementary push-pull output stage
- Low crossover distortion
- Frequency response analysis
- THD measurement using Fourier analysis
- Power and efficiency evaluation

---

## Circuit Architecture

### Stage 1: Voltage Amplification

- Input coupling network (C1-R1)
- UniversalOpamp2 voltage amplifier
- Closed-loop gain configuration
- High input impedance

### Stage 2: Interstage Coupling & Biasing

- AC coupling network (C2-R5)
- Diode bias network (D1-D2)
- Bias stabilization network
- Crossover distortion reduction

### Stage 3: Power Output Stage

- Complementary TIP41/TIP42 transistor pair
- Push-pull Class-AB operation
- Output coupling capacitor
- 8 Ω load interface

---

## Block Diagram

```text
Audio Input
     │
     ▼
┌─────────────────┐
│ Voltage         │
│ Amplification   │
│ (UniversalOpamp)│
└─────────────────┘
     │
     ▼
┌─────────────────┐
│ Coupling &      │
│ Class-AB Bias   │
│ Network         │
└─────────────────┘
     │
     ▼
┌─────────────────┐
│ Push-Pull       │
│ Power Stage     │
│ TIP41 / TIP42   │
└─────────────────┘
     │
     ▼
    8 Ω Load
```

---

## Design Specifications

| Parameter | Value |
|------------|---------|
| Supply Voltage | ±12 V |
| Load Resistance | 8 Ω |
| Amplifier Class | Class-AB |
| Simulation Tool | LTspice |
| Input Frequency | 1 kHz |
| Output Stage | TIP41 / TIP42 |

---

## Performance Results

### Frequency Response

| Parameter | Value |
|------------|---------|
| Lower Cutoff Frequency | ≈ 42 Hz |
| Upper Cutoff Frequency | ≈ 250 kHz |

### Distortion Performance

| Parameter | Value |
|------------|---------|
| THD | ≈ 0.025 % |

### Power Performance

| Parameter | Value |
|------------|---------|
| Output Power | ≈ 1.43 W |
| Input Power | ≈ 2.52 W |
| Efficiency | ≈ 56.8 % |

---

## Simulations Performed

### AC Analysis

- Gain measurement
- Bandwidth estimation
- Cutoff frequency determination

### Transient Analysis

- Output waveform verification
- Clipping detection
- Dynamic response evaluation

### Fourier Analysis

- Harmonic spectrum analysis
- Total Harmonic Distortion (THD) measurement

### Power Analysis

- Output power measurement
- Input power measurement
- Efficiency calculation

---

## Key Results

- Achieved Class-AB operation with low crossover distortion
- Obtained THD as low as **0.025%**
- Delivered approximately **1.43 W** into an **8 Ω load**
- Achieved approximately **56.8% efficiency**
- Maintained stable operation across the audio frequency range

---

## Tools Used

- LTspice
- Analog Circuit Design
- AC Analysis
- Fourier Analysis
- Transient Analysis

---

## Future Improvements

- PCB implementation
- Thermal analysis
- Speaker protection circuit
- Tone control stage
- Higher power output design

---

## Author

**Aditya**

Analog Circuit Design • Audio Electronics • LTspice Simulation
