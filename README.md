# Industrial Sensor Module

## Overview
This industrial sensor module is designed for factory automation applications, providing real-time environmental monitoring of temperature, humidity, and air quality (VOC). The module is built to withstand harsh industrial conditions and supports multiple communication protocols, making it a versatile solution for various automation systems.

## Features
- **Power Input:** 9-24V DC
- **Voltage Regulation:**
  - 5V and 3.3V regulators (LDO and DC-DC buck converter)
- **Sensors:**
  - SHT31 (Temperature & Humidity, I2C)
  - CCS811 (VOC and CO2, I2C)
  - External Analog Input (0-5V, read through 12-bit ADC)
- **Communication Interfaces:**
  - RS485 (Modbus RTU support)
  - UART & I2C external pins
  - ESP32C3 Mini onboard
- **PCB Specifications:**
  - **Dimensions:** 50mm x 50mm
  - **Layer Count:** 4-layer PCB for improved signal integrity and EMI resistance
  - **Terminal Blocks:** Phoenix Contact (or equivalent) screw terminals for RS485 and power input
  - **ESD Protection:** TVS diodes on input lines to ensure robustness

## PCB Design
The PCB layout is optimized to minimize the influence of airflow on sensor measurements. The module is compact, modular, and suitable for various industrial applications.

## PCB Images
### Front View
The front side of the PCB features the ESP32C3 Mini, sensor modules, and necessary components for power regulation and communication. 
![Endüstriyel Sensör Modülü Front](https://github.com/user-attachments/assets/663ac6fb-dd59-4e93-8a2f-02c8cf6bd400)

### Back View
The back side of the PCB includes additional circuit traces, connectors, and protection components. 
![Endüstriyel Sensör Modülü Front Bottom](https://github.com/user-attachments/assets/d9f711ac-cdbb-4f4a-ac2b-e72f07fcd73b)

### Angled View
This perspective provides a detailed look at the board's overall design, component placement, and the layout strategy used to optimize performance and durability.
![Endüstriyel Sensör Modülü Front Cross](https://github.com/user-attachments/assets/f8cb3fd3-2845-4bbd-a1b5-fb6687180567)

## Getting Started
### Hardware Setup
1. Provide a **9-24V DC** power input via the terminal block.
2. Connect RS485 for Modbus RTU communication or use UART/I2C for direct interfacing.
3. Read sensor values via ESP32C3 Mini or any other microcontroller with supported interfaces.

### Firmware Development
- The ESP32C3 Mini can be programmed using **ESP-IDF** or **Arduino framework**.
- Libraries required:
  - `Wire.h` for I2C communication
  - `ModbusMaster.h` for Modbus RTU communication (if needed)
  - `Adafruit_SHT31.h` for SHT31 sensor
  - `Adafruit_CCS811.h` for CCS811 sensor

## Gerber Files & Manufacturing
- The **Gerber files** are available in the `gerber/` directory.
- Recommended PCB manufacturing specs:
  - **Layer Count:** 4
  - **Copper Thickness:** 1oz
  - **Surface Finish:** ENIG

## Contact
For any inquiries or contributions, feel free to open an issue or reach out.

---
_Designed with KiCad._ Designed by Yusuf Karabocek
