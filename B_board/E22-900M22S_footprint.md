# E22-900M22S — footprint duomenys (iš Ebyte STEP modelio)
Atnaujinta: 2026-10-19

STEP failas yra tik 3D modelis – jo negalima "dėti" į schemą ar PCB kaip komponento.
Jį naudok kaip 3D kūną footprint'e (PcbLib: Place -> 3D Body -> Generic STEP Model).

## Iš STEP modelio nuskaityta
- Korpusas: 14.0 mm (X) x 20.0 mm (Y), aukštis iki ~3.1 mm (su ekranu); centras = (0, 0)
- 22 pad'ai (pusapvalės "stamp" skylės), po 11 kiekvienoje ilgojoje pusėje (x = -7 ir x = +7)
- Pad'o plotis 0.8 mm, žingsnis 1.27 mm, varis nuo korpuso krašto 0.9 mm gilyn
- Kiekvienoje pusėje: 8 pad'ai pastoviu žingsniu + 3 pad'ų grupė viršuje (tarpas ~5.6 mm tarp jų)

## Pad'ų centrai (vaizdas iš viršaus, pin 1 viršuje kairėje) — REIKIA PATIKRINTI
| Pin | Pavadinimas | X (mm) | Y (mm) |
|---|---|---|---|
| 1 | GND | -7.0 | +9.00 |
| 2 | GND | -7.0 | +7.73 |
| 3 | GND | -7.0 | +6.46 |
| 4 | GND | -7.0 | +0.89 |
| 5 | GND | -7.0 | -0.38 |
| 6 | RXEN | -7.0 | -1.65 |
| 7 | TXEN | -7.0 | -2.92 |
| 8 | DIO2 | -7.0 | -4.19 |
| 9 | VCC | -7.0 | -5.46 |
| 10 | GND | -7.0 | -6.73 |
| 11 | GND | -7.0 | -8.00 |
| 12 | GND | +7.0 | -8.00 |
| 13 | DIO1 | +7.0 | -6.73 |
| 14 | BUSY | +7.0 | -5.46 |
| 15 | NRST | +7.0 | -4.19 |
| 16 | MISO | +7.0 | -2.92 |
| 17 | MOSI | +7.0 | -1.65 |
| 18 | SCK | +7.0 | -0.38 |
| 19 | NSS | +7.0 | +0.89 |
| 20 | GND | +7.0 | +6.46 |
| 21 | ANT | +7.0 | +7.73 |
| 22 | GND | +7.0 | +9.00 |

## Ką dar patikrinti prieš gaminant PCB
1. Pin numeravimas ir pin 1 kampas pagal Ebyte manual brėžinį (STEP rodo tik geometriją, ne numerius; numeraciją išvedžiau pagal U formos tvarką ir pin pavadinimus).
2. Ar vaizdas ne veidrodinis (X/Y ženklai).
3. PCB pad'o dydis: siūlau 0.8 mm plotis ir ~2.0 mm ilgis, išsikišantis ~1.1 mm už modulio krašto (litavimui) – tai mano pasiūlymas, ne gamintojo.
