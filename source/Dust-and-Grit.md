# IDR: Dust (D) and Grit (G)

**Test documentation · Draft v0.2**

This document defines how the D and G groups of the IDR code are tested and rated. It applies to smartphones, tablets, foldables and other portable electronic devices, and it has two test tiers: a **home** tier for an individual testing one device they intend to keep, and a **lab** tier for testers who can sacrifice and tear down two or more devices.

---

## 1. Scope

| Group | Tests | Threat |
|---|---|---|
| **D**, Dust | Sealing | Fine particles slipping through seals into the device |
| **G**, Grit | Mechanism tolerance | Coarse particles jamming or grinding moving parts |

Both groups use the same procedure and the same 0–9 scale. Only the test medium and the full dose differ.

**Moving parts** means any part that moves in normal use: hinges, slides, buttons and keys, ports and port covers, trays, and rotating crowns or dials.

---

## 2. Test tiers

| | Home | Lab |
|---|---|---|
| **Units** | 1 | 2 or more |
| **Device fate** | Kept: the tester intends to keep it working | Sacrificed |
| **Device condition** | Any, from new to heavily used; recorded as found | Spread across wear: one new, one heavily used (real or simulated), and further units filling in the levels between |
| **Ladder** | Stops at the first effect, or at the tester's chosen maximum level (§8.3) | Runs to failure or level 9 |
| **Teardown** | No | Yes, every unit |
| **Can detect enclosure breach (E)** | Electrical faults only | Yes |
| **Code prefix** | `IDR1*` | `IDR1` |
| **IDRS short code** | Cannot be issued | Can be issued |

Home results are useful for comparing devices and spotting weak points, but they cannot confirm sealing, so the `*` marks them as never equivalent to lab results.

How device condition is measured, and how results from several units combine into one published code, will be defined in the usage (U) documentation [TBD]. Until then, lab reports list each unit's results separately alongside its wear condition.

---

## 3. Safety

- **Wear a respirator** (N95 minimum, P100 recommended) and safety glasses whenever handling, sieving or applying either medium.
- **Sand contains crystalline silica.** Sieving and agitating it releases respirable silica dust, which causes silicosis. This applies even to "washed" play sand. Work outdoors or with strong ventilation.
- **Do not use** silica flour, ground glass, or other fine abrasive powders in the home kit.
- **Stop immediately** if the device becomes hot, swells, smells, or smokes. Move it outdoors onto a non-flammable surface.
- Back up the device before testing.
- **Home testers:** the procedure aims to keep the device working, but there is no guarantee. Some debris may stay in the device permanently, and deliberately contaminating a device may void its warranty.

---

## 4. Equipment

### Home kit

| Item | Purpose | Notes |
|---|---|---|
| Kitchen scale, 0.1 g resolution | Weighing doses | Required. Volume measures are not accurate enough (§6.3) |
| Test sieves: #20, #40, #100, #200 (ASTM E11) | Grading media | 850, 425, 150 and 75 µm openings. Sold individually and inexpensively |
| Clear plastic storage bin with lid | Containing media during application | Large enough to operate the device's moving parts inside |
| Soft paintbrush, ~2 cm | Working media into seams; cleaning | Dedicated to testing |
| Hand air blower (camera "rocket" blower) | Recovery cleaning (§8.4) | Not canned air |
| Feeler gauge set, 0.05–1.0 mm | Closure gap | Hinged or closing devices only |
| Digital luggage scale or push-pull gauge | Hold force | Devices with magnets, detents or latches only |
| Ruler or calipers | Exposure area | |
| Thermometer/hygrometer | Recording conditions | Humidity affects how powders clump |
| Second phone or camera | Photos, audio and video records | |
| UV flashlight (365 nm) + UV-fluorescent pigment powder | Optional: making ingress visible | Mix about 1% pigment by mass into the D medium |

### Lab kit

Everything in the home kit, plus:

- ISO 12103-1 test dust for the D medium (§5)
- A sieve shaker
- UV tracer and UV flashlight (**required** for D tests, so teardown can show where dust got in)
- Teardown tools for each device under test

---

## 5. Test media

| | D medium | G medium |
|---|---|---|
| **Home kit** | Calcium carbonate powder, passing the #200 sieve (< 75 µm) | Play sand, sieved into two fractions and blended 50/50 by mass: 150–425 µm (passes #40, held on #100) and 425–850 µm (passes #20, held on #40) |
| **Lab kit** | ISO 12103-1 A1–A2 blend | Same sieved blend as the home kit, from graded silica test sand |
| **Preparation** | Store sealed; use as supplied after sieving | Oven-dry at 105–110 °C for 1 hour, cool before use |
| **Reuse** | Discard after each full test | Re-sieve before reuse |

**Why two different materials:** sealing (D) depends mainly on particle *size*, so a soft, low-hazard mineral like calcium carbonate is a reasonable home substitute. Mechanism damage (G) depends on particle *hardness* as well, so G uses real quartz sand.

Particles finer than 75 µm cannot be produced with hand sieves. A home tester who wants an ultrafine medium (< 10 µm) must buy a graded powder and record its datasheet particle size in the report.

---

## 6. Dose

### 6.1 Exposure area

Dose scales with the device's **exposure area**, not its mass. Particles get in through surfaces, seams and moving parts, so a dense device and a light device of the same size have the same exposure.

```
A = sum of (length × width) of the largest face of each rigid section, in cm²
```

| Device type | Rigid sections | A |
|---|---|---|
| Slab phone or tablet | 1 | Front face |
| Book-style foldable | 2 | Both halves (equals the unfolded face) |
| Flip-style foldable | 2 | Both halves |
| Laptop | 2 | Base + lid |

Devices with hinges receive a larger dose automatically, in proportion to their extra surfaces and seams.

### 6.2 Dose formula

```
Dose (g) = (A ÷ 100) × F × p
```

| Symbol | Meaning |
|---|---|
| A | Exposure area, cm² |
| F | Full dose per 100 cm²: **25 g for D**, **100 g for G** |
| p | Cumulative fraction of the full dose for the level (§7) |

Example values:

| Device | A | D, lvl 1 | D, lvl 5 | D, lvl 9 | G, lvl 1 | G, lvl 5 | G, lvl 9 |
|---|---|---|---|---|---|---|---|
| Phone, 16 × 7.5 cm | 120 cm² | 0.6 g | 7.5 g | 30 g | 2.4 g | 30 g | 120 g |
| Book foldable, 16 × 12.5 cm unfolded | 200 cm² | 1.0 g | 12.5 g | 50 g | 4.0 g | 50 g | 200 g |
| Tablet, 24 × 17 cm | 408 cm² | 2.0 g | 25.5 g | 102 g | 8.2 g | 102 g | 408 g |

### 6.3 Why grams and not tablespoons

Powders pack differently depending on the product and how they're scooped. One tablespoon (15 mL) of dry sand weighs roughly 23 g, but a tablespoon of fine powder can weigh anywhere from about 5 to 15 g. Tablespoon figures may be used as rough guidance (Appendix A), but **the weighed mass is what counts.**

---

## 7. The 0–9 scale

Levels are **cumulative**: each level adds more medium and more cycles on top of the previous one, with no cleaning in between. This reproduces debris building up over time.

| Level | Severity | Cumulative dose (p) | Cumulative cycles |
|---|---|---|---|
| 0 | Failed level 1 | n/a | n/a |
| 1 | Trace | 2% | 10 |
| 2 | Trace | 5% | 20 |
| 3 | Light | 10% | 30 |
| 4 | Light | 15% | 50 |
| 5 | Moderate | 25% | 75 |
| 6 | Moderate | 35% | 100 |
| 7 | Heavy | 50% | 150 |
| 8 | Heavy | 75% | 200 |
| 9 | Buried | 100% | 250 |

For each level, apply the *difference* between that level's cumulative dose and the previous level's, and run the difference in cycles.

**One cycle** means operating every moving part through its full range once, at about one cycle every 2 seconds:

- Hinges and slides: fully closed to fully open and back.
- Buttons and keys: pressed once each. (For keyboards, a fixed set of keys defined in the report.)
- Crowns and dials: one full turn each way.
- Port covers and trays: opened and closed once every 10 cycles.
- Ports: a plug inserted and removed once every 10 cycles.

---

## 8. Procedure

### 8.1 Before testing

1. Remove cases, covers and screen protectors.
2. Record the device's condition (age, visible wear, prior repairs). Lab units are preconditioned to their assigned wear levels per the U documentation [TBD].
3. Record temperature and humidity.
4. Measure the exposure area and calculate the dose for every level.
5. Take **baseline measurements** (§9) for every applicable effect.
6. Home testers: choose a maximum level in advance, if you want one.

### 8.2 Each level

1. **Weigh** the dose increment for this level.
2. **Place the device** inside the bin in its most open state (hinged devices fully open; slab devices front face up).
3. **Apply half** the increment, sprinkled evenly from about 10 cm above. Shaking it through the #20 sieve gives an even spread.
4. **Brush** each seam, hinge line and port opening with 5 light strokes.
5. **Run half** the level's cycles.
6. **Turn the device over** (hinged devices: close it). Apply the other half of the increment to the exposed faces, edges and ports, brush, and run the remaining cycles.
7. **Shed loose material:** hold the device edge-down and tap it 3 times on each long edge onto a folded towel. Do not blow or wipe the seams at this stage.
8. **Measure** every applicable effect (§9) and record the results.
9. **Grade the level** (§10) and decide whether to continue (§8.3).

### 8.3 When to stop

| Tier | Continue to the next level unless… |
|---|---|
| **Home** | Any effect other than `i` appeared at this level, the chosen maximum level was reached, or level 9 was completed |
| **Lab** | The level was failed (an uppercase effect appeared), or level 9 was completed |

Home testers stop at the first sign of degradation to give the device the best chance of surviving.

### 8.4 After testing: home tier (recovery)

1. Tap out loose material on every edge.
2. Use the hand air blower **across** seams, grilles and ports, not straight into them, while operating moving parts slowly to work debris out.
3. Brush seams and ports gently with the soft brush.
4. Clean the screen with a dry lint-free cloth.
5. Do **not** use liquids or canned air. Canned air is high pressure and can drive debris deeper.
6. **Repeat the measurements** (§9) and record them. An effect that remains after cleaning is likely permanent, which is useful to report.

### 8.5 After testing: lab tier (teardown)

1. Photograph every face, seam and port under UV light.
2. Tear down the device. Inspect each sealed compartment for debris and photograph with UV light.
3. Inspect hinge and mechanism internals for debris, scoring and damaged parts. Photograph and describe.
4. Record any enclosure breach (E) with its location.

---

## 9. Measurements and effect thresholds

Take every applicable measurement at baseline and after each level. Effects that don't apply to a device (for example, closure gap on a slab phone) are recorded as N/A.

| Effect | How to measure | Applies to |
|---|---|---|
| Closure gap | Feeler gauge at the free edge: three points along it. Record the largest. Insert gently without forcing | Hinged or closing devices |
| Hold force | Tape a string loop to the centre of the free edge. Pull perpendicular with the luggage scale or gauge until it opens. Average the peak of 3 pulls | Devices with magnets, detents or latches |
| Grinding | Record audio and video of 10 cycles from 30 cm, in a quiet room. Note anything heard or felt | Devices with moving parts |
| Buttons and ports | Press each button or key 5 times; all presses must register. Insert a plug into each port | All |
| Screen | Display full-screen white, mid-grey and black. Photograph at 0° and 45° under the same lighting. Draw a grid in a drawing app to check touch | Devices with displays |
| Ingress | Inspect seams, gaps, grilles and ports with a flashlight (UV light if tracer was used) | All |

### Thresholds (provisional)

| Letter | Effect | Lowercase (within tolerance) | Uppercase (failure) |
|---|---|---|---|
| b | Buttons, keys or ports | Stiff or gritty; plug meets resistance | Does not register; plug cannot seat |
| c | Closure gap | Increase of more than 0.3 mm over baseline | Increase of more than 1.0 mm, or will not stay closed |
| E | Enclosure breach or electrical fault | n/a | Debris inside a sealed compartment (lab teardown only), or electrical fault (reboots, charging failure, sensor errors) |
| h | Hold force | Change of more than 15% from baseline | Change of more than 40%, or no hold |
| i | Ingress only | Debris visible in seams, grilles or ports with no other effect | n/a |
| r | Rough motion (grinding) | Grinding or crunching heard at 30 cm or felt | Moving part binds: cannot complete its full range with normal hand force |
| s | Screen | Marks or pressure points visible on grey at 45° | Dead pixels, lines, cracks, or touch dead zones |

All threshold values are provisional and will be adjusted once real devices have been tested (§13).

---

## 10. Grading

- A level is **passed** if no uppercase effect appeared after it.
- The **digit** is the highest level passed (0 if level 1 failed).
- **Lowercase letters** are every effect present at the rated level, in alphabetical order. `i` is used only when no other effect is present.
- The **uppercase letter** is the failure effect at the next level up. If several failures appear at once, use the most severe, in this order: E, S, C, R, H, B.
- **No uppercase letter** means no failure was reached. With a digit of 9, the device passed the whole ladder. With a digit below 9, testing was stopped first, which is normal for home tests.
- **Enclosure breaches found at teardown** are recorded in the report with their location. Because a teardown can't show at which level the breach happened, that unit's D result is marked unverified in the report, and no IDRS dust digit can be issued from it (see §13).

### Examples (hypothetical)

| Code | Tier | Meaning |
|---|---|---|
| `D5r` | Home | Passed moderate dust; grinding appeared at level 5, so testing stopped to protect the device |
| `G3` | Home | Passed light grit with no effects; the tester's chosen maximum was 3 |
| `D9` | Lab | Passed buried fine dust with nothing getting in |
| `D7iE` | Lab | Passed heavy fine dust with debris visible in seams but no effect; electrical fault at level 8 |
| `G6rC` | Lab | Passed moderate grit with grinding; at level 7 the hinge would not close |
| `G3hrR` | Lab | Passed light grit with loosened hold and grinding; at level 4 the hinge bound |

---

## 11. Short code (IDRS)

- **Lab tier only.**
- The IDRS digit is the highest level passed with **no letters other than `i`**, taken from the per-level records in the report (not from the code).
- **Multiple units:** how unit results combine will be set in the U documentation [TBD]. Until then, use the **lowest** digit across all units.

---

## 12. Report checklist

- Tier (home or lab)
- Device model, firmware version, number of units, serial numbers
- Condition of each unit (and assigned wear level for lab units)
- Kit and media used: sources, sieve fractions, tracer
- Temperature and humidity
- Exposure area and calculated doses
- Baseline and per-level measurements for every applicable effect
- Photos, audio and video for every level
- Home: chosen maximum level, why testing stopped, and measurements after recovery cleaning
- Lab: teardown findings and photos for every unit
- Final D and G codes for each unit, and IDRS digits (lab only)

---

## 13. Open issues

1. **Timing of enclosure breaches.** Teardown shows that dust got into a sealed compartment, but not at which level. One possible fix is a separate **verification unit** taken straight to a claimed level and then torn down.
2. **Combining multiple units.** To be defined alongside the wear metric in the U documentation.
3. **Calibration.** The doses and thresholds are starting points. After testing a range of devices, adjust them so real devices spread across levels 1–9. If almost everything scores 0 or 9, the scale is set wrong.
4. **Home vs lab equivalence.** Test the same model with both kits and compare.
5. **Cycling consistency.** Hand cycling varies between testers. A motorized cycling rig with a fixed speed and range would make results more repeatable.

---

## Appendix A: Approximate volume conversions (informative only)

| Medium | Approx. bulk density | 1 tbsp (15 mL) |
|---|---|---|
| Dry sand | 1.5–1.6 g/mL | about 23 g |
| Fine powders (calcium carbonate, etc.) | 0.3–1.0 g/mL, depending on product and packing | about 5–15 g |

For a typical phone at level 9, that's roughly 5 tablespoons of sand for G, and anywhere from 2 to 6 tablespoons of powder for D. The width of that range is why §6.3 requires weighing.
