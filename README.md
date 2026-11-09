# Portable Weather Data Logger

> **In development (2026 - present).** Two-board portable weather station: STM32, SX1262 868 MHz radio, CAN, USB-C and solar charging. Schematics for both boards are done and reviewed (0 validation errors); PCB layout and fabrication are next.

Two-board portable weather station designed in Altium Designer.

| Board | Role | MCU | Link |
|---|---|---|---|
| A | Control node: display (Olimex MOD-LCD2.8RTP), microSD logging, CAN | STM32F105R8T6 | SX1262 868 MHz radio + CAN |
| B | Sensor node: SHT40, BME280, VEML7700, SCD41, CCS811, SDP810, LSM6DSOX, SM351LT, 8 MB flash, fan | STM32G474RET6 | SX1262 868 MHz radio + CAN |

Both boards: USB-C + solar charging (MCP73831, BQ24210), BQ29700 battery protection, TPS63021 3.3 V buck-boost.

## Highlights

- Two separate, complete Altium Designer projects, one per board
- Offline-first design: data is collected in the field, stored on microSD and exported over USB, with no network required
- Long-range 868 MHz radio link (SX1262) between the boards, with a calculated matching network; RF tuning planned with a NanoVNA
- Battery-powered field units: USB-C and solar charging, battery protection, 3.3 V buck-boost rail
- Adaptive aspiration fan on the sensor node, switched on only when solar irradiance and wind make temperature readings unreliable
- Documented design process: DR1 calculations, block diagrams, schematic PDFs and a JLCPCB-ready BOM

## Documentation

- [Board A schematics (PDF)](docs/A%20board%20PDF.pdf)
- [Board B schematics (PDF)](docs/B%20board%20PDF.pdf)
- DR1 calculations: docs/DR1_Calculations_EN.pdf
- BOM: bom/ and dr2/ (JLCPCB BOM with LCSC part numbers)

## Project status

| Stage | Status | Date |
|---|---|---|
| Block diagrams (A, B) | ✅ Done | 2026-11-02 |
| Schematics - board A | ✅ Done (Validate: 0 errors) | 2026-11-09 |
| Schematics - board B | ✅ Done (Validate: 0 errors) | 2026-11-09 |
| Lecturer's DR1 remarks (2026-11-08) | ✅ All fixed | 2026-11-09 |
| DR1 calculations | ✅ Done (docs/DR1_Calculations_EN.pdf) | 2026-11-09 |
| Preliminary BOM (TME + JLCPCB/LCSC) | ✅ Done (bom/) | 2026-11-09 |
| DR1 - schematic review (week 8) | ⏳ Submitted, waiting for approval | |
| Component availability check (LCSC) | ⏳ In progress | |
| PCB layout - board A | ⬜ Not started | |
| PCB layout - board B | ⬜ Not started | |
| DR2 - manufacturing review (week 14): Gerber, CPL, final BOM, DFM | ⬜ Not started | |
| Fabrication + assembly (JLCPCB) | ⬜ Not started | |
| Bring-up, RF tuning (NanoVNA), firmware | ⬜ Not started | |

Legend: ✅ done · ⏳ in progress · ⬜ not started

## Open items

- [ ] Parts not found on LCSC (decide before PCB, footprints may change): CCS811B, BGS12WN6 RF switch, ABM81 32 MHz crystal, Molex 1054500101 USB-C, PESD1CAN-UX (SOT-323)
- [ ] Solar module: 5 V class, V<sub>oc</sub> ≤ 6.2 V (proposed WSL Solar 5V 1W)
- [ ] Measure B D3 (SMAJ5.0CA on VBAT) leakage at 4.2 V
- [ ] TBR values: display current, G474 current, Fox crystal ESR/C0

## Repository structure

```
A_board/   Altium project - control node
B_board/   Altium project - sensor node
docs/      DR1 calculations, block diagrams, schematic PDFs
bom/       BOM (TME) and JLCPCB BOM with LCSC part numbers
dr1/       Design Review 1 - schematics
dr2/       Design Review 2 - fabrication package
```

## License

Copyright (c) 2026 Rafdigo. All rights reserved. See [LICENSE](LICENSE).
