# Hi, I'm Mageshwar R 👋

**B.E. Electrical & Electronics Engineering** · Meenakshi Sundararajan Engineering College, Chennai — CGPA: 8.46  
**B.Sc. Electronic Systems** · IIT Madras (Online) — CGPA: 7.31

I build things at the intersection of **hardware and software** — bare-metal firmware, custom PCBs, Linux systems programming, and applied ML on edge devices. My long-term goal is fusion energy research, working toward a German Masters in plasma/nuclear engineering en route to ITER.

---

## 🏆 Awards

- 🥇 **1st Place — Circuit Design, SPARK '26 (IIT Madras)** — Designed a linear sensor signal-conditioning circuit (non-inverting level shifter + scaler) to interface a ±0.7 V sensor to a 0–5 V ADC
- 🥈 **2nd Place — Rapid Prototyping, SPARK '26 (IIT Madras)** — ESP32-C3 + TFT reaction game: Wokwi simulation → EasyEDA PCB → Onshape enclosure
- 🥈 **2nd Place — Youth Scientist Conference '25 (MSEC)** — Paper on bio-electricity / bio-fuel cell from human urine
- 🥉 **3rd Place — AI-Based 3D Modeling Contest (MSEC)** — Graphene–piezoelectric exosleeve wearable glove

---

## 🔧 What I Work With

**Languages**
`C` `Embedded C` `C++` `Python` `MATLAB` `Bash` `TCL`

**Hardware & Embedded**
`STM32 (BluePill, Nucleo F7, H743)` `ESP32` `Arduino` `ADE9000` `MPU6050`
`UART / SPI / I2C` `MQTT` `nl80211 / IEEE 802.11` `PCB Design`

**Tools & Platforms**
`STM32CubeIDE` `STM32CubeMX` `KiCad` `Altium Designer (Certified)` `EasyEDA Pro`
`Vivado / Vitis` `PlatformIO` `LTspice` `OrCAD X` `MATLAB/Simulink` `Wokwi` `Onshape` `Fusion 360`

**Linux Systems**
`Arch Linux` `systemd` `Bash` `procfs/sysfs` `Generic Netlink / nl80211` `SSH tunnelling` `Tailscale VPN` `xfreerdp`

---

## 🚀 Projects

### ⚡ Calton — 3-Phase AC Energy Monitor *(In Progress)*
Custom hardware energy monitoring system using the **ADE9000** metering IC and **STM32H743ZIT6TR** microcontroller. Full custom KiCad schematic with isolated voltage sensing (resistor divider + AMC1301 isolated amplifier, gain 8.2×), MOV surge protection, SPI4 interface, and B0505S isolated DC-DC power. Targeting IEC 62053 / EN 50160 compliance.
> `STM32H743` `ADE9000` `SPI` `KiCad` `AMC1301` `Power Metering`

---

### 📡 [SparkSense](https://github.com/m4g3shw4r/Sparksense) — ESP32 Motor Condition Monitor *(In Progress)*
Multi-sensor IoT platform for predictive maintenance of AC/DC machines. ESP32 firmware in C++ interfacing MPU6050 vibration (I2C), DHT22, current/voltage sensors; relay auto-shutoff, OLED UI (SPI), MQTT cloud telemetry. Edge-based anomaly detection using **TinyML** on-device inference — no cloud round-trip required.
> `ESP32` `C++` `TinyML` `MQTT` `I2C` `SPI` `IoT` `Predictive Maintenance`

📄 *Co-authoring: "SparkSense: A TinyML-Enabled Multi-Sensor Predictive Maintenance Platform" — In Preparation*

---

### 📶 [wifi-beacon-scanner](https://github.com/m4g3shw4r/wifi-beacon-scanner) — IEEE 802.11 BSS Scanner
Linux nl80211 Generic Netlink Wi-Fi scanner in C. Triggers active scans via raw NL80211 sockets (same kernel API as `iw`/`wpa_supplicant`), manually parses 802.11 IE TLVs (SSID, RSN/WPA2, WPA1 vendor OUI), decodes capability bits. Colour-coded live dashboard sorted by signal strength. Zero external dependencies beyond libnl.
> `C` `Linux` `nl80211` `Generic Netlink` `IEEE 802.11` `Raw Sockets`

---

### 🔁 [ring-buffer-uart-sim](https://github.com/m4g3shw4r/ring-buffer-uart-sim) — Lock-Free Ring Buffer + UART Simulator
Power-of-2 ring buffer with branchless index masking for lock-free SPSC operation — same architecture as STM32 HAL circular DMA buffers. UART frame encoder/decoder on top: configurable baud, 7/8 data bits, None/Odd/Even parity, 1/2 stop bits, bitmask error flags. Tested 115200 8N1, 9600 8E1 framing-error injection, 57600 7O2.
> `C` `Embedded` `UART` `Ring Buffer` `DMA` `-Wall -Wextra -Wpedantic`

---

### 📊 [netif-monitor](https://github.com/m4g3shw4r/netif-monitor) — Linux Network Interface Monitor
Parses `/proc/net/dev` directly in C (no subprocesses) for all 16 per-interface RX/TX fields; computes delta-based throughput between snapshots — same technique used in embedded Linux gateway firmware. Flicker-free ANSI dashboard with auto-scaling (B/KB/MB/GB), colour-coded by activity and error state.
> `C` `Linux` `procfs` `Systems Programming` `Networking`

---

### 🖥️ [remote-fpga-dev](https://github.com/m4g3shw4r/remote-fpga-dev) — Remote FPGA Development Environment
Full documentation and automation scripts for accessing a Windows FPGA workstation (Vivado/Vitis, 200 GB install) from Arch Linux over a **Tailscale VPN** tunnel — SSH for CLI batch builds, RDP-over-SSH-tunnel for full GUI. Includes TCL batch build scripts covering synthesis → placement → routing → bitstream.
> `Bash` `SSH` `Tailscale` `FreeRDP` `Vivado` `TCL` `WireGuard`

---

### 🔍 [Li-Sense-Detect](https://github.com/m4g3shw4r/Li-Sense-Detect) — Real-Time ANPR on Raspberry Pi 5
Two-stage detection + OCR pipeline on **Raspberry Pi 5**: PiCamera2 capture, contour-based plate localisation, Tesseract OCR. Timestamped entry/exit logging with persistent SQLite storage. Profiled and optimised for ARM Cortex-A76 latency using grayscale, adaptive threshold, and morphological preprocessing.
> `Python` `Raspberry Pi 5` `OpenCV` `Tesseract OCR` `SQLite` `Edge ML` `ARM Cortex-A76`

📄 *"Li-Sense Detect: Real-Time License Plate Recognition System Using Raspberry Pi 5" — Nov 2025*

---

### 🌡️ [Energy-Automation-PID-Building-Simulation](https://github.com/m4g3shw4r/Energy-Automation-PID-Building-Simulation)
Occupancy-based lighting + PID HVAC temperature control modeled over a 24-hour cycle in MATLAB/Octave, with full energy (kWh) and cost reporting.
> `MATLAB` `PID Control` `Simulink` `Energy Systems`

---

### 📻 Compact Function Generator
Portable analog signal generator fabricated and tested on a DSO. Generates sine/square/triangle waveforms across **10 Hz – 450 kHz**; validated amplitude stability and signal integrity.
> `Analog Electronics` `PCB` `Signal Generation` `Oscilloscope`

---

## 💼 Internships

**North Chennai Thermal Power Station (NCTPS-I)** · Engineering Intern · *Jun – Jul 2025*
Analyzed real-time DCS/SCADA pipelines for 230 kV switchyard equipment (CT/PT/CVT, breakers/isolators); studied protection relay testing (IR/Megger), meter calibration, and Permit-to-Work safety protocols in a live HV environment.

**Chennai Metro Rail Limited (CMRL)** · Engineering Intern · *Jan – Feb 2025*
Analyzed MEP infrastructure (HVAC, AHU, server cooling) across metro depots; studied OCC/SCADA monitoring for real-time metro-scale fault detection across distributed embedded systems.

---

## 🌱 Currently

- Completing **Calton** PCB design (ADE9000 + STM32H743) — targeting IEC 62053 compliance
- Semester 6 EEE — Power Electronics, Power System Protection, Data Science
- NPTEL: Embedded System Design with ARM · Embedded Sensing & Interfacing · Programming in C
- **Altium Designer Certified** · NPTEL Advanced Power Electronics — Elite
- Treasurer, **Renewables Club** — MSEC

---

## 🎯 Long-Term Goal

Fusion energy research at **ITER, France** — via a German Masters (targeting Erasmus Mundus **FUSION-EP / STEPS**, TU Munich, KIT Karlsruhe, University of Stuttgart).

---

## 📫 Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Mageshwar_R-0077B5?style=flat&logo=linkedin)](https://www.linkedin.com/in/m4g3shw4r)
[![GitHub](https://img.shields.io/badge/GitHub-m4g3shw4r-181717?style=flat&logo=github)](https://github.com/m4g3shw4r)

*Open to internships and collaboration on embedded systems, power electronics, and energy projects.*
