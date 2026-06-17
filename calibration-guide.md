# Calibration Guide — BambuLab P1S + NuMakers Filaments

*[Print Wolves](https://www.printwolves.com) · BambuLab P1S Reference*

> **Printer:** BambuLab P1S · **Nozzles in use:** 0.2 mm | 0.4 mm | 0.6 mm
> **Important:** Calibration values (flow ratio, K-value) are **nozzle-size specific**. Re-run all calibrations when swapping nozzles.

---

> Run calibrations **in this order** every time you load a new filament type or brand-new spool.
> Record all results in `calibration-log.md`.

---

## Calibration Order

```
1. First Layer / Z-Offset  →  2. Flow Rate  →  3. Flow Dynamics (K-Value)
```

Skip step 1 if Z-offset is already dialled in. Always do Flow Rate before Flow Dynamics — flow rate affects K-value results.

---

## Step 1 — First Layer / Z-Offset

**Purpose:** Ensures the nozzle is at the correct height for the first layer. Bad Z-offset makes every other calibration unreliable.

### Bambu Studio
1. Go to **Device → Calibration → First Layer Calibration**
2. Select your plate type and filament
3. Print the calibration square and inspect: nozzle too close = squished/mushed lines; too far = gaps between lines
4. Adjust via **Device → Live Z Adjust** during or after print
5. Save the offset

### OrcaSlicer
Same path: **Calibration → First Layer Calibration**

---

## Step 2 — Flow Rate Calibration

**Purpose:** Calibrates how much filament the extruder pushes out. Affects dimensional accuracy, surface quality, and layer bonding strength.

### When to re-run
- New filament brand or type
- New spool (same brand, different batch/color can vary)
- If surfaces look rough, grainy, or over-filled

---

### Bambu Studio — Flow Rate

1. Open **Calibration → Flow Rate** from the top menu
2. Select:
   - Printer: **BambuLab P1S**
   - Filament: your loaded NuMakers filament profile
   - Plate type: match what's in the printer
3. Click **Start Calibration** — printer will print a series of test squares at different flow offsets
4. Examine the squares once cooled:

   | Surface appearance | Meaning | Action |
   |--------------------|---------|--------|
   | Rough, grainy, gaps between lines | Under-extrusion | Use a higher offset sample |
   | Smooth, uniform, lines just touching | ✅ Correct | Use this sample |
   | Raised ridges, blobs at edges | Over-extrusion | Use a lower offset sample |

5. Click the winning sample number in Bambu Studio
6. If you want finer tuning, click **Calibrate** again to print a narrower range around that value
7. Save by clicking **Set Flow Ratio** — this updates `Filament → Advanced → Flow ratio`

**Typical result for NuMakers filaments:**
- PLA family: ~1.02–1.03
- PETG family: ~1.02–1.03
- ABS / ASA: ~0.94–0.96

---

### OrcaSlicer — Flow Rate

1. Go to **Calibration → Flow Rate → Coarse Calibration**
2. Select printer and filament profile
3. OrcaSlicer prints test cubes at different flow offsets — identify the cube with the smoothest top surface
4. Run **Calibration → Flow Rate → Fine Calibration** at a narrower range around the coarse result for precision
5. Enter the winning offset under **Filament → Advanced → Flow ratio**

> Note: The curved single-wall ramp in OrcaSlicer is the **Max Volumetric Speed** test — not flow rate. Do not confuse the two.

---

### Entering the Flow Ratio Manually

In both slicers:
- **Filament → (select your profile) → Advanced → Flow ratio**
- If the best sample was at **+5%** offset → set flow ratio to **1.05**
- If the best sample was at **-5%** offset → set flow ratio to **0.95**
- Default starting value per NuMakers: **1.0227** (PLA/PETG) | **0.95** (ABS/ASA)

---

## Step 3 — Flow Dynamics Calibration (Pressure Advance / K-Value)

**Purpose:** Compensates for extruder pressure lag during speed changes. Fixes corner blobs, ghosting, and gaps at sharp edges.

> The P1S does **not** have LiDAR or the eddy current sensor. It cannot auto-calibrate K-value. You must run the manual pattern test.

### When to re-run
- New filament type (PLA → PETG, etc.)
- Significantly different print temperature than before
- After changing nozzle size
- When corners look blobby or have gaps

---

### Bambu Studio — Flow Dynamics (Manual Pattern)

1. Open **Calibration → Flow Dynamics Calibration**
2. Choose **Manual Calibration**
3. Set parameters:
   - Nozzle diameter: **select your current nozzle** (0.2 / 0.4 / 0.6 mm)
   - Plate type: match your loaded plate
   - Filament: your NuMakers profile
   - Method: **Pattern** (preferred over Line — more accurate on P1S)
   - K start: `0.000`
   - K end: `0.100`
   - K interval: `0.005`
4. Click **Start** — printer will print a pattern of lines, each labelled with a K-value
5. Examine the pattern under good light:

   | Corner appearance | Meaning | Action |
   |-------------------|---------|--------|
   | Blobby, excess material at corners | K too low | Look higher in the pattern |
   | Sharp, clean corners, smooth transitions | ✅ Correct | Note this K-value |
   | Gaps / divots at corners | K too high | Look lower in the pattern |

6. Pick the **highest K that does not create gaps**
7. Enter the value: **Filament → Advanced → Pressure advance**
8. Click **Save as PA Profile** — name it e.g. `NuMakers PLA+ Black – K0.032`

---

### OrcaSlicer — Pressure Advance

1. Go to **Calibration → Pressure Advance**
2. Select **PA Pattern** test (recommended) or **PA Line**
3. Set range: start `0.000`, end `0.100`, step `0.005`
4. Print, examine corners using the same table above
5. Enter value under **Filament → Advanced → Pressure advance**
6. Save the filament profile with a descriptive name

---

### Saving & Applying Profiles (Bambu Studio v1.9+)

Bambu Studio uses **PA Profiles** to reuse calibration results:

1. After calibration, click **Save as PA Profile**
2. Name format: `NuMakers [Filament] [Color] – K[value]` (e.g. `NuMakers PETG-HS Clear – K0.058`)
3. Navigate to **Device panel → Filament settings → PA Profile**
4. Select your saved profile from the dropdown
5. The K-value is now linked to that filament slot for future prints

> PA Profiles are reusable across multiple spools of the same filament type and color. You only need to re-calibrate when switching between types.

---

## Calibration Reference — K-Value Starting Points

| Filament | Start K | Expected Range |
|----------|---------|---------------|
| PLA / PLA+ / PLA Matte / PLA Metallic | 0.035 | 0.020 – 0.060 |
| PLA Silk / Dual-Tri Silk | 0.040 | 0.020 – 0.060 |
| PLA CF | 0.025 | 0.015 – 0.040 |
| PLA Wood / Glow / Starlight / Marble | 0.035 | 0.020 – 0.060 |
| PETG-HS / PETG Translucent | 0.060 | 0.040 – 0.080 |
| PETG CF | 0.040 | 0.030 – 0.060 |
| ABS | 0.040 | 0.030 – 0.060 |
| ASA | 0.045 | 0.030 – 0.070 |

---

## Optional: Max Volumetric Speed Test

Run this if you want to push print speeds or if you notice quality drops at higher speeds.

### OrcaSlicer
**Calibration → Max Volumetric Speed** — prints a ramp that increases extrusion rate until the filament can't keep up. Note the speed where quality degrades and use 80% of that as your max.

### Bambu Studio
No direct MVS test — use the values from the NuMakers cheatsheet as your ceiling:
- PLA/PETG family: 15 mm³/s
- ASA: 12 mm³/s
- ABS: 22 mm³/s

---

## Nozzle Size — K-Value Adjustment Guide

> All K-values in this guide are measured with a **0.4 mm nozzle**. Use these multipliers when switching nozzle sizes.

| Nozzle Size | K-Value Multiplier vs 0.4 mm | Example (PLA+ base K 0.035) |
|-------------|-----------------------------|-----------------------------|
| 0.2 mm | × 0.85 (lower) | ~0.030 |
| 0.4 mm | × 1.00 (baseline) | 0.035 |
| 0.6 mm | × 1.15 (higher) | ~0.040 |

> These are approximations. Always run the pattern calibration after switching nozzle sizes — do not rely solely on the multiplier.

### Max Volumetric Speed by Nozzle (NuMakers filaments)

| Filament Group | 0.2 mm | 0.4 mm | 0.6 mm |
|----------------|--------|--------|--------|
| PLA family | 5–7 mm³/s | 15 mm³/s | 20–22 mm³/s |
| PETG family | 5–7 mm³/s | 15 mm³/s | 18–20 mm³/s |
| ABS | 8–10 mm³/s | 22 mm³/s | 28–30 mm³/s |
| ASA | 5–6 mm³/s | 12 mm³/s | 15–18 mm³/s |
| CF variants | Not recommended | 12 mm³/s | 15 mm³/s |

---

*Sources: [BambuBuilds K-Value Guide](https://bababuilds.com/blog/bambu-lab-flow-dynamics-calibration-k-value/) · [Eolas Prints Calibration Guide](https://eolasprints.com/en-us/blogs/advanced-3d-printing/bambu-studio-calibration-guide-getting-perfect-prints-every-time) · [Bambu Lab Wiki](https://wiki.bambulab.com/en/software/bambu-studio/calibration_flow_rate)*
