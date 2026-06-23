# 🎵 Complementary Darlington Class-AB Audio Power Amplifier

A three-stage **Class-AB audio power amplifier** designed and simulated in **LTspice**. The amplifier combines a voltage amplification stage, a three-diode Class-AB bias network, and a complementary **Darlington push-pull output stage** to achieve low distortion, high current gain, and efficient power delivery to an **8 Ω speaker load**.

---

## 📌 Project Overview

The objective of this project was to design and analyze a low-distortion audio power amplifier capable of driving an **8 Ω load** while maintaining good efficiency and low Total Harmonic Distortion (THD).

### Key Features

- Three-stage Class-AB architecture
- Complementary Darlington output stage
- Three-diode Class-AB bias network
- High current gain output stage
- Low crossover distortion
- Low THD operation
- Efficient power delivery to 8 Ω load

### Analyses Performed

- Transient Analysis
- Fourier (FFT) Analysis
- Power Analysis
- Efficiency Calculation
- THD Measurement

---

## 📸 Circuit Schematic

<p align="center">
  <img src="<img width="1197" height="627" alt="image" src="https://github.com/user-attachments/assets/209ad3e6-dcea-4c81-bb69-cddc93896f7b" />
" width="900">
</p>

**Figure 1:** Complete LTspice schematic of the Complementary Darlington Class-AB Audio Power Amplifier.

---

## 🏗️ Amplifier Architecture

The amplifier consists of three stages:

### 🔵 Stage 1 – Voltage Amplification Stage

#### Components

- UniversalOpamp2
- Feedback Network
- Input Coupling Capacitor

#### Functions

- Provides voltage amplification
- Offers high input impedance
- Amplifies the input audio signal
- Drives the output power stage

The op-amp is configured as a non-inverting amplifier with a closed-loop gain of approximately **8 V/V**.

---

### 🟢 Stage 2 – Three-Diode Class-AB Bias Network

#### Components

- D1, D2, D3 (1N4148)
- Bias Resistors
- Coupling Capacitors

#### Functions

- Establishes Class-AB operation
- Generates bias voltage for output transistors
- Reduces crossover distortion
- Improves output waveform linearity

#### Bias Voltage

```
Vbias ≈ 3 × 0.7 V
Vbias ≈ 2.1 V
```

This keeps both halves of the output stage slightly conducting around the zero-crossing region.

---

### 🟠 Stage 3 – Complementary Darlington Output Stage

#### Components

- TIP31C Darlington Pair
- TIP32C Darlington Pair
- 0.5 Ω Emitter Resistors
- 8 Ω Load

#### Functions

- Provides high current gain
- Drives low impedance speaker loads
- Delivers output power efficiently
- Reduces loading on the voltage amplifier stage

#### Why Darlington Pairs?

The Darlington configuration was selected to:

- Increase effective current gain
- Reduce drive current requirements
- Improve load-driving capability
- Improve large-signal performance
- Enable efficient power delivery into an 8 Ω load

The measured efficiency improved compared to a basic complementary emitter-follower stage due to reduced loading and improved output voltage swing.

---

## 📊 Transient Analysis

<p align="center">
  <img src="images/transient_response.png" width="900">
</p>

**Figure 2:** Input and output waveforms at 1 kHz.

### Results

| Parameter | Value |
|------------|---------|
| Input Peak Voltage | 1 V |
| Output Peak Voltage | 8 V |
| Voltage Gain | 8 V/V |
| Voltage Gain (dB) | 18.06 dB |

### Observation

The amplifier successfully amplifies a 1 V peak input signal to approximately 8 V peak while maintaining waveform integrity and low distortion.

---

## ⚡ Output Power Analysis

<p align="center">
  <img src="images/output_power.png" width="900">
</p>

**Figure 3:** Instantaneous load power delivered to the 8 Ω speaker load.

### Result

| Parameter | Value |
|------------|---------|
| Average Output Power | 3.99 W |

The amplifier delivers nearly 4 W of power to the load while maintaining low harmonic distortion.

---

## 🔋 Supply Power Analysis

<p align="center">
  <img src="images/input_power.png" width="900">
</p>

**Figure 4:** Power drawn from the ±12 V supply rails.

### Result

| Parameter | Value |
|------------|---------|
| Average Input Power | 7.92 W |

---

## 📈 Efficiency Analysis

Efficiency was calculated using:

```
η = (Pout / Pin) × 100
η = (3.99 / 7.92) × 100
η ≈ 50.4 %
```

### Result

| Parameter | Value |
|------------|---------|
| Efficiency | 50.4 % |

The measured efficiency falls within the practical range expected for discrete Class-AB power amplifiers.

---

## 🎼 Fourier Analysis & THD

<p align="center">
  <img src="images/fft_analysis.png" width="900">
</p>

**Figure 5:** Fourier spectrum of the amplifier output.

### Fourier Results

| Parameter | Value |
|------------|---------|
| Fundamental Frequency | 1 kHz |
| Fundamental Amplitude | 6.99 V |
| THD | 0.033 % |

### Observation

The low THD demonstrates:

- Effective suppression of crossover distortion
- Proper Class-AB biasing
- Good linearity of the Darlington output stage
- High-quality audio amplification

---

## 📋 Performance Summary

| Parameter | Value |
|------------|---------|
| Supply Voltage | ±12 V |
| Load Resistance | 8 Ω |
| Voltage Gain | 8 V/V |
| Voltage Gain (dB) | 18.06 dB |
| Output Power | 3.99 W |
| Input Power | 7.92 W |
| Efficiency | 50.4 % |
| THD | 0.033 % |
| Output Stage | Complementary Darlington |
| Bias Network | Three-Diode Class-AB |

---

## 🛠️ Tools Used

- LTspice
- Analog Circuit Design
- Transient Simulation
- Fourier Analysis
- Power Analysis
- Efficiency Evaluation

---

## 🚀 Future Improvements

- PCB implementation
- Thermal analysis of output transistors
- Speaker protection circuitry
- Tone control stage
- Sziklai-pair output stage comparison
- Higher power output design
- Closed-loop stability optimization

---

## 📂 Repository Structure

```text
├── LTspice_Files
│   ├── AUDIO_AMPLIFIER_CIRCUIT.asc
│   └── AUDIO_AMPLIFIER_CIRCUIT.net
│
├── Images
│   ├── schematic.png
│   ├── transient_response.png
│   ├── output_power.png
│   ├── input_power.png
│   └── fft_analysis.png
│
└── README.md
```

---

## 👨‍💻 Author

**Aditya**

Analog Electronics • Audio Power Amplifier Design • LTspice Simulation
