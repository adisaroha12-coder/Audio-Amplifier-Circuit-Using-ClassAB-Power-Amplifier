# 🎵 Class-AB Audio Power Amplifier

A three-stage Class-AB audio power amplifier designed and simulated in **LTspice**. The amplifier consists of a voltage amplification stage, a Class-AB bias network, and a complementary push-pull power output stage for low-distortion audio amplification.

---

## 📌 Project Overview

The objective of this project was to design and analyze a low-distortion audio amplifier capable of driving an **8 Ω speaker load** while maintaining good efficiency and low Total Harmonic Distortion (THD).

Key analyses performed:

- AC Analysis
- Transient Analysis
- Fourier (FFT) Analysis
- Power Analysis
- Efficiency Calculation
- THD Measurement

---

## 🏗️ System Architecture

```text
┌────────────────────┐
│ 🎵 AUDIO INPUT     │
│ 1 kHz Sine Wave    │
└─────────┬──────────┘
          │
          ▼
┌────────────────────┐
│ 🔵 STAGE 1         │
│ Voltage Amplifier  │
│ Universal Op-Amp   │
│ Gain ≈ 6           │
└─────────┬──────────┘
          │
          ▼
┌────────────────────┐
│ 🟢 STAGE 2         │
│ Coupling & Biasing │
│ D1, D2, R7, R8     │
│ Class-AB Bias      │
└─────────┬──────────┘
          │
          ▼
┌────────────────────┐
│ 🟠 STAGE 3         │
│ Push-Pull Output   │
│ TIP41 + TIP42      │
│ Power Amplifier    │
└─────────┬──────────┘
          │
          ▼
┌────────────────────┐
│ 🔴 8Ω SPEAKER      │
│ Audio Output       │
└────────────────────┘
```

---

# 🔵 Stage 1: Voltage Amplification

### Components
- UniversalOpamp2
- C1
- R1
- R2
- R3
- R4

### Functions

- Blocks DC from the input source.
- Provides high input impedance.
- Amplifies the audio signal voltage.
- Prepares the signal for the power stage.

### Input Coupling Network

| Component | Value |
|------------|---------|
| C1 | 1 µF |
| R1 | 100 kΩ |

Cutoff Frequency:

\[
f_c = \frac{1}{2\pi RC}
\]

\[
f_c \approx 1.59 Hz
\]

---

# 🟢 Stage 2: Coupling & Class-AB Bias Network

### Components

- C2
- R5
- D1
- D2
- R6
- C3
- R7
- R8

### Functions

- Blocks op-amp DC offset.
- Generates Class-AB bias voltage.
- Reduces crossover distortion.
- Provides stable transistor biasing.

### Interstage Coupling Network

| Component | Value |
|------------|---------|
| C2 | 47 µF |
| R5 | 220 kΩ |

Cutoff Frequency:

\[
f_c \approx 0.015 Hz
\]

### Bias Voltage

Two silicon diodes generate approximately:

\[
V_{bias} \approx 1.4V
\]

which keeps both output transistors slightly ON.

---

# 🟠 Stage 3: Push-Pull Power Amplifier

### Components

- TIP41
- TIP42
- R9
- R10
- C6
- R11

### Functions

- Provides current amplification.
- Drives low impedance loads.
- Delivers power to the speaker.
- Maintains Class-AB operation.

### Output Coupling Network

| Component | Value |
|------------|---------|
| C6 | 470 µF |
| R11 | 8 Ω |

Cutoff Frequency:

\[
f_c \approx 42.3 Hz
\]

---

# 📈 Performance Results

## Frequency Response

| Parameter | Value |
|------------|---------|
| Lower Cutoff Frequency | ≈ 42 Hz |
| Upper Cutoff Frequency | ≈ 250 kHz |

---

## Power Performance

| Parameter | Value |
|------------|---------|
| Load Resistance | 8 Ω |
| Output Power | ≈ 1.43 W |
| Input Power | ≈ 2.52 W |
| Efficiency | ≈ 56.8 % |

---

## Distortion Performance

### Total Harmonic Distortion (THD)

\[
THD=\frac{\sqrt{V_2^2+V_3^2+V_4^2+\cdots}}{V_1}\times100\%
\]

Measured THD:

| Operating Point | THD |
|-----------------|------|
| Optimized Point | ≈ 0.025 % |
| Near Maximum Output | ≈ 0.289 % |

---

# 🔬 Simulations Performed

## AC Analysis

- Gain Measurement
- Bandwidth Estimation
- Cutoff Frequency Determination

## Transient Analysis

- Output Waveform Verification
- Clipping Analysis
- Dynamic Response Study

## Fourier Analysis

- Harmonic Spectrum Analysis
- THD Measurement

## Power Analysis

- Output Power Calculation
- Input Power Calculation
- Efficiency Evaluation

---

# 📊 Key Results

✅ Three-stage Class-AB architecture

✅ Output Power ≈ 1.43 W

✅ Efficiency ≈ 56.8 %

✅ THD as low as 0.025 %

✅ Stable operation into 8 Ω load

✅ Audio-band amplification with low distortion

---

# 🛠️ Tools Used

- LTspice
- Analog Circuit Design
- AC Analysis
- Fourier Analysis
- Transient Simulation

---

# 🚀 Future Improvements

- PCB implementation
- Thermal analysis of output transistors
- Speaker protection circuitry
- Tone control stage
- Higher power output design

---

# 👨‍💻 Author

**Aditya**

Analog Electronics • Audio Amplifier Design • LTspice Simulation
