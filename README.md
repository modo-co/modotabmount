# Modo Tab Mount – Smart Tablet Wall Mount

**Open-source smart tablet mount with ESPHome firmware, magnetic docking, and customizable sensors.**  

![Modo Tab Mount demo](https://raw.githubusercontent.com/modo-co/modotabmount/main/images/modotabmount_animat.gif)

## Overview

Modo Tab Mount is a modular wall mount for tablets, designed for **standard EU flush electrical back boxes**. It combines sleek design with smart electronics:

- Magnetic docking for easy attach/detach  
- Floating tablet design (minimal wall gap)  
- Integrated 5V smart power supply  
- ESP32-based microcontroller with ESPHome firmware  
- Optional sensors for automation and monitoring  
- Fully compatible with Home Assistant  

This project is aimed at **makers, home automation enthusiasts, and developers** who want a customizable smart wall mount.

## Features

- **Magnetic Docking:** Secure snap-on mounting without mechanical locks.  
- **Floating Design:** Elegant, minimal gap between tablet and wall.  
- **Smart Power Supply:** 5V output for tablet and peripherals.  
- **Backlit LEDs:** Optional WS2812B individually addressable LED strip bracket for status indications or night light.  
- **ESPHome Firmware:** Open-source, customizable for sensors, LEDs, and automations.  
- **Home Assistant Ready:** Integrates with Home Assistant for tablet charging automation, power monitoring, and reading connected sensors.  
- **Expandable:** Add custom peripherals like air quality or occupancy sensors.

## Hardware Components

| Component            | Description                                                                 |
|----------------------|-----------------------------------------------------------------------------|
| Wall Box Mount       | 3D-printed (PETG + CF fillament) with embedded neodymium magnets/iron ring  |
| Tablet Plate         | 3 mm thick solid iron plate, attached using 3M VHB tape                     |
| Power Supply         | MEAN WELL IRM-10-5 (5V, 2A)                                                |
| PCB                  | Custom PCB for power supply and peripheral connections               |
| Microcontroller      | Seeed Studio XIAO ESP32-C3 with USB-C and exposed GPIOs                    |
| LEDs                 | 2.7 mm WS2812B addressable LED strip                            |
| Charging Cable       | Flat FPC cable with Type-C, Lightning, or Micro USB connector               |


## Repository Content

This repository contains the files and resources needed for the Modo Tab Mount project:

| Folder / File           | Description                                                                 |
|-------------------------|-----------------------------------------------------------------------------|
| `PCB/`                  | Schematics and Gerber files for the custom power supply and controller PCB  |
| `Docs/`                 | Installation instructions, datasheets, and technical documentation          |
| `Images/`               | Photos, diagrams                                                            |
| `modotabmount.yaml`     | ESPHome configuration file                                                  |
| `README.md`             | Project overview                                                            |
| `LICENSE`               | Project license information                                                 |


## 📦 Firmware

The **Modo Tab Mount** firmware runs on an **ESP32-C3** and is built using **ESPHome**.  
It provides safe tablet charging, power monitoring, LED feedback, and seamless **Home Assistant integration**.

### Distribution model

- Firmware is provided as a **precompiled binary (`.bin`)** via **GitHub Releases**
- End users **do not need to install ESPHome or compile anything**
- The ESPHome YAML configuration is included **for reference and advanced customization only**

### 🔌 Smart Charging Control

- PWM-regulated 5V output for controlled tablet charging
- Charging can be enabled or disabled remotely
- Configurable **charging limit (%)** to reduce battery wear
- **Thermal protection** with automatic throttling based on device temperature
- Cool-down logic prevents overheating during long charging sessions

Charging state is exposed as a readable status  
(e.g. *Normal*, *Thermal throttling*, *Cooling down*).

### ⚡ Power & Energy Monitoring

An onboard **INA219** sensor measures:

- Output voltage
- Output current
- Instantaneous power
- 30-second averaged values for stable reporting

All values are available in **Home Assistant** and via the **built-in web interface**, enabling automations based on real power usage.

### 💡 LED Feedback & Ambient Lighting

The integrated **WS2812 LED ring** provides both functional feedback and ambient lighting:

- Automatic LED indication during **Wi-Fi access-point setup mode**
- Full RGB control with multiple built-in effects
- Automatic LED dimming while charging to reduce visual distraction
- All LED behavior can be controlled via Home Assistant or the local web UI

### 🌐 Connectivity & Interfaces

- Native **Home Assistant API** (ESPHome)
- Built-in **web interface** for local control and diagnostics
- **OTA firmware updates** supported
- **Bluetooth Proxy** enabled to extend Home Assistant BLE coverage

### ⚙️ Configuration & Diagnostics

User-configurable parameters include:

- Charging limit
- Maximum temperature
- Throttle strength
- LED brightness during charging

Built-in diagnostics expose:

- Wi-Fi signal strength
- Device uptime
- Internal temperature
- Memory usage

A software-triggered factory reset is also available.

### 🔧 Advanced Usage

Advanced users may modify the ESPHome YAML configuration and build custom firmware versions.  
Custom firmware modifications are performed **at the user’s own risk**.


## 🔒 Safety Notice

⚠️ This project involves **mains voltage (230V AC)**.  
Installation should only be performed by qualified persons.  
If unsure, consult a licensed electrician.

## License

### Hardware (3D Models, Schematics, PCB Layouts)
All hardware designs in this repository are licensed under the **Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)** license.  
You are free to share and adapt these materials **for personal or educational use**, but **commercial use is not allowed** (e.g., manufacturing or selling).

Full license text: [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/)

### Firmware / Software
All firmware and software in this repository is licensed under the **MIT License**, allowing you to freely use, modify, and distribute the code, including for commercial purposes.

See the [LICENSE](./LICENSE) file for full details.

---
