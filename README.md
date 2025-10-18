# Embedded Hardware Development Workflow

This repository contains a simplified version of the typical workflow when developing hardware for an embedded system based on a microcontroller.

---

## 🧩 Overview

The goal of this repository is to provide an overview of a typical workflow for:

- **Requirement definition stage** (system specifications, component selection, definition of validation tests)
- **Hardware design stage** (schematics, PCB layout, and fabrication)
- **Testing and validation stage** (board bring-up, unit, integration, and HIL testing)

---

## 📁 Repository Structure

<pre>
├── <a href="0_Requirements">0_Requirements/</a>
│
├── <a href="1_Design-Data">1_Design-Data/</a>
│   ├── <a href="1_Design-Data/0_Hardware">0_Hardware/</a>
│   │   ├── <a href="1_Design-Data/0_Hardware/0_pre-schematic-reports">0_pre-schematic-reports/</a>
│   │   ├── <a href="1_Design-Data/0_Hardware/1_schematic">1_schematic/</a>
│   │   ├── <a href="1_Design-Data/0_Hardware/2_pcb">2_pcb/</a>
│   │   └── <a href="1_Design-Data/0_Hardware/3_fabrication-files">3_fabrication-files/</a>
│   │
│   └── <a href="1_Design-Data/1_Firmware">1_Firmware/</a> <i>(used in hybrid repositories)</i>
│
└── <a href="2_Validation">2_Validation/</a>
</pre>

---

## ⚙️ Hardware Development Workflow

1. **Requirements Definition**
   - Define top level requirements (e.g. number of inputs/outputs and or necessary communication protocols)
   - Specify MCU variant (e.g., ESP32-WROOM-32, ESP32-S3, STM32F4, etc).
   - Define I/O mapping and required peripherals (CAN, SPI, Wi-Fi, sensors, etc.).

2. **Schematic Design**
   - Tools: Altium Designer.
   - Use reference hardware design guidelines from Espressif/ST/others.
   - Include power regulation, input and output stages and any required physical communication layer (CAN, SPI, I2C).

3. **PCB Layout**
   - Follow each manufacturers design rules for trace length, component placement, ground planes, etc.
   - Perform DRC and ERC checks before Gerber generation.

4. **Fabrication & Assembly**
   - Export Gerbers, pick-and-place, and BOM files.
   - Validate part availability using component sourcing tools.

5. **Hardware Bring-Up**
   - Validate power rails, USB-UART communication, and flash memory.
   - Use adequate IDE to test module's IOs and peripherals with simple base code.

---

## 🧰 Tools and Dependencies

| Category | Tool | Description |
|-----------|------|-------------|
| Hardware | Altium | Schematic & PCB design |
| Firmware | PlatformIO or STM32CubeIDE | Build and deployment environment |
| Documentation | Doxygen / MkDocs | Code and design documentation |

---

## 📚 Documentation

- [Requirements Report](0_Requirements/0_Requirements-Report.pdf)
- [MCU Mapping Report](1_Design-Data/0_Hardware/0_pre-schematic-reports/0_MCU-Mapping-Report.pdf)
- [Validation Report](2_Validation/0_Validation-Report.pdf)

---

**Author:** [Joao Gaspar](https://github.com/joao-gaspar-7)
**Last Updated:** October 2025