# 🖥️ RISC-V SoC Tapeout Journey — VSD Program

<div align="center">

[![RISC-V](https://img.shields.io/badge/RISC--V-SoC-blue?style=for-the-badge\&logo=riscv)](https://github.com/riscv/learn)
[![VSD](https://img.shields.io/badge/VSD-Program-orange?style=for-the-badge)](https://www.vlsisystemdesign.com/)
[![Progress](https://img.shields.io/badge/Weekly%20Tasks-Documented-success?style=for-the-badge)](https://github.com/Nideshkanna/riscv-soc-tapeout)
[![Open-Source](https://img.shields.io/badge/Open--Source-EDA%20Tools-brightgreen?style=for-the-badge)](https://vlsiresources.com/opensourcevlsi/)

</div>

Welcome to my documentation of the **RISC-V SoC Tapeout Program by VSD** 🚀
This repository serves as the **main tracker** of my weekly tasks, with each week maintained in a **separate GitHub repository** for clarity and grading.

<div align="center">

> *"From RTL to GDSII, we design silicon step by step, mastering open-source tools and contributing to India’s largest collaborative RISC-V tapeout initiative."* ⚡

</div>

---

## 📂 Repository Structure

Each week has its own dedicated repository:

| Week        | Focus Area                                     | Repository Link                                                            | Status        |
| ----------- | ---------------------------------------------- | -------------------------------------------------------------------------- | ------------- |
| **Week 0**  | 🔧 Environment Setup & Tool Installation       | [Week0](https://github.com/Nideshkanna/week0-getting-started)              | ✅ Done        |
| **Week 1**  | 📝 RTL Design Flow                             | [Week1](https://github.com/Nideshkanna/week1-rtl-design-flow)              | ✅ Completed   |
| **Week 2**  | 🔄 BabySoC Functional Verification & Synthesis | [Week2](https://github.com/Nideshkanna/week2-research-babysoc) | ✅ Completed   |
| **Week 3**  | 🏗️ STA & Timing Analysis                      | [Week3](https://github.com/Nideshkanna/week3_VSDBabySoC_GLS_STA)        | ✅ Completed   |
| **Week 4**  | ⚡ CMOS Circuit Design (sky130)                 | [Week4](https://github.com/Nideshkanna/week4_CMOS_Circuit_Design_sky130)   | ⏳ In Progress |
| **Week 5+** | 🎯 Tapeout Prep & Sign-off                     | *(Upcoming)*                                                               | ⏳ Pending     |

---

## 📅 Week 0 — Tools Setup

📌 **Focus:** Installing and verifying the open-source EDA toolchain on Ubuntu 22.04

| Tool               | Purpose                   | Status      |
| ------------------ | ------------------------- | ----------- |
| **Yosys**          | RTL Synthesis             | ✅ Installed |
| **Icarus Verilog** | Simulation & Testbench    | ✅ Installed |
| **GTKWave**        | Waveform Viewer           | ✅ Installed |
| **Ngspice**        | Circuit Simulation        | ✅ Installed |
| **Magic**          | Layout & DRC              | ✅ Installed |
| **OpenLane**       | Complete RTL → GDSII Flow | ✅ Installed |

### 🌟 Key Learnings

* Set up the **open-source EDA toolchain** on Ubuntu 22.04.
* Understood the **role of each tool** in the RTL-to-GDSII flow.
* Verified installation with **sample test runs**.
* Prepared the environment for **Week 1 RTL design tasks**.

---

## 📅 Week 1 — RTL Design Basics

📌 **Focus:** Writing, simulating, and synthesizing basic Verilog designs

| Task                          | Description                                         | Status      |
| ----------------------------- | --------------------------------------------------- | ----------- |
| **Verilog Coding**            | Designed simple combinational & sequential circuits | ✅ Completed |
| **Icarus Verilog Simulation** | Simulated RTL with testbenches                      | ✅ Completed |
| **GTKWave Analysis**          | Observed waveforms to validate outputs              | ✅ Completed |
| **Yosys Synthesis**           | Generated synthesized netlists                      | ✅ Completed |
| **Logic Optimization**        | Understood combinational & sequential optimizations | ✅ Completed |

### 🌟 Key Learnings

* Gained hands-on practice with **RTL design using Verilog**.
* Learned how to build **testbenches** and simulate using **Icarus Verilog**.
* Used **GTKWave** for waveform visualization and debugging.
* Ran **Yosys synthesis** to convert RTL to a gate-level netlist.
* Explored the **importance of optimizations** in reducing area, power, and delay.

📌 *Next up: Week 2 — BabySoC Functional Verification & Synthesis* 🚀

---

## 📅 Week 2 — Pre-Synthesis Simulation & Synthesis

📌 **Focus:** Functional verification and RTL synthesis for BabySoC

| Task                         | Description                                                         | Status      |
| ---------------------------- | ------------------------------------------------------------------- | ----------- |
| **Project Setup**            | Configured VSDBabySoC environment and module hierarchy              | ✅ Completed |
| **Pre-Synthesis Simulation** | Fixed duplicate module issues; ran `iverilog` to generate waveforms | ✅ Completed |
| **Yosys Synthesis**          | Executed synthesis script; generated `vsdbabysoc.synth.v`           | ✅ Completed |

### 🌟 Key Learnings

* Verified RTL functionality prior to synthesis.
* Learned **file management** and testbench debugging in large RTL projects.
* Produced a **synthesized netlist** ready for STA analysis.

📌 *Outcome:* BabySoC RTL is verified and synthesized — ready for timing analysis (Week 3).

---

## 📅 Week 3 — STA & Timing Analysis

📌 **Focus:** Static Timing Analysis using OpenSTA across multiple PVT corners

| Task                     | Description                                       | Status      |
| ------------------------ | ------------------------------------------------- | ----------- |
| **OpenSTA Setup**        | Configured Docker environment and library paths   | ✅ Completed |
| **TCL Script Execution** | Ran `sta_across_pvt.tcl` to analyze timing        | ✅ Completed |
| **Slack Analysis**       | Extracted setup/hold slack for TT, SS, FF corners | ✅ Completed |

### 🌟 Key Learnings

* Learned **STA fundamentals** and multi-corner timing checks.
* Observed **minor hold violations** in fast corner; typical and slow corners passed.
* Reinforced the importance of **complete input/output constraints**.

📌 *Outcome:* STA validated; design timing closure achieved across major paths.

---

## 📅 Week 4 — CMOS Circuit Design (sky130)

📌 **Focus:** SPICE-level CMOS design experiments with Sky130 PDK

| Task                          | Description                                | Status        |
| ----------------------------- | ------------------------------------------ | ------------- |
| **MOSFET IV Characteristics** | Simulate Id vs Vds for NMOS/PMOS           | ⏳ In Progress |
| **CMOS Inverter VTC**         | Extract switching threshold, noise margins | ⏳ In Progress |
| **Transient Delays**          | Rise/fall propagation delays               | ⏳ In Progress |
| **Supply & Sizing Variation** | Observe impact on VTC, delays, margins     | ⏳ In Progress |

### 🌟 Key Learnings

* Deepen understanding of **device physics and its impact on timing**.
* Prepare intuition for **post-layout STA & critical path optimization**.

📌 *Next step:* Complete Week 4 experiments and document plots, tables, and observations.

---

## 📈 Progress Tracker

<div align="center">

[![Week 0](https://img.shields.io/badge/Week%200-✅%20Done-green?style=flat-square)](https://github.com/Nideshkanna/week0-getting-started)
[![Week 1](https://img.shields.io/badge/Week%201-✅%20Completed-green?style=flat-square)](https://github.com/Nideshkanna/week1-rtl-design-flow)
[![Week 2](https://img.shields.io/badge/Week%202-✅%20Completed-green?style=flat-square)](https://github.com/Nideshkanna/week2-research-babysoc)
[![Week 3](https://img.shields.io/badge/Week%203-✅%20Completed-green?style=flat-square)](https://github.com/Nideshkanna/week3_VSDBabySoC_GLS_STA)
[![Week 4](https://img.shields.io/badge/Week%204-In%20Progress-blue?style=flat-square)](https://github.com/Nideshkanna/week4_CMOS_Circuit_Design_sky130)
![Week 5+](https://img.shields.io/badge/Week%205+-Upcoming-blue?style=flat-square)

</div>

---

## 🙏 Acknowledgments

I am grateful to:

* [**Kunal Ghosh**](https://github.com/kunalg123) and the **[VSD team](https://vsdiat.vlsisystemdesign.com/)**
* **RISC-V International** and **Efabless**
* The open-source **EDA community** for making this initiative possible

---

## 🚀 Next Steps

* Complete **Week 4: CMOS Circuit Design experiments** (SPICE VTC, delays, variation analysis).
* Analyze results to gain intuition for **timing and noise margins**.
* Prepare for **Week 5+ Tapeout prep & post-layout STA**.

---

👨‍💻 **Maintainer:** [Nidesh Kanna R](https://github.com/Nideshkanna)

📌 **Part of:** [RISC-V SoC Tapeout Program](https://github.com/Nideshkanna/riscv-soc-tapeout)

---
