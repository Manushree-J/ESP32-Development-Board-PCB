 <div align="center">

# 👋 Hi, I'm Manushree J

**Electronics & Communication Engineering Student**

Interested in Embedded Systems, Firmware Development, and PCB Design.

[LinkedIn Profile](https://www.linkedin.com/in/manushree-j-83086035a/)

</div>

---

## About Me

I'm an Electronics and Communication Engineering student who enjoys learning through hands-on engineering projects. I'm particularly interested in embedded systems, microcontroller-based development, and hardware design.

I believe in learning through experimentation, refining designs through multiple iterations, and understanding the engineering decisions behind each project.

---

# Custom ESP32 Development Board

**ESP32-WROOM-32E | KiCad 9 | Four-Layer PCB | CAN Interface**

A custom ESP32 development board developed through multiple PCB design iterations, progressing from an initial two-layer layout to a four-layer design. The current revision focuses on component-placement changes and further PCB layout refinement.

## 3D PCB Views

<table>
  <tr>
    <td align="center" width="50%">
      <strong>Angled 3D View</strong><br>
      <img src="images/esp32_pcb_angle.png" alt="ESP32 PCB angled 3D view" width="100%">
    </td>
    <td align="center" width="50%">
      <strong>Top View</strong><br>
      <img src="images/esp32_pcb_topview.png" alt="ESP32 PCB top view" width="100%">
    </td>
  </tr>
</table>

## Four-Layer PCB Layout

### 1. Front Copper — F.Cu

![Front copper layer](images/esp32_F.cu.png)

### 2. Inner Copper 1 — In1.Cu

![Inner copper layer 1](images/esp32_In1.Cu.png)

### 3. Inner Copper 2 — In2.Cu

![Inner copper layer 2](images/esp32_In2.Cu.png)

### 4. Back Copper — B.Cu

![Back copper layer](images/esp32_B.cu.png)

## Schematic

![ESP32 development board schematic](images/esp32_schematic.png)

## Key Features

- ESP32-WROOM-32E microcontroller module
- USB-C connectivity with CP2102N USB-to-UART interface
- AMS1117-3.3 V voltage regulation
- GPIO expansion header
- BOOT and RESET buttons
- Onboard user LED
- SN65HVD230 CAN transceiver
- NUP2105L CAN bus protection
- Configurable 120 Ω CAN termination
- Three-pin CAN screw terminal
- Four corner mounting holes

## Design Evolution

This project documents three stages of development:

1. **Initial two-layer PCB:** Establishing the core ESP32 board architecture, USB connectivity, power supply, and GPIO access.
2. **Four-layer PCB:** Moving to a four-copper-layer stack-up.
3. **Current redesign:** Revisiting component placement and refining the overall layout, including the CAN interface.

The goal is to improve the design through iterative refinement and careful review of layout decisions.

## Engineering Work

- Schematic capture and component selection
- Footprint assignment and component placement
- Four-layer PCB stack-up and copper-layer layout
- Signal routing and copper-zone configuration
- Electrical Rule Check (ERC) and Design Rule Check (DRC)
- 3D visualization using KiCad
- Project documentation and version control using Git

## Project Status

**Ongoing — PCB design and layout refinement.**

The next steps include reviewing component placement and routing, checking design constraints, preparing the board for fabrication, and validating the assembled hardware.

Fabrication and physical hardware validation have not yet been completed.

## Tools Used

`KiCad 9` · `ESP32-WROOM-32E` · `CP2102N` · `SN65HVD230` · `NUP2105L` · `Git`

