# ESP32 Development Board PCB — Original 2-Layer Design

## Overview

A custom ESP32-WROOM-32E development board designed using **KiCad 9**, created to explore schematic capture, component selection, PCB layout, routing, and embedded hardware design.

This is the **original 2-layer PCB revision**, before the later enhanced-placement redesign.

## Features

- **Microcontroller:** ESP32-WROOM-32E with integrated Wi-Fi and Bluetooth
- **USB interface:** USB-C connector
- **USB-to-UART bridge:** CP2102N for programming and serial communication
- **Power regulation:** AMS1117-3.3 V regulator
- **GPIO access:** Expansion header for external peripherals
- **Programming controls:** BOOT and RESET push buttons
- **User indication:** Onboard LED
- **PCB design:** Two copper layers — front and back

## Hardware Design

The board integrates the ESP32 module with its supporting power, programming, and GPIO circuitry. The design brings the main connections needed for embedded development into a custom PCB.

## Design Tools

- KiCad 9 Schematic Editor
- KiCad 9 PCB Editor
- KiCad 3D Viewer
- Electrical Rules Checker (ERC)
- Design Rules Checker (DRC)

## PCB Design Workflow

1. Schematic capture and component selection
2. Footprint assignment
3. Component placement
4. Two-layer PCB routing
5. Copper-zone configuration
6. Electrical and design-rule checks
7. 3D visualization and layout review

## Project Files

This directory contains the design files and visual documentation for the original revision.

- KiCad schematic (`.kicad_sch`)
- KiCad PCB layout (`.kicad_pcb`)
- PCB layout screenshots
- 3D visualization, where available

## Project Status

The original PCB design was subsequently used as the basis for a four-layer redesign with enhanced placement and additional board features.

Fabrication and hardware validation should be recorded separately once completed.

## Future Improvements

- Refine component placement and routing
- Review manufacturability and electrical clearances
- Fabricate and assemble the PCB
- Validate USB programming, power regulation, and GPIO functionality on hardware

---

**Tools:** KiCad 9 · ESP32 · PCB Design · Schematic Capture · Routing · Embedded Systems
