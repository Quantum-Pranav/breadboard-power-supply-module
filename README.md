# 🔌 Breadboard Power Supply Module (Custom MB102 Replacement)

A compact multi-output DC–DC breadboard power module designed as an improved alternative to the widely used MB102 power board. This project covers the complete hardware development cycle—from circuit design and PCB layout to fabrication, assembly, and experimental validation.

---

## 📷 Finished Hardware

<p align="center">
<img src="Images/final_board.jpg" width="700">
</p>

*Fabricated and assembled breadboard power module.*

---

## 📖 Overview

The objective of this project was to design a reliable breadboard power module capable of providing multiple regulated voltage rails for embedded systems and electronics prototyping while incorporating proper protection, filtering, and PCB layout practices for switching power supplies.

---

## ✨ Features

* Dual DC input

  * 12 V Barrel Jack
  * 5 V Micro-USB
* Adjustable Buck Converter (TI TPS54202)

  * **0.8 V – 11 V**
  * **~1.7 A Output**
* 5 V Buck-Boost Converter (TI TPS63060)
* 3.3 V LDO (TI TLV1117-33)
* Resettable 1.1 A PPTC Polyfuses
* Ferrite Bead Output Filtering
* Dedicated 5 V, 3.3 V and Adjustable Outputs

---

## 🔧 Circuit Design

<p align="center">
<img src="Images/schematic.png" width="900">
</p>

*Complete schematic of the breadboard power module.*

---

## 🖥 PCB Design

<p align="center">
<img src="Images/pcb_3d.png" width="750">
</p>

The PCB was designed in **Altium Designer** using SMD components and optimized for switching regulator performance.

### Layout Highlights

* Minimized switching current loops
* Solid ground strategy
* Isolated feedback routing
* Proper decoupling capacitor placement
* EMI-conscious component placement
* Wide power traces for high-current paths

---

## 📊 Experimental Results

<p align="center">
<img src="Images/oscilloscope.png" width="800">
</p>

### Measured Performance

| Parameter              | Value     |
| ---------------------- | --------- |
| Adjustable Output      | 0.8–11 V  |
| Maximum Current        | ~1.7 A    |
| Adjustable Rail Ripple | ~200 mVpp |
| 5 V Rail Ripple        | ~111 mVpp |

---

## ⚠️ Design Challenges

During hardware validation, noticeable EMI susceptibility was observed around the switching regulator. This project emphasized the importance of:

* Switching loop minimization
* Return current paths
* Feedback routing
* EMI-aware PCB layout
* Practical hardware debugging

Future revisions will focus on improving electromagnetic compatibility and reducing output ripple.

---

## 🛠 Technologies Used

* Altium Designer
* PCB Design
* Power Electronics
* TI TPS54202
* TI TPS63060
* TI TLV1117-33
* EMI & Noise Analysis

---

## 📂 Repository Structure

```text
Images/
├── final_board.jpg
├── schematic.png
├── pcb_3d.png
└── oscilloscope.png

Hardware/
├── Schematic.pdf
├── PCB.pdf
├── Gerbers.zip
├── BOM.xlsx
└── Test_Report.pdf

Altium/
└── Source Files
```

---

## 🚀 Future Improvements

* Improve EMI performance
* Reduce output ripple
* Thermal characterization under load
* Add output current monitoring
* Improve PCB layout for switching regulators

---

## 📄 License

This project is released under the MIT License.
