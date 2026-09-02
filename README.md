# ESP32 Development Board PCB

A custom 2-layer ESP32 development board designed in **KiCad 9**, integrating USB connectivity, GPIO expansion, CAN communication, OLED support, and commonly used embedded interfaces into a single development platform.

---

## Overview

This project covers the complete PCB design workflow, from schematic capture and component selection through PCB placement, routing, and design-rule verification.

The board is centered around the **ESP32-WROOM-32E** and is designed as a versatile development platform for embedded systems, communication interfaces, and peripheral experimentation.

The design was developed as a **portfolio and learning project**. The PCB has not been physically manufactured or hardware-tested.

---

## Key Features

- **ESP32-WROOM-32E** wireless microcontroller module
- **USB-C** connector for power and USB communication
- **CP2102N** USB-to-UART bridge
- **AMS1117-3.3** voltage regulator
- **30-pin GPIO expansion header**
- **OLED interface**
- **CAN bus interface**
- **SN65HVD230** CAN transceiver
- **NUP2105L** CAN bus protection
- **Selectable 120 Ω CAN termination**
- UART interface
- SPI interface
- I²C interface
- Boot and Reset push buttons
- User status LED
- Local power decoupling
- 2-layer PCB design

---

## System Architecture

The board is organized around several functional blocks:

### Microcontroller

The **ESP32-WROOM-32E** provides the main processing capability along with integrated Wi-Fi and Bluetooth connectivity.

### USB / Programming

A USB-C interface is connected to a **CP2102N USB-to-UART bridge**, providing a convenient connection between the development board and a host computer.

The USB interface supports board power and serial communication/programming.

### Power

The USB-C input supplies the board, with an **AMS1117-3.3** regulator generating the 3.3 V rail required by the ESP32 and supporting circuitry.

Decoupling capacitors are placed around the relevant power circuits to support stable local supply operation.

### CAN Communication

The CAN interface is implemented using the **SN65HVD230** transceiver.

The CAN bus includes **NUP2105L** protection, while a selectable **120 Ω termination resistor** is provided through the onboard termination jumper.

### GPIO Expansion

A single **30-pin expansion header** provides access to the available ESP32 GPIOs along with:

- 3.3 V
- 5 V
- GND

This allows external sensors, displays, communication modules, and other peripherals to be connected without requiring dedicated headers for every interface.

---

## Supported Interfaces

| Interface | Implementation |
|---|---|
| USB | USB-C + CP2102N |
| UART | ESP32 UART interface |
| I²C | ESP32 GPIO21 / GPIO22 |
| SPI | ESP32 GPIO18 / GPIO19 / GPIO23 |
| CAN | SN65HVD230 |
| GPIO | 30-pin expansion header |
| OLED | Dedicated connector |
| Power | USB-C + AMS1117-3.3 |

---

## GPIO Expansion

The board uses a universal GPIO expansion header rather than separate headers for each communication protocol.

The header exposes the following ESP32 GPIOs:

```text
GPIO0
GPIO1
GPIO2
GPIO3
GPIO4
GPIO5
GPIO12
GPIO13
GPIO14
GPIO15
GPIO16
GPIO17
GPIO18
GPIO19
GPIO21
GPIO22
GPIO23
GPIO25
GPIO26
GPIO27
GPIO32
GPIO33
GPIO34
GPIO35
GPIO36
GPIO39
