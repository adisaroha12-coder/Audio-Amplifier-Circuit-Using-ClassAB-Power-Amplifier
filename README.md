# 🎵 Complementary Darlington Class-AB Audio Power Amplifier

A three-stage **Class-AB audio power amplifier** designed and simulated in **LTspice**. The amplifier combines a voltage amplification stage, a diode-biased Class-AB network, and a complementary **Darlington push-pull output stage** to achieve low distortion, high current gain, and efficient power delivery to an **8 Ω speaker load**.

---

# 📌 Project Overview

The objective of this project was to design and analyze a low-distortion audio power amplifier capable of driving an **8 Ω load** while maintaining good efficiency and low Total Harmonic Distortion (THD).

The design employs:

* Non-inverting voltage amplifier
* Three-diode Class-AB bias network
* Complementary Darlington emitter-follower output stage
* Negative feedback for gain stabilization

Key analyses performed:

* AC Analysis
* Transient Analysis
* Fourier (FFT) Analysis
* Power Analysis
* Efficiency Calculation
* THD Measurement

---

# 🏗️ Amplifier Architecture

The amplifier consists of three stages:

## 🔵 Stage 1 – Voltage Amplification Stage

### Components

* UniversalOpamp2
* Input coupling capacitor
* Feedback resistors

### Functions

* Provides voltage gain.
* Offers high input impedance.
* Amplifies the incoming audio signal.
* Drives the power output stage.

### Closed-Loop Gain

The op-amp is configured as a non-inverting amplifier:

[
A_v = 1+\frac{R_f}{R_g}
]

[
A_v = 1+\frac{70k}{10k}
]

[
A_v = 8
]

[
A_v = 18.06\ dB
]

---

## 🟢 Stage 2 – Class-AB Bias Network

### Components

* D1, D2, D3 (1N4148)
* Bias resistors
* Coupling capacitors

### Functions

* Establishes Class-AB operation.
* Generates bias voltage for the output stage.
* Minimizes crossover distortion.
* Improves linearity around the zero-crossing region.

### Biasing Principle

The three silicon diodes generate approximately:

[
V_{bias} \approx 2.1V
]

which partially forward-biases the output transistors and significantly reduces crossover distortion.

---

## 🟠 Stage 3 – Complementary Darlington Output Stage

### Components

* TIP31C Darlington Pair
* TIP32C Darlington Pair
* Emitter resistors (0.5 Ω)
* 8 Ω Load

### Functions

* Provides high current gain.
* Drives low-impedance speaker loads.
* Delivers output power efficiently.
* Reduces loading on the voltage amplifier stage.

### Why Darlington Pairs?

The Darlington configuration was selected to:

* Increase effective current gain.
* Reduce drive current requirements.
* Improve load-driving capability.
* Improve large-signal performance.
* Enable efficient power delivery into an 8 Ω load.

The measured efficiency improved compared to the single-transistor output stage due to reduced loading and improved output swing.

---

# 📈 Performance Results

## Voltage Gain

| Parameter    | Value      |
| ------------ | ---------- |
| Voltage Gain | ≈ 8 V/V    |
| Gain (dB)    | ≈ 18.06 dB |

---

## Frequency Response

| Parameter              | Value      |
| ---------------------- | ---------- |
| Lower Cutoff Frequency | ≈ 35–40 Hz |
| Upper Cutoff Frequency | > 700 kHz  |
| Midband Gain           | ≈ 18 dB    |

The amplifier comfortably covers the entire audible frequency range (20 Hz – 20 kHz).

---

## ⚡ Power Performance

| Parameter       | Value    |
| --------------- | -------- |
| Supply Voltage  | ±12 V    |
| Load Resistance | 8 Ω      |
| Output Power    | ≈ 3.99 W |
| Input Power     | ≈ 7.92 W |
| Efficiency      | ≈ 50.4 % |

### Output Voltage

[
V_{RMS}=\sqrt{PR}
]

[
V_{RMS}=\sqrt{3.99 \times 8}
]

[
V_{RMS}\approx 5.65V
]

[
V_{PEAK}\approx 8V
]

---

## 📊 Distortion Performance

### Total Harmonic Distortion (THD)

[
THD=\frac{\sqrt{V_2^2+V_3^2+V_4^2+\cdots}}{V_1}\times100%
]

### Fourier Analysis Results

| Parameter             | Value   |
| --------------------- | ------- |
| Fundamental Frequency | 1 kHz   |
| Fundamental Amplitude | 6.99 V  |
| THD                   | 0.033 % |

The low THD demonstrates effective suppression of crossover distortion and good linearity of the Class-AB Darlington output stage.

---

# 🔬 Simulations Performed

## AC Analysis

* Voltage Gain Measurement
* Bandwidth Estimation
* Frequency Response Verification

## Transient Analysis

* Output Waveform Verification
* Large-Signal Gain Validation
* Clipping Analysis
* Dynamic Response Study

## Fourier Analysis

* Harmonic Spectrum Analysis
* THD Measurement
* Distortion Characterization

## Power Analysis

* Output Power Calculation
* Supply Power Calculation
* Efficiency Evaluation

---

# 📊 Key Results

✅ Three-stage Class-AB architecture

✅ Complementary Darlington output stage

✅ Three-diode Class-AB bias network

✅ Voltage Gain ≈ 8 V/V (18 dB)

✅ Output Power ≈ 4 W into 8 Ω load

✅ Efficiency ≈ 50.4 %

✅ THD ≈ 0.033 %

✅ Low crossover distortion

✅ Stable operation from ±12 V supply

✅ Wide bandwidth audio amplification

---

# 🛠️ Tools Used

* LTspice
* Analog Circuit Design
* AC Analysis
* Fourier Analysis
* Transient Simulation
* Power & Efficiency Analysis

---

# 🚀 Future Improvements

* PCB implementation
* Thermal analysis of output transistors
* Speaker protection circuitry
* Tone control stage
* Sziklai-pair output stage comparison
* Closed-loop compensation optimization
* Higher power output design

---

# 👨‍💻 Author

**Aditya**

Analog Electronics • Audio Power Amplifier Design • LTspice Simulation
