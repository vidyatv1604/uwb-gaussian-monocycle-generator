#  UWB Gaussian Monocycle Pulse Generator

##  Overview
This project presents the design and implementation of a **low-ringing Gaussian monocycle pulse generator** suitable for **Ultra-Wideband (UWB) applications up to 3 GHz**.

The system converts an input trigger signal into a **clean, broadband monocycle pulse** using RF/microwave design techniques such as **SRD-based impulse generation, microstrip transmission lines, and bandpass filtering**.


##  Objectives
- Generate **Gaussian monocycle pulses** for UWB systems  
- Achieve **low ringing and high spectral efficiency**  
- Implement **RF/microwave-based pulse shaping techniques**  
- Design a **compact PCB-based hardware system**


##  System Architecture

       Input Square Pulse---->SRD Based circuit/Mlin---->Band Pass Filter---->Output Monocycle

##  Functional Blocks

### 1️⃣ Input Excitation Source
- Provides the triggering signal (clock/input pulse)
- Typically derived from a **10 MHz oscillator**

### 2️⃣ Schmitt Trigger (Signal Conditioning)
- Converts noisy input into a **clean digital waveform**
- Ensures **sharp transitions for pulse generation**
- IC Used: `SN74LVC1G17`

### 3️⃣ SRD-Based Impulse Generator
- Core of the system
- Uses **Step Recovery Diode (SRD)** or **Schottky diode (BAT721-A)**
- Generates **narrow high-frequency impulses**

### 4️⃣ Microstrip Transmission Line
- Acts as distributed **R, L, C network**
- Controls pulse shaping, delay, and impedance matching  

### 5️⃣ Bandpass Filter (BPF)
- Converts impulse → **Gaussian monocycle pulse**
- Removes unwanted frequency components
- Designed using **Chebyshev response**

### 6️⃣ Output Stage
- Produces **clean UWB Monocyle pulse (up to 3 GHz)**


##  Key Features
-  High-frequency operation (up to 3 GHz)  
-  Ultra-wideband pulse generation  
-  Low ringing output  
-  Compact RF PCB design  
-  Efficient impulse-to-monocycle conversion  

##  Hardware Components

| Component | Description |
|----------|------------|
| SN74LVC1G17 | Schmitt Trigger IC |
| BAT721-A | Schottky Diode (SRD alternative) |
| Crystal Oscillator | 10 MHz clock source |
| Microstrip Lines | RF transmission |
| Resistors | Biasing & current control |
| RF PCB | Substrate for layout |

## Hardware Implementation

A PCB layout is designed to validate the simulated results in hardware. 
High-frequency design considerations include:

- Controlled impedance microstrip lines
- Ground plane optimization
- Minimization of parasitic inductance and capacitance
- Proper RF filtering and shielding

Hardware validation will include time-domain pulse measurement and frequency response verification.


##  Applications
- UWB Communication Systems  
- Automotive Radar  
- RF & Microwave Research  
- Biomedical Imaging  
- Ground Penetrating Radar (GPR)  
