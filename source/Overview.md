# IDR: Ingress & Durability Rating

**Overview · Draft v0.1**

IDR (Ingress & Durability Rating) is an independent, unofficial rating system for the dust, grit, water and wear resistance of mobile phones, tablets, foldable smartphones, and similar handheld devices. It is not affiliated with IEC 60529 (the IP code).

## Why IDR exists

IP ratings test a new device's sealed enclosure while it sits still. Hinges and other moving parts sit outside that enclosure, and in real life a device is worn and moving when dirt and water reach it. A device can carry IP68 while its hinge fills with grit and stops closing.

## Core principle

**Devices are tested as used: worn first, with moving parts operating.**

1. Every test runs on the same unit, in a fixed order: wear (U), then dust (D), then grit (G), then water (W).
2. Every part that moves in normal use (hinges, buttons, trays, port covers) is operated during dust, grit and water exposure.
3. Results record what happened, including partial damage, not only pass or fail.

## Two forms

| Form | Example | Used for |
|---|---|---|
| Full code (**IDR**) | `IDR1 U2 D3 G2gC W52` | Spec sheets, reviews, test reports |
| Short code (**IDRS**) | `IDRS 315` | Packaging and marketing |

Every IDRS code is derived from a full IDR test report, using the rules in the IDRS section below.

---

## Full code (IDR)

### Grammar

```
IDR{version} U… D… G… W…
```

Each group is written as:

**group letter + level digit(s) + effect letters (lowercase) + failure letter (uppercase, optional)**

- **Version:** the major spec version, written straight after the prefix (`IDR1`). Codes from different major versions are not comparable.
- **Groups:** always all four, always in the order U, D, G, W, separated by spaces.
- **X:** replaces the digit(s) when a group was not tested (`GX`). An untested group carries no letters.
- **Effect letters:** lowercase, in alphabetical order, describing what was observed at the rated level. No letters means no ingress and no effect.
- **Failure letter:** one uppercase letter naming the effect that caused failure at the next level up. Omitted if the device passed the top level.

### Reading a full code

| Slot | Example | Meaning |
|---|---|---|
| Prefix | `IDR1` | Ingress & Durability Rating, spec version 1 |
| Usage | `U2` | Tested after level-2 simulated wear, no effects |
| Dust | `D3` | Passed fine dust at heavy dose, no ingress |
| Grit | `G2gC` | Passed grit at moderate dose with grinding; at heavy dose it would not close |
| Water | `W52` | Passed 6 m for 30 minutes |

### U: Usage preconditioning

Simulated wear, applied before all other tests.

| Level | Meaning |
|---|---|
| U0 | Tested new, no preconditioning |
| U1 to U4 | Increasing wear: fold cycles, button presses, port insertions, drops. Cycle counts per level [TBD] |

The digit is the highest wear level completed. Effect letters record damage seen after wear (for example `U2h` means hold force had dropped). If the device fails during preconditioning, the failure letter records why, and the remaining groups are tested on a fresh unit preconditioned to the last completed level.

### D: Dust (sealing)

**Medium:** fine test dust, ISO 12103-1 A1–A2 blend.
**Tests:** whether seals keep fine particles out of the device.

### G: Grit (mechanism tolerance)

**Medium:** coarse blend, ISO 12103-1 A4 plus 150–850 µm sand.
**Tests:** whether moving parts keep working with debris inside them.

### Dose levels (D and G)

| Level | Dose |
|---|---|
| 0 | Failed at the lightest dose |
| 1 | Light [TBD g] |
| 2 | Moderate [TBD g] |
| 3 | Heavy, mechanism buried [TBD g] |

The digit is the highest dose passed. A pass may include lowercase effects as long as they stay within tolerance.

### W: Water

Written as `W{depth}{time}`.

| Depth tier | Depth | | Time tier | Duration |
|---|---|---|---|---|
| 1 | Spray / splash | | 1 | 10 min |
| 2 | 1 m | | 2 | 30 min |
| 3 | 2 m | | 3 | 1 h |
| 4 | 4 m | | 4 | 4 h |
| 5 | 6 m | | | |

- **Depth digit:** the deepest tier passed at time tier 1.
- **Time digit:** the longest time tier passed at that depth.
- A device that fails depth tier 1 is written `W0` with its failure letter and no time digit.
- Fresh water only. Salt and chlorinated water are planned as future groups.

### Effect letters (closed list)

Testers may only use letters from this list. Lowercase means observed but within tolerance; uppercase means the cause of failure.

| Letter | Effect | Groups | Lowercase | Uppercase |
|---|---|---|---|---|
| b | Buttons or ports impaired | All | Yes | Yes |
| c | Closure gap (uppercase: will not close within tolerance) | All | Yes | Yes |
| E | Enclosure breach (dust or liquid inside the sealed compartment) or electrical fault | D, G, W | No | Yes |
| f | Fogging or condensation inside a lens or display | W | Yes | Yes |
| g | Grinding or crunching during movement | All | Yes | Yes |
| h | Hold or closing force reduced (magnets, detents) | All | Yes | Yes |
| i | Ingress only, no measurable effect (used alone) | D, G, W | Yes | No |
| m | Audio impaired after the drying period [TBD] | W | Yes | Yes |
| s | Screen marks, pressure points or dead pixels | All | Yes | Yes |

Tolerance values for each effect are set in the full specification [TBD].

---

## Short code (IDRS)

### Format

```
IDRS {dust}{grit}{water}
```

Three digits in a fixed order: dust, grit, water. Example: `IDRS 315`, read "I-D-R-S three-one-five."

### Derivation rules

1. **Never better than the full result.** When a rule is unclear, round down.
2. **Clean passes only.** The dust and grit digits are the highest dose passed with no effect letters other than `i`.
3. **Fixed wear level.** An IDRS code may only be issued from a test at the standard wear level (U2 [TBD]) or higher. Tests at lower wear levels can produce a full code but not an IDRS code.
4. **Fixed water duration.** The water digit is the deepest depth tier passed cleanly for at least time tier 2 (30 minutes).
5. **Untested groups.** Shown as X, e.g. `IDRS 3X5`.
6. **Derived from the report, not the code.** The full code only records effects at the rated level, so the IDRS code must be worked out from the per-dose results in the test report.
7. **Report must be available.** An IDRS code is only valid when the full IDR code and test report are published alongside it.

### Worked example (hypothetical)

| Group | Test results | Full code | IDRS digit |
|---|---|---|---|
| U | Level 2 completed, no effects | `U2` | (requirement met) |
| D | Clean at doses 1, 2 and 3 | `D3` | 3 |
| G | Dose 1 clean; dose 2 grinding; dose 3 would not close | `G2gC` | 1 |
| W | 6 m passed at 10 and 30 min, failed at 1 h, no effects | `W52` | 5 |

**Full code:** `IDR1 U2 D3 G2gC W52`
**Short code:** `IDRS 315`

The grit digit drops from 2 to 1 because the dose-2 pass came with grinding.

---

## Status

This overview defines the code format and reporting rules. Values marked [TBD] (doses, cycle counts, tolerances, drying period) will be set in the full specification, along with apparatus, test procedures and the report template.
