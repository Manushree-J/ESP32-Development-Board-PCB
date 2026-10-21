# ESP32 Development Board | PCB Design & Hardware Development

A custom ESP32 development board designed using **KiCad 9**, documenting the progression from an initial two-layer PCB to four-layer designs and an enhanced hardware revision featuring a CAN communication interface.

This project demonstrates practical learning in electronic design, PCB layout, multilayer routing, design verification, and iterative hardware development.

## Project Overview

The objective of this project is to design and progressively improve a custom ESP32 development board while developing a deeper understanding of electronic hardware design and engineering workflows.

The repository captures three design stages, with each revision building on the previous one through exploration, refinement, and the application of new concepts.

## Design Evolution

### 01 — Original Two-Layer PCB

The initial revision established the core functionality of the custom development board.

**Key features**
- ESP32-WROOM-32E module
- USB-C connectivity
- CP2102N USB-to-UART interface
- AMS1117-3.3 V voltage regulator
- GPIO expansion header
- BOOT and RESET push buttons
- Onboard user LED
- Two-layer PCB layout

**Engineering focus:** Schematic capture, component selection, footprint assignment, component placement, PCB routing, and basic design verification.

### 02 — Four-Layer PCB

The second stage explored multilayer PCB design and the use of internal copper layers to improve routing flexibility.

**Key areas**
- Four-layer stackup configuration
- Component placement and signal routing
- Internal copper-layer planning
- Copper-zone configuration
- ERC and DRC checks
- Three-dimensional PCB visualization

**Engineering focus:** Multilayer PCB organization, routing strategies, copper-layer management, and design-rule analysis.

### 03 — Enhanced Four-Layer PCB with CAN Interface

The latest design stage extends the board's capabilities with a CAN communication interface and mechanical mounting provisions.

**Key features**
- ESP32-WROOM-32E module
- USB-C and CP2102N programming interface
- AMS1117-3.3 V power regulation
- GPIO expansion and user controls
- SN65HVD230 CAN transceiver
- NUP2105L CAN bus protection
- Configurable 120 Ω CAN termination
- Three-pin CAN screw terminal
- Four corner mounting holes
- Four-layer PCB layout

**Engineering focus:** Peripheral integration, communication-interface design, connector placement, mechanical considerations, and iterative PCB refinement.

## ESP32 GPIO Reference

The ESP32-WROOM-32E exposes GPIOs with different capabilities. The following table is a **general reference for the classic ESP32**, not a verified pinout of this custom PCB.

| GPIO | Potential functions | Considerations |
|---|---|---|
| GPIO0 | Digital I/O, PWM | Boot-strapping pin; may be connected to BOOT circuitry |
| GPIO2 | Digital I/O, ADC2, touch | Boot-strapping considerations |
| GPIO4 | Digital I/O, ADC2, touch, PWM | Multipurpose pin |
| GPIO5 | Digital I/O, SPI-related functions, PWM | Boot-strapping pin |
| GPIO12–15 | Digital I/O, ADC2, touch, SPI-related functions | Several pins have boot-strapping considerations |
| GPIO16–19 | Digital I/O, UART/SPI peripheral routing | Check actual board connections |
| GPIO21–23 | Digital I/O, commonly used for I²C/SPI | Functions are configurable |
| GPIO25–27 | Digital I/O, ADC2, PWM; DAC on GPIO25 and GPIO26 | Check peripheral and analog requirements |
| GPIO32–33 | Digital I/O, ADC1, touch, PWM | Useful for sensor and control applications |
| GPIO34–39 | Input-only GPIOs; ADC1 on supported pins | Cannot be used as digital outputs |

GPIO availability depends on module connections, board routing, peripheral assignments, and boot requirements. GPIOs used by the module's internal flash interface should not be treated as general-purpose expansion pins.

## Communication Protocols and Peripheral Capabilities

The classic ESP32 supports several wired and wireless interfaces. Actual availability on the custom board depends on the schematic, connected hardware, and firmware configuration.

| Interface | Purpose | Project relevance |
|---|---|---|
| UART | Serial communication and debugging | CP2102N programming and serial interface |
| I²C | Communication with sensors and peripheral ICs | Potential external peripheral interface |
| SPI | Communication with displays, sensors, and other peripherals | Potential external peripheral interface |
| PWM | LED dimming, motor control, and signal generation | Available through suitable GPIO assignments |
| ADC | Reading analog sensor signals | Supported analog-capable GPIOs |
| DAC | Analog voltage output | GPIO25 and GPIO26 on the classic ESP32 |
| Wi-Fi | Wireless networking | Integrated into the ESP32-WROOM-32E |
| Bluetooth | Wireless communication | Bluetooth Classic and BLE capabilities |
| CAN / TWAI | CAN-frame transmission and reception | Enhanced revision adds an SN65HVD230 CAN transceiver |

**Interface distinction:** UART, I²C, SPI, PWM, ADC, DAC, Wi-Fi, and Bluetooth are ESP32 capabilities, not necessarily dedicated board connectors or hardware-validated functions. The CAN interface requires appropriate ESP32 TWAI connections, transceiver wiring, and firmware configuration.

## Board-Specific Pin Mapping

The table below identifies important connections that should be documented from the final schematic. Exact GPIO numbers should be confirmed before publishing the pinout as definitive.

| Board signal | GPIO / pin | Connected component | Verification |
|---|---|---|---|
| USB-UART TX/RX | To be confirmed | CP2102N | Check schematic |
| BOOT | To be confirmed | BOOT button | Check schematic |
| RESET | EN pin / reset circuit | Reset button and circuitry | Check schematic |
| CAN TX | To be confirmed | SN65HVD230 | Check schematic |
| CAN RX | To be confirmed | SN65HVD230 | Check schematic |
| User LED | To be confirmed | LED circuit | Check schematic |
| GPIO expansion | To be confirmed per pin | GPIO header | Check schematic |

The final pin map should record each header pin, its ESP32 GPIO number, any connected onboard component, and relevant restrictions. Only confirmed connections should be documented as board-specific assignments.

## Tools & Technologies

| Category | Technologies |
|---|---|
| PCB design | KiCad 9 |
| Microcontroller | ESP32-WROOM-32E |
| USB-to-UART | CP2102N |
| Power regulation | AMS1117-3.3 V |
| Communication | UART, I²C, SPI, CAN/TWAI |
| Wireless | Wi-Fi, Bluetooth |
| Analog and control | ADC, DAC, PWM |
| Design verification | KiCad ERC and DRC |
| Visualization | KiCad 3D Viewer |
| Version control | Git and GitHub |

## Engineering Approach

The development process emphasizes incremental improvement and understanding the reasoning behind hardware design decisions.

- **Iterative development:** Progressively refining the board across multiple design revisions.
- **Design fundamentals:** Applying schematic design, component selection, footprint assignment, and PCB layout principles.
- **Multilayer design:** Exploring stackup configuration, copper layers, routing, and copper zones.
- **Peripheral integration:** Studying GPIO capabilities and communication interfaces.
- **Design verification:** Using ERC and DRC to identify potential issues during development.
- **Documentation and version control:** Maintaining design files and documenting progress through GitHub.
- **Continuous learning:** Using each revision to explore additional concepts and improve the overall design.

## Project Status

The repository documents the schematic and PCB design stages, including layout refinement and design-rule review.

**Physical fabrication, assembly, and hardware validation remain separate milestones** and will be documented when completed.

## Planned Work

- Finalize PCB layout and manufacturing checks.
- Verify the complete GPIO-to-header pin mapping.
- Fabricate and assemble the board.
- Verify power regulation and USB programming.
- Test GPIO functionality and peripheral interfaces.
- Develop embedded C firmware for peripheral control and communication.
- Validate CAN communication with compatible hardware.
- Document hardware testing, debugging, and subsequent design improvements.

## Project Objective

This project is part of my ongoing development in electronics and embedded systems engineering. It reflects a structured approach to learning: establish a working design foundation, explore more advanced hardware concepts, evaluate the results, and improve the design through successive revisions.

The goal is to develop practical engineering skills spanning **electronic circuit design, PCB development, GPIO and peripheral interfacing, hardware verification, and embedded systems integration**.

---

*KiCad 9 · ESP32 · PCB Design · Multilayer Hardware · GPIO · UART · I²C · SPI · CAN · Embedded Systems*
