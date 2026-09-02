# ESP32 Development Board – Custom PCB Design

A custom ESP32 development board designed from schematic to PCB using **KiCad**.

The board is built around the **ESP32-WROOM-32E** and integrates USB connectivity, power management, CAN communication, OLED/I²C, UART, SPI, boot/reset controls, and a consolidated GPIO expansion header.

---

## 📌 Project Overview

This project demonstrates the complete PCB design workflow:

- Circuit and schematic design
- Component selection and footprint assignment
- PCB component placement
- Two-layer PCB routing
- USB-to-UART interface design
- Power regulation
- CAN communication interface
- GPIO expansion
- PCB design verification
- 3D visualization and documentation

The main objective of the project is to create a versatile ESP32 development platform suitable for embedded-system development, communication experiments, and hardware prototyping.

---

## ✨ Key Features

- **ESP32-WROOM-32E** microcontroller module
- **USB-C** interface
- **CP2102N** USB-to-UART bridge
- **AMS1117-3.3** voltage regulator
- **CAN bus** interface using SN65HVD230
- CAN transient protection using **NUP2105L**
- **120 Ω CAN termination** with selectable jumper
- **OLED / I²C interface**
- **UART2 interface**
- **SPI interface**
- Boot and reset controls
- User status LED
- Local power-supply decoupling
- Consolidated **30-pin GPIO expansion header**
- Two-layer PCB design
- KiCad schematic, PCB and project files included

---

## 🧩 System Architecture

```text
                         ┌─────────────────────┐
                         │     USB-C Port      │
                         └──────────┬──────────┘
                                    │
                                    ▼
                         ┌─────────────────────┐
                         │      CP2102N        │
                         │   USB ↔ UART Bridge │
                         └──────────┬──────────┘
                                    │ UART0
                                    ▼
┌─────────────────────────────────────────────────────────┐
│                  ESP32-WROOM-32E                        │
│                                                         │
│  I²C ─────────────── OLED                               │
│  SPI ──────────────── Expansion / Peripherals           │
│  UART2 ────────────── Expansion / Peripherals           │
│  CAN ──────────────── SN65HVD230                        │
│  GPIO ─────────────── 30-Pin Expansion Header           │
│  GPIO2 ────────────── User LED                          │
│  EN ───────────────── Reset Circuit                     │
└─────────────────────────────────────────────────────────┘
                                    │
                                    ▼
                         ┌─────────────────────┐
                         │   Power Regulation  │
                         │    AMS1117-3.3      │
                         └─────────────────────┘
