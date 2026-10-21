# ESP32 Development Board PCB — 4-Layer Version

## Overview

A custom ESP32-WROOM-32E development board designed using KiCad 9 to explore multilayer PCB design, component placement, routing, and embedded hardware integration.

This revision introduces a **four-layer PCB stackup** while retaining the core ESP32 development-board functionality. It represents an intermediate design stage before the subsequent enhanced-placement redesign.

## Features

- **Microcontroller:** ESP32-WROOM-32E
- **USB connectivity:** USB-C interface
- **USB-to-UART bridge:** CP2102N
- **Power regulation:** AMS1117-3.3 V
- **GPIO expansion:** Header for external peripherals
- **Programming controls:** BOOT and RESET buttons
- **User indication:** Onboard LED
- **PCB construction:** Four copper layers

## PCB Stackup

| Layer | Purpose |
|---|---|
| F.Cu | Top copper layer |
| In1.Cu | Inner copper layer |
| In2.Cu | Inner copper layer |
| B.Cu | Bottom copper layer |

The four-layer structure provides additional routing flexibility and space for internal copper planes.

## Design Tools

- KiCad 9 Schematic Editor
- KiCad 9 PCB Editor
- KiCad 3D Viewer
- Electrical Rules Checker (ERC)
- Design Rules Checker (DRC)

## Design Workflow

1. Schematic capture and footprint assignment
2. Four-layer board configuration
3. Component placement
4. Signal routing across copper layers
5. Internal copper-zone configuration
6. Design-rule checking
7. 3D visualization and layout review

## Project Files

- KiCad schematic (`.kicad_sch`)
- Four-layer PCB layout (`.kicad_pcb`)
- PCB layout screenshots
- 3D board visualization, where available

## Learning Outcomes

- Understanding multilayer PCB stackups
- Working with internal copper layers and copper planes
- Managing component placement and signal routing
- Using KiCad ERC and DRC tools
- Reviewing PCB layouts for design and manufacturability

## Project Status

This is an intermediate four-layer design revision. The later enhanced-placement version is maintained separately.

Fabrication and physical hardware validation will be documented once completed.

---

**Tools and technologies:** KiCad 9 · ESP32 · USB-C · CP2102N · Four-Layer PCB · PCB Layout · Embedded Systems
