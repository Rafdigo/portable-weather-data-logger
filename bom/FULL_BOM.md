# Portable Data Logger — Pilnas BOM
## Paskutinis atnaujinimas: 2026-10-16

### MCU (×1 kiekvienai plokštei)
| Dalis | Aprašymas | Kaina | Tiekėjas |
|---|---|---|---|
| STM32G474RET6 (Board B) | Cortex-M4 170MHz LQFP64 | ~$8 | TME |
| STM32F105R8T6TR (Board A) | Cortex-M3 72MHz LQFP64 | ~$6 | TME |

### Jutikliai (Board B only, ×1 kiekvieno)
| Dalis | Funkcija | Kaina | Tiekėjas |
|---|---|---|---|
| SHT40-AD1B-R2 | Temp/drėgmė | ~$1.90 | TME |
| BME280 | Slėgis | ~$4.50 | TME |
| VEML7700-TR | Apšvietimas | ~$1.20 | TME |
| SGP41-D-R4 (arba CCS811B-JOPR5K) | VOC | ~$8.50 | TME |
| SCD41-D-R1 | CO₂ | ~$20.50 | DigiKey |
| LSM6DSOXTR | IMU | ~$3.50 | TME |
| SM351LT | Hall | ~$0.90 | TME |

### Ventiliatoriaus blokas (Board B only)
| Dalis | Aprašymas | Kaina | Tiekėjas |
|---|---|---|---|
| SUNON MF20100V1-1000U-A99 | BLDC ventiliatorius 20×20mm | ~$6.44 | TME |
| AO3400A | N-ch MOSFET SOT23 | ~$0.50 | TME |
| SS14 | Flyback diodas SMA 40V/1A | ~$0.30 | Mouser/DigiKey |
| TE 825433-2 | 2-pin header 2.54mm | ~$0.46 | TME |
| SMAJ5.0CA | TVS bidirectional | ~$0.30 | TME |
| Rezistoriai | 100Ω + 100kΩ (0603) | ~$0.02 | TME |
| Kondensatoriai | 10µF + 100nF×2 | ~$0.14 | TME |

### Maitinimo grandinė (×2, identiška abiem plokštėms)
| Dalis | Aprašymas | Kaina/vnt | Tiekėjas |
|---|---|---|---|
| 105450-0101 (Molex) | USB-C 24-pin SMT | ~$1.80 | TME/DigiKey |
| USBLC6-2SC6 | USB D± ESD SOT23-6 | ~$0.41 | TME |
| SMAJ5.0CA | VBUS TVS bidirectional | ~$0.30 | TME |
| MCP73831T-2DCI/OT | Li-Po charging SOT23-5 | ~$0.40 | TME |
| BQ24210DQCT | Solar charger WSON-10 | ~$1.68 | Mouser/DigiKey |
| B2B-PH-K-S(LF)(SN) ×2 | JST 2-pin (baterija+saulė) | ~$0.12 | TME |
| MIKROE-1120 | 3.7V 2000mAh Li-Po | ~$12.00 | TME |
| CL-SM3P | Saulės panelė 3W | ~$11.50 | TME |
| AO3401A | P-ch MOSFET SOT23 | ~$0.34 | TME |
| TPS63021DSJT | Buck-boost 3.3V VSON-14 | ~$2.90 | TME |
| MLP2016H2R2MT0S1 | 2.2µH induktorius | ~$0.30 | DigiKey |
| RK73H1ETTP5101F ×2 | 5.1kΩ CC pull-down | ~$0.02 | TME |
| Rezistoriai | 2kΩ(PROG), 100kΩ(Gate), 1kΩ(ISET), 1kΩ(VDPM), 10kΩ+4.3kΩ(TS) | ~$0.10 | TME |
| Kondensatoriai | 4.7µF(MCP VDD), 100nF×kelis | ~$0.10 | TME |

### Komunikacijos (per plokštę)
| Dalis | Aprašymas | Kaina | Tiekėjas |
|---|---|---|---|
| SN65HVD230DR | CAN transceiver SOIC8 | ~$2.27 | TME |
| 120Ω rezistorius | CAN terminavimas | ~$0.01 | TME |
| MTSW-103-08-G-S-229-RA | 3-pin UART debug header | ~$0.30 | TME |
| SX1262IMLTRT | RF transceiver QFN-24 | ~$4.33 | DigiKey/Mouser |
| 0900FM15K0039001E (Johanson) | RF matching IPD 0805 | ~$2-5 | Mouser |
| 32MHz kristalas | SX1262 reference clock | TBD | TBD |
| 47nH induktorius | SX1262 DCC_SW | TBD | TBD |

### SD kortelė (Board A only)
| Dalis | Aprašymas | Kaina | Tiekėjas |
|---|---|---|---|
| MEM2085-00-115-00-A (GCT) | microSD push-pull socket | ~$0.40 | TME |

### Ekranas (tik Board A)
| Dalis | Aprašymas | Kaina | Tiekėjas |
|---|---|---|---|
| Olimex MOD-LCD2.8RTP | 2.8" 240x320 ILI9341V, rezistyvinis jutiklis (I2C, NS2009/AR1021), UEXT 10 kont., kabelis rinkinyje | ~13 EUR | TME (likutį patikrinti) |
| TSW-105-22-G-D arba ZL202-10G | 2x5 header 2.54 mm THT (UEXT), 2 dalių simbolis J?A/J?B | ~0.13 EUR | TME |
| 10 uF 0603/0805 X5R >=10 V + 100 nF | 3.3 V filtras prie UEXT 1 | - | - |
| 2x 4.7 kOhm 0402 | I2C pull-up (DNP, jei modulyje yra) | - | - |

### I2C pull-ups (Board B)
| Dalis | Vertė | Kiekis |
|---|---|---|
| 2.2kΩ 0603 | I2C1 SCL/SDA + I2C2 SCL/SDA | 4 vnt. |

---
**BENDRA SUMA: ~$154.49** (abi plokštės, be PCB gamybos)

### Papildymai 2026-10-27 (abi plokstes, jei nenurodyta kitaip)
| Dalis | Aprasymas | Kaina | Tiekejas |
|---|---|---|---|
| BQ29700DSER | 1S Li-ion apsauga (x2) | ~$1.19 (kaina nepatikrinta) | Mouser |
| AO3400A | apsaugos FET (x4: 2 per plokste) | ~0.1 | TME/Mouser |
| TPS61023DRLR | 5 V boost (B plokste) | ~1-2 | Mouser |
| 1 uH induktorius (Wurth 74438357010 / Coilcraft XEL4030-102ME) | boost L | ~1 | Mouser |
| SDP810-125PA (Sensirion) | vejo greicio jutiklis (B) + Pito vamzdelis | ~21 EUR | TME (1-101597-01) | (schema padaryta; reflow netinka)
| PESD1CAN-UX | CAN TVS (A plokste nauja) | ~0.3 | TME |
| Header 3 (2.54) | CAN jungtis (x2) | ~0.1 | TME |
| USBLC6-2SC6 | ESD UART + SWD (x2 per plokste) | ~0.3 | TME |
