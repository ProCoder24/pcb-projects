# ESP32-S3 USB-C Development Board

## Overview

Custom ESP32-S3-MINI development board designed for dual USB-C connectivity, flexible programming interfaces, and high-performance wireless applications.

This board supports both traditional UART-based programming and native USB operation, enabling advanced use cases such as JTAG debugging, USB HID devices, and OTG applications.

---

## Technical Specifications

### 1. Core Processing & Wireless

* **Module:** Espressif ESP32-S3-MINI-1
* **Processor:** Xtensa® Dual-Core 32-bit LX7 MCU (up to 240 MHz)
* **Memory:**

  * 384 KB ROM
  * 512 KB SRAM
  * 16 KB RTC SRAM
* **Wireless:**

  * 2.4 GHz Wi-Fi (802.11 b/g/n)
  * Bluetooth® 5 (LE) with Long Range support

---

### 2. Connectivity & Interfaces

#### Dual USB-C Architecture

* **USB-C Port 1 (UART):**
  FTDI FT232RQ bridge for standard serial programming and debugging

* **USB-C Port 2 (Native USB):**
  Direct connection to ESP32-S3 (GPIO19/20) for:

  * USB JTAG debugging
  * USB OTG applications
  * USB HID device development

#### Expansion Headers

* 2 × 24-pin headers (0.1" pitch)
* Total: **48 breakout pins**, including:

  * 3.3V / 5V
  * GND
  * GPIOs

---

### 3. Power System

* **Input Voltage:**

  * 5V via USB-C
  * External 5V input pin

* **Regulator:** TLV1117-33IDCY LDO (5V → 3.3V)

* **Power Selection:**
  3-pin jumper to select active USB power source

---

### 4. On-board Peripherals

#### Buttons

* **Reset Button:** Connected to EN (CHIP_PU)
* **Boot/User Button:** Connected to GPIO0

#### Indicators

* **Power LED (Green):** Indicates active 3.3V rail
* **User LED (Red):** Connected to GPIO2

---

### 5. Hardware Engineering Features

* **Auto-Reset Circuit:**
  Dual BSS138 MOSFET-based circuit enabling automatic entry into download mode

* **ESD Protection:**
  Dedicated ESD suppressors on USB D+ / D− lines

* **PCB Stackup:**
  4-layer design:
  Signal – Ground – Power – Signal

  Optimized for:

  * RF performance
  * Power integrity
  * Thermal dissipation

---

## Project Structure

```
ESP32_USBC/
├── Hardware/        # Altium schematic and PCB files
├── Libraries/       # Custom components and footprints
├── Docs/            # Images and documentation
├── Manufacturing/   # Gerbers and fabrication files (future)
```

---

## Status

🚧 Work in progress (initial frozen revision)

---

## Design Highlights

* Dual USB architecture (UART + Native USB)
* Flexible power source selection
* 4-layer PCB stackup
* Integrated auto-reset for seamless programming

---

## Next Revision (Planned Improvements)

* Improve USB signal integrity (impedance control)
* Add additional ESD/TVS validation
* Optimize decoupling and PDN
* Validate high-speed USB routing constraints

---

## Tools Used

* Altium Designer
* LTspice
* openEMS

---

## Author

Jean Ombeni
Electrical Engineering