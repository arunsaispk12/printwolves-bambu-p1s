# Print Guide — NuMakers Filaments on BambuLab P1S

*[Print Wolves](https://www.printwolves.com) · BambuLab P1S Reference*

> Per-material tips, troubleshooting, bed prep, storage, and quality advice.

---

## Bed Surface Guide

| Filament | Recommended Plate | Avoid | Adhesive Needed? |
|----------|------------------|-------|-----------------|
| PLA / PLA+ / PLA Matte | Textured PEI or Cool Plate | — | Usually no |
| PLA Silk / Dual-Tri Silk | Textured PEI or High Temp | — | Optional glue stick |
| PLA Marble / Starlight / Glow | Textured PEI | — | Optional |
| PLA Wood | Textured PEI | — | Optional glue stick |
| PLA Metallic | Textured PEI | — | Optional |
| PLA CF | Textured PEI | — | Optional |
| PETG-HS | Textured PEI or High Temp | Cool Plate (sticks too well) | Optional — thin layer glue stick prevents over-adhesion |
| PETG Translucent | Textured PEI or High Temp | Cool Plate | Optional thin glue stick |
| PETG CF | Textured PEI | Cool Plate | Optional |
| ABS | Engineering Plate or High Temp | ❌ Cool Plate / PLA Plate | ABS slurry or glue stick for large prints |
| ASA | Engineering Plate or High Temp | ❌ Cool Plate / PLA Plate | Glue stick recommended |

> **PETG on PEI:** Apply a very thin layer of glue stick (release agent) to prevent the PETG from bonding too strongly to the PEI surface and causing sheet damage.

---

## Enclosure Rules

| Filament | Enclosure | Door | Chamber Temp |
|----------|-----------|------|-------------|
| PLA family (all variants) | Open or closed | Open preferred | Ambient |
| PETG family | Open or closed | Open preferred | Ambient |
| ABS | **Closed — mandatory** | Fully closed | ≥ 40°C recommended |
| ASA | **Closed — mandatory** | Fully closed | ≥ 40°C recommended |

> For ABS/ASA: close the door before starting the print, not after. Let the chamber warm up during the first few layers.

---

## Drying Guide

| Filament | Temp | Duration | Signs of wet filament |
|----------|------|----------|----------------------|
| PLA / PLA+ / PLA Matte | 55°C | 2–4 hr | Popping/crackling sounds, bubbles, poor surface |
| PLA Silk / Dual-Tri | 65°C | 2–4 hr | Dull finish, stringing, poor layer bonding |
| PLA Wood / Starlight / Glow / Marble / Metallic | 55°C | 2–4 hr | Popping, rough surface |
| PLA CF | 55°C | 8 hr | Brittle prints, popping |
| PETG-HS / PETG Translucent | 70°C | 2–4 hr | Cloudiness, stringing, weak layers |
| PETG CF | 70°C | 4–6 hr | Popping, delamination |
| ABS | 80°C | 4–6 hr | Bubbles on surface, warping |
| ASA | 80°C | 4–6 hr | Bubbles, warping, stringing |

> Store all filament in airtight containers with silica desiccant when not in use. PETG and ABS/ASA are especially hygroscopic.

---

## Per-Material Tips

### PLA / PLA+
- Fastest and easiest to print
- Cool the part actively — 100% fan from layer 2 onwards
- Enable ironing for top surfaces on decorative prints
- Stringing: reduce temp by 5°C increments; tune retraction
- First layer not sticking: clean bed with IPA, increase bed temp by 5°C
- Dimensional accuracy issues: run flow rate calibration

### PLA Silk / Dual-Tri Color Silk
- For a shiny finish: set other-layers nozzle temp to 250°C (first layer stays at 230°C)
- Print slightly slower than standard PLA for best sheen
- Keep fan at 100% — silk PLA needs active cooling to prevent drooping on overhangs
- Stringing is common — fine-tune retraction and reduce travel speed
- Avoid printing in high-humidity environments without drying first

### PLA Wood
- Use 0.4 mm nozzle minimum — wood fiber can clog smaller nozzles
- Do not exceed 230°C — higher temps can cause wood particles to char
- Reduce fan speed (80%) — aggressive cooling causes layer cracking
- Sand the finished print for a more realistic wood appearance
- Use staining or painting for enhanced wood effect

### PLA Glow in the Dark
- Abrasive — hardened nozzle strongly recommended for extended runs
- Reduce print speed slightly vs. standard PLA for better glow particle dispersion
- Do not use dark build plates — makes first layer inspection harder
- Charge under bright UV or sunlight for best glow effect

### PLA CF (Carbon Fiber)
- **Hardened nozzle is mandatory** — standard brass nozzles will wear within hours
- No enclosure needed
- Layer adhesion is excellent but the material is slightly brittle — avoid thin walls < 1.2 mm
- Use at least 3 perimeters for structural parts
- Sand or prime the surface to fill the rough texture if finish is critical

### PETG-HS
- Apply thin glue stick layer to PEI to avoid sheet damage on removal
- Fan at 100% as per NuMakers Bambu Studio profile — PETG-HS is engineered to handle active cooling at speed
- If you notice layer cracking or poor adhesion, reduce fan to 50% as a diagnostic step
- Stringing more common than PLA — increase retraction and reduce travel speed
- High-speed mode: works best with temp at 240°C and a clean dry spool

### PETG Translucent
- Print slowly for best clarity — 40–50 mm/s outer walls
- Avoid touching the print surface — oils from hands cause hazing
- Use 0% infill with 3+ perimeters for light-pipe or lens applications
- Fan at 100% for maximum clarity

### PETG CF
- **Hardened nozzle mandatory**
- Reduce fan speed (30–40%) — over-cooling causes layer delamination
- Structural parts: use 4+ perimeters, 40%+ infill
- Avoid large flat surfaces without brims — slight warping possible

### ABS
- Enclosure is mandatory — open enclosure causes rapid warping and layer splitting
- No auxiliary fan (set to 0%) — keep chamber warm
- Skirt recommended for large prints to stabilize chamber temp
- Smooth surface with acetone vapor for an ABS-specific finish
- Avoid drafts or AC vents near the printer during printing
- If warping: increase bed temp to 100°C, add brim, use ABS slurry on bed

### ASA
- Enclosure mandatory — ASA warps similarly to ABS
- UV-stable — preferred over ABS for outdoor functional parts
- Bed adhesion is trickier than ABS — use glue stick or hairspray
- Reduce fan to absolute minimum (10%) for first half of print
- Chamber temp should reach at least 35–40°C before printing tall objects

---

## Troubleshooting Quick Reference

| Symptom | Likely Cause | Fix |
|---------|-------------|-----|
| Stringing between parts | Temperature too high / retraction too low | Lower nozzle temp 5°C; increase retraction distance |
| Rough, grainy surface | Under-extrusion | Run flow rate calibration; increase temp 5°C |
| Blobs at corners | K-value too low | Run flow dynamics calibration; increase K |
| Gaps at corners | K-value too high | Decrease K-value |
| First layer not sticking | Bed dirty / Z too high / temp too low | Clean with IPA; lower Z-offset; raise bed temp |
| Warping (ABS/ASA) | Chamber too cool / no brim | Close enclosure; add brim; raise bed temp to 100°C |
| Layer delamination (PETG CF) | Fan too high | Reduce fan to 30–40% |
| Clogged nozzle (CF filaments) | Brass nozzle used / temp too low | Switch to hardened nozzle; raise temp 5°C |
| Popping / crackling sounds | Wet filament | Dry per drying guide above |
| Cloudy / dull PETG Translucent | Wet filament or temp too high | Dry 70°C 4hr; lower temp 5°C |
| Weak layer bonding | Under-extrusion or temp too low | Check flow ratio; raise nozzle temp 5°C |
| Elephant foot (first layer too wide) | Z-offset too close | Raise Z-offset; lower first layer flow |
| Over-extrusion (thick layers) | Flow ratio too high | Run flow rate calibration; reduce flow ratio |
| Nozzle dragging on print | Z too low or over-extrusion | Raise Z-offset; check flow ratio |

---

## First Layer Checklist (Before Every Print)

- [ ] Bed cleaned with IPA and lint-free cloth
- [ ] Correct plate installed and selected in slicer
- [ ] Filament loaded and purged (fresh purge line)
- [ ] Spool not tangled — feed path clear
- [ ] Filament dried if stored open > 48 hours (PETG/ABS/ASA) or > 1 week (PLA)
- [ ] Enclosure closed (ABS / ASA only)
- [ ] Correct filament profile active in slicer (including calibrated flow ratio and K-value)
- [ ] Z-offset confirmed for current plate

---

## Print Speed Recommendations

| Use Case | Outer Wall | Inner Wall | Infill | First Layer |
|----------|-----------|-----------|--------|-------------|
| Quality / detail | 40–60 mm/s | 80 mm/s | 120 mm/s | 20–30 mm/s |
| Standard | 80–100 mm/s | 150 mm/s | 200 mm/s | 30–40 mm/s |
| High speed (PLA+, PETG-HS) | 150–200 mm/s | 250 mm/s | 300 mm/s | 40 mm/s |
| ABS / ASA | 60–80 mm/s | 100 mm/s | 150 mm/s | 20–30 mm/s |

---

*Sources: [NuMakers PLA+ Guide](https://india.numakers.com/blogs/news/ultimate-3d-printing-guide-for-pla-filament) · [NuMakers PETG Guide](https://india.numakers.com/blogs/news/ultimate-3d-printing-guide-for-petg-filament) · [NuMakers ASA Guide](https://india.numakers.com/blogs/news/ultimate-3d-printing-guide-for-asa-filament)*
