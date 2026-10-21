# ESP32 Development Board — 4-Layer PCB Design

## Overview

A custom ESP32 development board designed using **KiCad 9**, featuring a four-layer PCB layout, USB-C connectivity, USB-to-UART programming, power regulation, GPIO expansion, and a CAN communication interface.

The project focuses on practical embedded hardware development, schematic design, component selection, PCB placement, multilayer routing, and design-rule verification.

## Features

- **Microcontroller:** ESP32-WROOM-32E
- **USB connectivity:** USB-C connector
- **USB-to-UART bridge:** CP2102N for programming and serial communication
- **Power regulation:** AMS1117-3.3 V regulator
- **GPIO expansion:** Header for external peripheral connections
- **Programming controls:** BOOT and RESET push buttons
- **User indication:** Onboard LED
- **CAN communication:** SN65HVD230 CAN transceiver
- **CAN bus protection:** NUP2105L protection device
- **CAN termination:** 120 Ω termination resistor with jumper configuration
- **CAN connection:** 3-pin screw terminal connector
- **Mechanical design:** Four corner mounting holes
- **PCB construction:** Four copper layers

## Hardware Design

### ESP32 Core
The ESP32-WROOM-32E serves as the main controller, providing processing and wireless connectivity capabilities for embedded applications.

### USB and Programming Interface
The USB-C connector and CP2102N USB-to-UART bridge provide an interface for firmware programming and serial communication.

### Power Supply
An AMS1117-3.3 V regulator provides the 3.3 V supply for the board's circuitry.

### CAN Communication Interface
The board incorporates an SN65HVD230 CAN transceiver, NUP2105L protection device, configurable 120 Ω termination, and a 3-pin screw terminal for CAN bus connections.

This interface provides a hardware foundation for exploring CAN communication between embedded devices.

### GPIO and User Controls
GPIO headers provide access to selected ESP32 pins for connecting external peripherals. BOOT and RESET buttons support programming and resetting the controller, while the onboard LED provides visual indication.

## Four-Layer PCB Stackup

| Layer | Purpose |
|---|---|
| F.Cu | Top copper layer |
| In1.Cu | Inner copper layer |
| In2.Cu | Inner copper layer |
| B.Cu | Bottom copper layer |

The four-layer layout provides additional routing flexibility and supports internal copper planes according to the board's layer configuration.

## Design Tools

- KiCad 9 Schematic Editor
- KiCad 9 PCB Editor
- KiCad 3D Viewer
- Electrical Rules Checker (ERC)
- Design Rules Checker (DRC)

## Design Workflow

1. Schematic capture and component selection
2. Footprint assignment and component placement
3. Four-layer PCB configuration
4. PCB routing and copper-zone configuration
5. Placement of connectors, user controls, and mounting holes
6. ERC and DRC checks
7. Clearance, silkscreen, and layout review
8. 3D visualization of the PCB

## Design Verification

The PCB layout was reviewed using KiCad's Electrical Rules Checker and Design Rules Checker to identify potential design issues and improve layout quality.

## Repository Contents

- KiCad schematic file (`.kicad_sch`)
- KiCad PCB layout file (`.kicad_pcb`)
- KiCad project file (`.kicad_pro`)
- PCB layout screenshots
- 3D PCB visualizations

## Project Status

The project has progressed through schematic development, four-layer PCB layout, component placement, routing, and design-rule review.

Fabrication, assembly, and physical hardware validation will be documented after the PCB is manufactured and tested.

## Future Improvements

- Complete the final manufacturability and clearance review
- Fabricate and assemble the PCB
- Test USB programming and power regulation
- Validate GPIO functionality
- Test CAN communication with compatible hardware
- Document test results and any required design revisions

---

**Tools and technologies:** KiCad 9 · ESP32-WROOM-32E · CP2102N · USB-C · SN65HVD230 · CAN Bus · Four-Layer PCB · Embedded Hardware Design

