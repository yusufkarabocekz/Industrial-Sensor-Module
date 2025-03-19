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

## License
This project is released under the **MIT License**.

## Contact
For any inquiries or contributions, feel free to open an issue or reach out.

---
_Designed with KiCad._

