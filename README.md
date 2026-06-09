# CryingPlants

A solar-powered Thread plant monitor with soil moisture sensing, battery monitoring and Home Assistant integration, built with ESPHome and ESP32-C6.

## Overview

CryingPlants is an open-source plant monitoring system designed for indoor and outdoor plants.

The device measures soil moisture using capacitive sensors, reports battery status, and communicates over Thread directly to Home Assistant. Powered by a LiPo battery and optional solar panel, CryingPlants is designed for long-term autonomous operation with ultra-low power consumption.

The project combines:

* ESPHome
* ESP32-C6
* Thread networking
* Home Assistant
* Deep Sleep power saving
* Solar charging
* Open-source hardware

## Features

* Up to 4 capacitive soil moisture sensors
* Thread connectivity (no Wi-Fi required)
* Native Home Assistant integration
* Battery voltage monitoring
* Battery level estimation
* Deep Sleep support for long battery life
* OTA firmware updates
* Solar-powered operation
* Open-source hardware and firmware

## Hardware

Current reference hardware:

* DFRobot FireBeetle 2 ESP32-C6
* 3.7V LiPo battery
* Capacitive soil moisture sensors
* Solar panel
* NDP6020P P-channel MOSFET

## Software

Firmware is based on ESPHome.

Required components:

* Home Assistant
* Thread Border Router
* ESPHome

Tested with:

* Apple TV 4K as Thread Border Router
* Home Assistant running on Raspberry Pi
* ESPHome 2026.x

## Repository Structure

```text
docs/           Documentation and images
firmware/       ESPHome firmware
hardware/       PCB, schematics and BOM
fritzing/       Fritzing source files
enclosure/      3D printable enclosure files
examples/       Example configurations
```

## Building the Hardware

Detailed assembly instructions can be found in:

```text
docs/build-guide/
```

PCB files and Gerber files are located in:

```text
hardware/pcb/
hardware/gerber/
```

## Flashing the Firmware

Example ESPHome workflow:

```bash
esphome run cryingplants.yaml
```

OTA updates are supported via Thread.

## Home Assistant Integration

Once flashed and commissioned, CryingPlants automatically exposes:

* Soil moisture sensors
* Battery voltage
* Battery level
* Device diagnostics

to Home Assistant.

## Power Consumption

CryingPlants is optimized for battery-powered operation using Deep Sleep.

Typical workflow:

1. Wake up
2. Power sensors
3. Measure values
4. Send data via Thread
5. Return to Deep Sleep

This minimizes energy consumption and enables long runtimes on battery power.

## Roadmap

* [x] Thread communication
* [x] Home Assistant integration
* [x] Battery monitoring
* [x] Deep Sleep
* [x] PCB Version 1.3
* [ ] Solar charging optimization
* [ ] Enclosure design
* [ ] Multi-device deployment guide
* [ ] Automatic calibration

## License

This project is licensed under the Apache License 2.0.
See the LICENSE file for details.

## Contributing

Contributions, bug reports and hardware improvements are welcome.

## Disclaimer

This project is provided as-is without warranty. Use at your own risk.
