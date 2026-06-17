# Calibration Log — NuMakers × BambuLab P1S

*[Print Wolves](https://www.printwolves.com) · BambuLab P1S Reference*

> Fill in one row per spool calibrated. Run calibrations in order: Flow Rate → Flow Dynamics (K-Value).
> See `calibration-guide.md` for step-by-step procedures.

---

## How to Use This Log

1. After completing flow rate calibration, record the **Flow Ratio** result
2. After completing pressure advance calibration, record the **K-Value** result
3. Save the values into your Bambu Studio or OrcaSlicer filament profile
4. Use the **Profile Name** column to track what you saved in the slicer

---

## Calibration Log

| Date | Filament | Color | Nozzle Size | Spool Batch / Notes | Flow Ratio | K-Value | PA Profile Name (in slicer) | Print Temp (°C) | Bed Temp (°C) |
|------|----------|-------|-------------|---------------------|------------|---------|----------------------------|-----------------|---------------|
| | PLA+ | | 0.4 mm | | | | | 230 | 55 |
| | PLA+ | | 0.4 mm | | | | | 230 | 55 |
| | PLA Silk | | 0.4 mm | | | | | 230 | 65 |
| | PETG-HS | | 0.4 mm | | | | | 230 | 65 |
| | ABS | | 0.4 mm | | | | | 260 | 90 |
| | ASA | | 0.4 mm | | | | | 260 | 90 |
| | PLA CF | | 0.4 mm | | | | | 220 | 40 |
| | PETG CF | | 0.4 mm | | | | | 240 | 70 |

> Add rows as needed. Copy a blank row below.

**Blank row to copy:**
```
| | | | | | | | | | |
```

---

## Flow Rate Reference (NuMakers defaults)

| Filament Group | Default Flow Ratio | Typical Calibrated Range |
|----------------|--------------------|--------------------------|
| PLA / PLA+ / PLA Matte / Silk | 1.0227 | 1.00 – 1.05 |
| PLA Wood / Glow / Starlight / Marble / Metallic | 1.0227 | 1.00 – 1.08 |
| PLA CF | Use generic PLA CF profile | 0.95 – 1.05 |
| PETG-HS / PETG Translucent | 1.0227 | 1.00 – 1.05 |
| PETG CF | 1.00 | 0.95 – 1.05 |
| ABS | 0.95 | 0.90 – 0.98 |
| ASA | 0.95 | 0.90 – 0.98 |

---

## K-Value Reference (NuMakers starting points)

| Filament Group | Starting K | Typical Range |
|----------------|-----------|---------------|
| PLA / PLA+ / PLA Matte / PLA Metallic | 0.035 | 0.020 – 0.060 |
| PLA Silk / Dual-Tri Silk | 0.040 | 0.020 – 0.060 |
| PLA CF | 0.025 | 0.015 – 0.040 |
| PLA Wood / Glow / Starlight / Marble | 0.035 | 0.020 – 0.060 |
| PETG-HS / PETG Translucent | 0.060 | 0.040 – 0.080 |
| PETG CF | 0.040 | 0.030 – 0.060 |
| ABS | 0.040 | 0.030 – 0.060 |
| ASA | 0.045 | 0.030 – 0.070 |

---

## Applying Values to the Printer

### Bambu Studio
1. Open **Filament → (your profile) → Advanced**
2. Set **Flow ratio** to your calibrated value
3. Set **Pressure advance** to your K-value
4. Click **Save** (overwrite existing) or **Save as** (new profile)
5. In **Device panel → Filament slot → PA Profile**, select your saved profile

### OrcaSlicer
1. Open **Filament → (your profile) → Advanced**
2. Set **Flow ratio** and **Pressure advance**
3. Click **Save preset**
4. When loading a print, select this preset for the corresponding filament slot
