# NuMakers Filament Presets — BambuLab P1S

*[Print Wolves](https://www.printwolves.com) · BambuLab P1S Reference*

> Official NuMakers profiles for Bambu Studio. These are pre-tuned starting points — run your own flow rate and K-value calibration and save results on top of these.

---

## How to Import a Profile into Bambu Studio

1. Visit `https://wiki.numakers.com/printing-tips/printer-profiles`
2. Find your filament and download the file using the File ID below
3. In Bambu Studio: **Filament → (gear icon) → Import from file**
4. Select the downloaded `.json` file
5. Run **Flow Rate** and **Flow Dynamics** calibrations (see `calibration-guide.md`)
6. Save the calibrated values into the profile

---

## Available P1S Profile File IDs

| Filament | File ID | Download |
|----------|---------|----------|
| PLA+ | `3Fs0pcJHu8u37Si47aMH` | wiki.numakers.com/printing-tips/printer-profiles |
| PLA Silk | `IBlZkOw7E8FADAokEL5b` | wiki.numakers.com/printing-tips/printer-profiles |
| PLA Matte | `H1iJfcoa7SUMtzllihIV` | wiki.numakers.com/printing-tips/printer-profiles |
| PLA CF | `mc9jE5eiFYb8uafgPBRB` | wiki.numakers.com/printing-tips/printer-profiles |
| PLA Wood | `IoADtlsOCCvhqjmSRYXW` | wiki.numakers.com/printing-tips/printer-profiles |
| PETG / PETG Translucent | `zwgyAP7UrnG5huwJo4Ay` | wiki.numakers.com/printing-tips/printer-profiles |
| PETG CF | `JSrbJs329jJz59FD3azN` | wiki.numakers.com/printing-tips/printer-profiles |
| ABS | `XPf7XuRqv3GYjdx507Gz` | wiki.numakers.com/printing-tips/printer-profiles |
| ASA | `aqy7cy3fdiEHAvPlrbkt` | wiki.numakers.com/printing-tips/printer-profiles |

> **Note:** PLA, PLA Metallic, PETG-HS, PLA Marble, PLA Starlight, PLA Glow — if no dedicated profile ID is listed, use the nearest base profile (e.g., PLA+ profile for PLA / PLA Metallic; PETG profile for PETG-HS) and apply your calibrated values on top.

---

## Nozzle Sizes

NuMakers profiles are built for 0.4 mm. When using 0.2 mm or 0.6 mm nozzles:
- Import the base profile normally
- Bambu Studio will auto-adjust some speed limits for the nozzle size
- **Always re-run flow rate and flow dynamics calibration after switching nozzle sizes**
- Save separate profiles per nozzle size using the naming convention below

---

## Profile Naming Convention (Bambu Studio)

When saving a calibrated profile, use this format so it's easy to find:

```
NuMakers [Filament] [Color] [Nozzle] – FR[flow ratio] K[k-value]
```

Examples:
- `NuMakers PLA+ Black 0.4mm – FR1.023 K0.034`
- `NuMakers PETG-HS Clear 0.4mm – FR1.022 K0.058`
- `NuMakers ASA Grey 0.4mm – FR0.95 K0.045`

---

## Filament Profiles Not Listed Above

For filaments without a dedicated NuMakers profile, use these base profiles as a starting point:

| Filament | Use this base profile |
|----------|----------------------|
| PLA | PLA+ profile |
| PLA Metallic | PLA+ profile |
| PLA Marble | PLA+ profile |
| PLA Starlight | PLA+ profile |
| PLA Glow in the Dark | PLA+ profile (reduce MVS to 12) |
| PETG-HS | PETG profile |
| PETG Translucent | PETG profile |
| Dual/Tri-Color Silk | PLA Silk profile |

---

*Profile source: [NuMakers Wiki — Printer Profiles](https://wiki.numakers.com/printing-tips/printer-profiles)*
