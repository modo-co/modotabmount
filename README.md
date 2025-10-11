# Modo Tab Mount – Smart Tablet Wall Mount

**Open-source smart tablet mount with ESPHome integration, magnetic docking, and customizable sensors.**  

<video width="640" height="360" controls>
  <source src="https://raw.githubusercontent.com/modo-co/modotabmount/main/images/main_anim_all_visible.mp4.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

## Overview

Modo Tab Mount is a modular wall mount for tablets, designed for **EU flush electrical back boxes**. It combines sleek design with smart electronics:

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
| Tablet Plate         | 3 mm thick solid iron plate, attached using 3M VHB tape                     |
| Mounting Plate       | 3D-printed (PETG + CF fillament) with embedded neodymium magnets/iron ring    |
| Power Supply         | MEAN WELL IRM-10-5 (5V, 2A)                                                |
| PCB                  | Custom PCB for power supply and peripheral connections               |
| Microcontroller      | Seeed Studio XIAO ESP32-C3 with USB-C and exposed GPIOs                    |
| LEDs                 | 2.7 mm WS2812B addressable LED strip (optional)                             |
| Flat Charging Cable  | Flat FPC cable with Type-C, Lightning, or Micro USB connector               |


## Repository Content

This repository contains the files and resources needed for the Modo Tab Mount project:

| Folder / File           | Description                                                                 |
|-------------------------|-----------------------------------------------------------------------------|
| `3D_Models/`            | 3D-printable files for the mounting plate and other components (STL/STEP)   |
| `PCB/`                  | Schematics and Gerber files for the custom power supply and controller PCB  |
| `modotabmount.yaml`     | ESPHome configuration file                                                  |
| `Docs/`                 | Installation instructions, datasheets, and technical documentation          |
| `Images/`               | Photos, diagrams, and reference images for assembly                         |
| `README.md`             | Project overview and instructions                                           |
| `LICENSE`               | Project license information                                                 |

## License

### Hardware (3D Models, Schematics, PCB Layouts)
All hardware designs in this repository are licensed under the **Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)** license.  
You are free to share and adapt these materials **for personal or educational use**, but **commercial use is not allowed** (e.g., manufacturing or selling).

Full license text: [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/)

### Firmware / Software
All firmware and software in this repository is licensed under the **MIT License**, allowing you to freely use, modify, and distribute the code, including for commercial purposes.

See the [LICENSE](./LICENSE) file for full details.

---
