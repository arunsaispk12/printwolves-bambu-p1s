# NuMakers Filament Cheatsheet — BambuLab P1S

*[Print Wolves](https://www.printwolves.com) · BambuLab P1S Reference*

> **Printer:** BambuLab P1S · **Nozzles in use:** 0.2 mm | 0.4 mm | 0.6 mm
> **Nozzle material:** Standard brass (PLA/PETG non-CF) | Hardened steel (CF variants, long ABS/ASA runs)
> **Slicer:** Bambu Studio (primary) / OrcaSlicer (secondary) · **Filament diameter:** 1.75 mm

---

## Nozzle Selection Guide

| Nozzle | Best For | Max Speed | Notes |
|--------|----------|-----------|-------|
| **0.2 mm** | Fine detail, miniatures, small parts | 50–80 mm/s | Much slower print times; great surface detail; clog risk higher with filled filaments — avoid CF/Wood/Glow |
| **0.4 mm** | General purpose (default) | 150–300 mm/s | Best all-rounder; calibration values in this sheet are for 0.4 mm |
| **0.6 mm** | Large functional parts, fast prints, high infill | 150–250 mm/s | Coarser finish; better layer adhesion; use for ABS/ASA structural parts |

### Nozzle Size — Settings Adjustments

| Setting | 0.2 mm vs 0.4 mm | 0.6 mm vs 0.4 mm |
|---------|-----------------|-----------------|
| Max volumetric speed | Reduce by ~50% | Increase by ~30–50% |
| Max layer height | 0.15 mm | 0.45 mm |
| Pressure advance (K) | Slightly lower (−10–15%) | Slightly higher (+10–15%) |
| Flow ratio | Recalibrate — do not assume same value | Recalibrate |
| Print speed | Reduce outer wall to 30–40 mm/s | Can increase infill to 300+ mm/s |

> Always re-run flow rate and flow dynamics calibration when swapping nozzle sizes. K-values from a 0.4 mm nozzle do **not** transfer to 0.2 mm or 0.6 mm.

---

## Quick Reference — All 16 Filaments

### Functional PLA

| Filament | Nozzle Temp | Bed Temp (Textured PEI) | Flow Ratio | Max Vol Speed | Fan Speed | AUX Fan | Enclosure | Nozzle | Drying |
|----------|-------------|------------------------|------------|--------------|-----------|---------|-----------|--------|--------|
| **PLA** | 230 / 230 °C | 55 / 55 °C | 1.0227 | 15 mm³/s | 100% | 70% | Not required | Standard | 55°C / 2–4 hr |
| **PLA+** | 230 / 230 °C | 55 / 55 °C | 1.0227 | 15 mm³/s | 100% | 70% | Not required | Standard | 55°C / 2–4 hr |
| **PLA Matte** | 230 / 230 °C | 55 / 55 °C | 1.0227 | 15 mm³/s | 100% | 70% | Not required | Standard | 55°C / 2–4 hr |
| **PLA CF** | 220 / 220 °C | 40 / 40 °C | Use generic PLA CF profile | — | 100% | 70% | Not required | **Hardened** | 55°C / 8 hr |

> **PLA CF:** Load the generic PLA CF profile in Bambu Studio — no modifications needed. Hardened nozzle is mandatory. Dry at 55°C for 8 hrs before printing.

---

### Aesthetic PLA

| Filament | Nozzle Temp | Bed Temp (Textured PEI) | Flow Ratio | Max Vol Speed | Fan Speed | AUX Fan | Enclosure | Drying |
|----------|-------------|------------------------|------------|--------------|-----------|---------|-----------|--------|
| **PLA Metallic** | 230 / 230 °C | 55 / 55 °C | 1.0227 | 15 mm³/s | 100% | 70% | Not required | 55°C / 2–4 hr |
| **PLA Silk** | 230 / 250 °C ¹ | 65 / 65 °C | 1.0227 | 15 mm³/s | 100% | 70% | Not required | 65°C / 2–4 hr |
| **Dual/Tri-Color Silk** | 230 / 250 °C ¹ | 65 / 65 °C | 1.0227 | 15 mm³/s | 100% | 70% | Not required | 65°C / 2–4 hr |
| **PLA Marble** | 230 / 230 °C | 55 / 55 °C | 1.0227 | 15 mm³/s | 100% | 70% | Not required | 55°C / 2–4 hr |
| **PLA Starlight** | 230 / 230 °C | 55 / 55 °C | 1.0227 | 15 mm³/s | 100% | 70% | Not required | 55°C / 2–4 hr |
| **PLA Glow in Dark** | 220 / 220 °C | 55 / 55 °C | 1.0227 | 12 mm³/s | 100% | 70% | Not required | 55°C / 2–4 hr |
| **PLA Wood** | 220 / 220 °C | 55 / 55 °C | 1.05 | 10 mm³/s | 80% | 50% | Not required | 55°C / 2–4 hr |

> ¹ **PLA Silk shiny finish:** set other-layers nozzle to 250°C. For standard finish, keep at 230/230°C.

---

### PETG

> **Abbreviations:** PETG-HS = High Speed · PETG-CF = Carbon Fibre

| Filament | Nozzle Temp | Bed Temp (Textured PEI) | Flow Ratio | Max Vol Speed | Fan Speed | AUX Fan | Enclosure | Drying |
|----------|-------------|------------------------|------------|--------------|-----------|---------|-----------|--------|
| **PETG** | 230 / 230 °C | 65 / 65 °C | 1.0227 | 15 mm³/s | 100% | 70% | Not required | 70°C / 2–4 hr |
| **PETG-HS** (High Speed) | 230 / 230 °C ² | 65 / 65 °C | 1.0227 | 15 mm³/s | 100% | 70% | Not required | 70°C / 2–4 hr |
| **PETG Translucent** | 230 / 230 °C | 65 / 65 °C | 1.0227 | 12 mm³/s | 100% | 70% | Not required | 70°C / 2–4 hr |
| **PETG-CF** (Carbon Fibre) | 240 / 250 °C | 70 / 70 °C | 1.0 | 12 mm³/s | 30–40% | 30% | Not required | 70°C / 4–6 hr |

> ² **PETG-HS temperature note:** NuMakers Bambu Studio guide recommends 230°C as starting point for Bambu printers. The product spec sheet lists the material range as 240 ± 10°C — if you experience under-extrusion or poor layer bonding, raise to 240–245°C.

> **PETG-CF:** Hardened nozzle mandatory. Reduce fan speed — too much cooling causes layer delamination.

---

### ABS / ASA

| Filament | Nozzle Temp | Bed Temp (Eng./High Temp/Tex. PEI) | Flow Ratio | Max Vol Speed | Fan (min/max) | AUX Fan | Enclosure | Drying |
|----------|-------------|-------------------------------------|------------|--------------|--------------|---------|-----------|--------|
| **ABS** | 260 / 265 °C | 90 / 90 °C | 0.95 | 22 mm³/s | 10% / 80% | 0% | **Required** | 80°C / 4–6 hr |
| **ASA** | 260 / 260 °C | 90 / 90 °C | 0.95 | 12 mm³/s | 10% / 80% | 0% | **Required** | 80°C / 4–6 hr |

> **ABS/ASA:** Use Engineering plate or High-Temp plate only — NOT cool plate or PLA plate (set to 0°C). Close enclosure before starting. No cooling for first 2–3 layers.

---

## Bed Temperature by Plate Type

| Filament Group | Cool / PLA Plate | Engineering Plate | High Temp Plate | Textured PEI |
|----------------|-----------------|-------------------|-----------------|--------------|
| PLA family | 35°C | — | 55°C | 55°C |
| PLA Silk family | 45°C | — | 65°C | 65°C |
| PETG family | 45°C | — | 65°C | 65°C |
| ABS | ❌ 0°C | 90°C | 90°C | 90°C |
| ASA | ❌ 0°C | 90°C | 90°C | 90°C |

---

## Pressure Advance (K-Value) Reference — P1S Manual Calibration

> These are starting ranges. Always run calibration for each new spool/color. Record results in `calibration-log.md`.

| Filament Group | K-Value Range | Typical Starting Point |
|----------------|--------------|----------------------|
| PLA / PLA+ / PLA Matte / PLA Metallic | 0.020 – 0.060 | 0.035 |
| PLA Silk / Dual-Tri Silk | 0.020 – 0.060 | 0.040 |
| PLA CF | 0.015 – 0.040 | 0.025 |
| PLA Wood / Glow / Starlight / Marble | 0.020 – 0.060 | 0.035 |
| PETG-HS / PETG Translucent | 0.040 – 0.080 | 0.060 |
| PETG CF | 0.030 – 0.060 | 0.040 |
| ABS | 0.030 – 0.060 | 0.040 |
| ASA | 0.030 – 0.070 | 0.045 |

---

## NuMakers Official P1S Profile File IDs

Import via Bambu Studio: **Device → Filament → Import from file**
Or download from: `https://wiki.numakers.com/printing-tips/printer-profiles`

| Filament | Profile File ID |
|----------|----------------|
| PLA+ | `3Fs0pcJHu8u37Si47aMH` |
| PLA Silk | `IBlZkOw7E8FADAokEL5b` |
| PLA Matte | `H1iJfcoa7SUMtzllihIV` |
| PLA CF | `mc9jE5eiFYb8uafgPBRB` |
| PLA Wood | `IoADtlsOCCvhqjmSRYXW` |
| PETG / PETG Translucent | `zwgyAP7UrnG5huwJo4Ay` |
| PETG CF | `JSrbJs329jJz59FD3azN` |
| ABS | `XPf7XuRqv3GYjdx507Gz` |
| ASA | `aqy7cy3fdiEHAvPlrbkt` |

---

## Cooling — First Layer Rules

| Filament Group | No Cooling First N Layers |
|----------------|--------------------------|
| PLA family | 1 layer |
| PLA Silk family | 1 layer |
| PETG family | 1 layer |
| ABS | 3 layers |
| ASA | 2 layers |

---

*Sources: [NuMakers Specification Files](https://india.numakers.com/pages/specification-files) · [NuMakers Wiki Printer Profiles](https://wiki.numakers.com/printing-tips/printer-profiles) · [Cheat Sheets](https://numakers.com/pages/cheat-sheets)*
