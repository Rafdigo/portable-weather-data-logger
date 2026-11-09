# Portable Weather Data Logger

An autonomous, offline-first outdoor weather station built from two custom STM32 boards that talk to each other over a long-range 868 MHz radio link. Everything works without any network infrastructure: data is collected in the field, stored locally and exported over USB.

> Status: work in progress. Schematics are being finished; PCB layout and fabrication come next.

## Idea

Low-cost weather stations that use a passive radiation shield can read 2-5 C too high in strong sun and low wind. Professional stations fix this with an always-on fan, which costs power. This project uses a small **adaptive aspiration fan** that only switches on when solar irradiance and wind speed indicate a high risk of measurement error, so accuracy improves without draining the battery.

## System overview

| | Board A - Control Node | Board B - Sensor Node |
|---|---|---|
| MCU | STM32F105R8T6TR | STM32G474RET6 |
| Role | Receives data, stores it, shows status, exports to PC | Field unit: reads sensors, drives the fan, transmits data |
| Storage / UI | SD card (SPI, FAT32), touchscreen LCD | - |
| Interfaces | USB, CAN, SWD, SX1262 radio | USB, CAN, SWD, SX1262 radio |
| Power | Li-ion battery, USB-C and solar charging, buck-boost regulator | Same power chain |

The boards are linked by **SX1262 (868 MHz)** radios with a calculated matching network and an antenna keep-out zone. Both boards are battery powered and designed for field deployment.

## Board B sensors (all I2C)

- SHT40 - temperature and humidity (primary)
- BME280 - barometric pressure, secondary temperature/humidity cross-check
- VEML7700 - ambient light
- CCS811B - VOC / air quality
- SCD41 - CO2
- LSM6DSOX - accelerometer and gyroscope
- SM351LT - Hall effect sensor (fan RPM / position)

## Repository structure

| Folder | Contents |
|---|---|
| `A_board/` | Altium Designer project for Board A (control node) |
| `B_board/` | Altium Designer project for Board B (sensor node) |
| `docs/` | Design notes, schematic PDFs and supporting documents |
| `bom/` | Bill of materials and supplier notes |
| `dr1/` | Design Review 1 - schematics |
| `dr2/` | Design Review 2 - fabrication package |

Each board is a separate Altium project. Open the `.PrjPcb` file in the matching folder.

## Roadmap

- [x] Block diagram, component selection and power chains
- [x] MCU, power, USB, I2C, CAN, UART and SD card schematics
- [ ] Radio (SX1262) section and matching network
- [ ] DR1: schematic review
- [ ] PCB layout
- [ ] DR2: fabrication package, PCB order and assembly
- [ ] Firmware and field testing

## Tools

Altium Designer, STM32 toolchain, JLCPCB / LCSC for fabrication and assembly.
