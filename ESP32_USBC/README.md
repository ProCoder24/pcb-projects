\# ESP32-S3 USB-C Development Board



\## Overview



Custom ESP32-S3-MINI development board designed for dual USB-C connectivity, flexible programming interfaces, and high-performance wireless applications.



This board supports both traditional UART-based programming and native USB operation, enabling advanced use cases such as JTAG debugging, USB HID devices, and OTG applications.



\---



\## Technical Specifications



\### 1. Core Processing \& Wireless



\* \*\*Module:\*\* Espressif ESP32-S3-MINI-1

\* \*\*Processor:\*\* Xtensa® Dual-Core 32-bit LX7 MCU (up to 240 MHz)

\* \*\*Memory:\*\*



&#x20; \* 384 KB ROM

&#x20; \* 512 KB SRAM

&#x20; \* 16 KB RTC SRAM

\* \*\*Wireless:\*\*



&#x20; \* 2.4 GHz Wi-Fi (802.11 b/g/n)

&#x20; \* Bluetooth® 5 (LE) with Long Range support



\---



\### 2. Connectivity \& Interfaces



\#### Dual USB-C Architecture



\* \*\*USB-C Port 1 (UART):\*\*

&#x20; FTDI FT232RQ bridge for standard serial programming and debugging



\* \*\*USB-C Port 2 (Native USB):\*\*

&#x20; Direct connection to ESP32-S3 (GPIO19/20) for:



&#x20; \* USB JTAG debugging

&#x20; \* USB OTG applications

&#x20; \* USB HID device development



\#### Expansion Headers



\* 2 × 24-pin headers (0.1" pitch)

\* Total: \*\*48 breakout pins\*\*, including:



&#x20; \* 3.3V / 5V

&#x20; \* GND

&#x20; \* GPIOs



\---



\### 3. Power System



\* \*\*Input Voltage:\*\*



&#x20; \* 5V via USB-C

&#x20; \* External 5V input pin



\* \*\*Regulator:\*\*

&#x20; TLV1117-33IDCY LDO (5V → 3.3V)



\* \*\*Power Selection:\*\*

&#x20; 3-pin jumper to select active USB power source



\---



\### 4. On-board Peripherals



\#### Buttons



\* \*\*Reset Button:\*\* Connected to EN (CHIP\_PU)

\* \*\*Boot/User Button:\*\* Connected to GPIO0



\#### Indicators



\* \*\*Power LED (Green):\*\* Indicates active 3.3V rail

\* \*\*User LED (Red):\*\* Connected to GPIO2



\---



\### 5. Hardware Engineering Features



\* \*\*Auto-Reset Circuit:\*\*

&#x20; Dual BSS138 MOSFET-based circuit enabling automatic entry into download mode



\* \*\*ESD Protection:\*\*

&#x20; Dedicated ESD suppressors on USB D+ / D− lines



\* \*\*PCB Stackup:\*\*

&#x20; 4-layer design:

&#x20; Signal – Ground – Power – Signal



&#x20; Optimized for:



&#x20; \* RF performance

&#x20; \* Power integrity

&#x20; \* Thermal dissipation



\---



\## Project Structure



```

ESP32\_USBC/

├── Hardware/        # Altium schematic and PCB files

├── Libraries/       # Custom components and footprints

├── Docs/            # Images and documentation

├── Manufacturing/   # Gerbers and fabrication files (future)

```



\---



\## Status



🚧 Work in progress (initial frozen revision)



\---



\## Design Highlights



\* Dual USB architecture (UART + Native USB)

\* Flexible power source selection

\* Clean 4-layer PCB stackup

\* Integrated auto-reset for seamless programming



\---



\## Next Revision (Planned Improvements)



\* (Planned) LTspice for power analysis

\* (Planned) openEMS for EM validation



\---



\## Tools Used



\* Altium Designer

\* LTspice
\* OpenEMS

\---



\## Author



Jean Ombeni

Electrical Engineering

