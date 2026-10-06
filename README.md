# ESP32 Development Board — 4-Layer PCB

A custom ESP32 development board designed in KiCad 9, built around the **ESP32-WROOM-32E** module.

The board combines USB programming, regulated power, wireless connectivity, CAN communication, and common embedded interfaces into a compact development platform.

---

## Overview

The ESP32 Development Board is designed as a general-purpose embedded development platform.

The board provides:

- ESP32-WROOM-32E microcontroller module
- Integrated Wi-Fi and Bluetooth
- USB-C interface
- CP2102N USB-to-UART bridge
- AMS1117-3.3 voltage regulator
- I²C interface
- SPI interface
- UART interfaces
- CAN interface
- OLED interface
- Boot and Reset push buttons
- User LED
- 30-pin GPIO expansion header
- Four-layer PCB stackup
- Ground plane on the inner layer
- CAN protection and selectable termination

---

## Hardware Architecture

The main system is centered around the **ESP32-WROOM-32E**.

### Main Blocks

```text
                    ┌──────────────────────┐
                    │      USB-C INPUT     │
                    └──────────┬───────────┘
                               │
                    ┌──────────▼───────────┐
                    │      CP2102N         │
                    │    USB-to-UART       │
                    └──────────┬───────────┘
                               │ UART
                               │
                    ┌──────────▼───────────┐
                    │    ESP32-WROOM-32E   │
                    │                      │
                    │ Wi-Fi + Bluetooth    │
                    │ GPIO / UART / SPI    │
                    │ I²C / CAN           │
                    └───────┬─────┬────────┘
                            │     │
               ┌────────────┘     └─────────────┐
               │                                │
        ┌──────▼──────┐                  ┌──────▼──────┐
        │   OLED/I²C  │                  │    CAN      │
        │             │                  │ SN65HVD230  │
        └─────────────┘                  └──────┬──────┘
                                               │
                                         CANH / CANL

                    ┌──────────────────────┐
                    │    AMS1117-3.3      │
                    │    Power Supply     │
                    └──────────────────────┘
