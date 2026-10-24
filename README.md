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

<img width="933" height="843" alt="esp32_pcb_angle" src="https://github.com/user-attachments/assets/8294ec80-5dcc-45e2-81c9-c1a1fc53c718" />
<img width="854" height="905" alt="esp32_pcb_topview" src="https://github.com/user-attachments/assets/42cf75d2-ab2a-41cd-9db5-74e7a35fd9d2" />

## Four-Layer PCB Layout

### 1. Front Copper — F.Cu

<img width="764" height="849" alt="esp32_F cu" src="https://github.com/user-attachments/assets/c7b3bdb0-cc2d-4155-af45-90b8025b94ec" />

### 2. Inner Copper 1 — In1.Cu

<img width="788" height="845" alt="esp32_In1 Cu" src="https://github.com/user-attachments/assets/3de58c02-2180-434a-8824-a955221cd762" />

### 3. Inner Copper 2 — In2.Cu

<img width="764" height="845" alt="esp32_In2 Cu" src="https://github.com/user-attachments/assets/ba35d087-3cbd-44fe-b6d9-761849f5938e" />

### 4. Back Copper — B.Cu

<img width="750" height="835" alt="esp32_B cu" src="https://github.com/user-attachments/assets/4cee9322-e1f8-4beb-ab8d-0bb215522235" />

## Schematic

<img width="1307" height="887" alt="esp32_schematic" src="https://github.com/user-attachments/assets/44f1b864-2949-40ed-b747-a1082e54b3f6" />

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

