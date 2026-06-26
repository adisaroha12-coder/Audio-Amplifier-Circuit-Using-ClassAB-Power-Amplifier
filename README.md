# 🎵 Complementary Darlington Class-AB Audio Power Amplifier

A three-stage **Class-AB audio power amplifier** designed and simulated in **LTspice**. The amplifier employs a **non-inverting voltage amplification stage**, a **four-diode Class-AB bias network**, and a **complementary Darlington push-pull output stage** to deliver low-distortion audio amplification with improved current driving capability for an **8 Ω speaker load**.

---

# 📌 Project Overview

This project focuses on the design and simulation of a discrete **Class-AB audio power amplifier** capable of driving low-impedance loads while maintaining low Total Harmonic Distortion (THD), moderate efficiency, and good voltage gain.

## Key Features

* Three-stage Class-AB amplifier architecture
* Non-inverting voltage amplification stage
* Four-diode Class-AB bias network
* Complementary Darlington push-pull output stage
* Global negative feedback
* Low crossover distortion
* Low THD audio amplification
* Efficient power delivery into an 8 Ω load

---

# 🏗️ Amplifier Architecture

The amplifier consists of three functional stages.

---

## 🔵 Stage 1 – Voltage Amplification Stage

### Components

* UniversalOpamp2
* Input coupling capacitor
* Feedback network
* Supply decoupling capacitors

### Functions

* Amplifies the low-level audio input signal
* Provides high input impedance
* Generates the required voltage gain
* Drives the output power stage
* Global negative feedback improves linearity and stability

---

## 🟢 Stage 2 – Four-Diode Class-AB Bias Network

### Components

* Four 1N4148 Diodes
* Bias Resistors
* Interstage Coupling Capacitors

### Functions

* Establishes proper Class-AB operation
* Generates the required bias voltage for the Darlington output stage
* Keeps both output transistors slightly conducting around the zero-crossing region
* Significantly reduces crossover distortion

### Bias Voltage

The Darlington output stage requires approximately four base-emitter voltage drops.

```text
Vbias ≈ 4 × 0.7 V ≈ 2.8 V
```

This bias voltage ensures smooth transition between positive and negative half-cycles.

---

## 🟠 Stage 3 – Complementary Darlington Output Stage

### Components

* TIP31C Darlington Pair
* TIP32C Darlington Pair
* 0.5 Ω Emitter Resistors
* Output Coupling Capacitor
* 8 Ω Speaker Load

### Functions

* Provides high current gain
* Drives low-impedance speaker loads
* Delivers output power efficiently
* Reduces loading on the voltage amplification stage

### Why Darlington Pairs?

The complementary Darlington configuration was selected because it:

* Increases effective current gain
* Reduces base drive current requirements
* Improves load-driving capability
* Enables higher output power
* Maintains low distortion under large-signal operation

---

# 📊 Analyses Performed

* Transient Analysis
* AC Frequency Response
* Fourier (FFT) Analysis
* Output Power Analysis
* Supply Power Analysis
* Efficiency Evaluation
* Total Harmonic Distortion (THD) Measurement

---

# 📸 Circuit Schematic

*(<img width="1242" height="670" alt="image" src="https://github.com/user-attachments/assets/6a9a9472-150a-4001-89b8-58113f63fa15" />
.)*

**Figure 1:** Complete LTspice schematic of the Complementary Darlington Class-AB Audio Power Amplifier.

---

# 📈 Transient Analysis

*(Insert transient waveform image.)*

**Figure 2:** Input and output waveforms at 1 kHz.

### Observation

The amplifier provides voltage amplification while maintaining excellent waveform fidelity with minimal crossover distortion.

---

# ⚡ Output Power Analysis

*(Insert output power waveform.)*

**Figure 3:** Instantaneous load power delivered to the 8 Ω speaker.

### Measured Result

| Parameter            | Value      |
| -------------------- | ---------- |
| Average Output Power | **4.82 W** |

The amplifier delivers nearly **5 W** of continuous output power into an 8 Ω load.

---

# 🔋 Supply Power Analysis

*(Insert supply power waveform.)*

**Figure 4:** Total power drawn from the ±12 V supply rails.

### Measured Result

| Parameter           | Value      |
| ------------------- | ---------- |
| Average Input Power | **9.07 W** |

---

# 📊 Efficiency Analysis

The overall efficiency is calculated using

```text
η = (Pout / Pin) × 100
```

Using measured values,

```text
η = (4.82 / 9.07) × 100

η = 53.1 %
```

### Measured Result

| Parameter  | Value      |
| ---------- | ---------- |
| Efficiency | **53.1 %** |

The measured efficiency is consistent with the expected performance of a discrete Class-AB power amplifier employing a complementary Darlington output stage.

---

# 🎼 Fourier Analysis & THD

*(Insert FFT image.)*

**Figure 5:** Fourier spectrum of the amplifier output.

### Measured Result

| Parameter             | Value      |
| --------------------- | ---------- |
| Fundamental Frequency | **1 kHz**  |
| THD                   | **0.08 %** |

### Observation

The very low THD demonstrates:

* Proper Class-AB biasing
* Effective reduction of crossover distortion
* Good linearity of the Darlington output stage
* High-quality audio amplification

---

# 📋 Performance Summary

| Parameter       | Value                    |
| --------------- | ------------------------ |
| Supply Voltage  | ±12 V                    |
| Load Resistance | 8 Ω                      |
| Output Power    | **4.82 W**               |
| Input Power     | **9.07 W**               |
| Efficiency      | **53.1 %**               |
| THD             | **0.08 %**               |
| Output Stage    | Complementary Darlington |
| Bias Network    | Four-Diode Class-AB      |
| Simulation Tool | LTspice XVII             |

---

# 🛠️ Design Highlights

* Implemented a three-stage Class-AB amplifier using a complementary Darlington output stage.
* Utilized a four-diode bias network to minimize crossover distortion.
* Applied global negative feedback to improve gain accuracy and waveform linearity.
* Evaluated amplifier performance through transient, AC, FFT, power, and efficiency analyses.
* Achieved low harmonic distortion while delivering nearly **5 W** into an **8 Ω** speaker load.

---

# 🚀 Future Improvements

* Replace the diode bias network with a VBE multiplier for adjustable thermal biasing.
* Design and fabricate a PCB.
* Add speaker protection circuitry.
* Perform thermal analysis of the output transistors.
* Compare Darlington and Sziklai output stages.
* Improve efficiency using optimized biasing techniques.

---

# 📂 Repository Structure

```text
├── LTspice_Files
│   ├── AUDIO_AMPLIFIER_CIRCUIT.asc
│   ├── AUDIO_AMPLIFIER_CIRCUIT.net
│
├── Images
│   ├── schematic.png
│   ├── transient_response.png
│   ├── output_power.png
│   ├── input_power.png
│   ├── efficiency.png
│   ├── fft_analysis.png
│   └── ac_response.png
│
├── README.md
└── LICENSE
```

---

# 👨‍💻 Author

**Aditya**

**B.Tech Electronics Engineering**

**Interests:** Analog IC Design • Audio Power Amplifiers • CMOS Analog Circuits • LTspice Simulation
