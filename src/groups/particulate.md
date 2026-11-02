# D and G: Particulate Testing

This chapter defines the scale, dose, procedure and grading shared by the [D (dust)](dust.md) and [G (grit)](grit.md) groups. The two groups differ only in their test medium and full dose, which are defined in their own chapters.

## Exposure area

```
A = sum of (length × width) of the largest face of each rigid section, in cm²
```

| Device type | Rigid sections | A |
|---|---|---|
| Slab phone or tablet | 1 | Front face |
| Book-style foldable | 2 | Both halves (equals the unfolded face) |
| Flip-style foldable | 2 | Both halves |
| Laptop | 2 | Base + lid |

> **Note (informative):** Dose scales with exposure area, not mass. Particles get in through surfaces, seams and moving parts, so a dense device and a light device of the same size have the same exposure. Devices with hinges receive a larger dose automatically, in proportion to their extra surfaces and seams.

## Dose

```
Dose (g) = (A ÷ 100) × F × p
```

| Symbol | Meaning |
|---|---|
| A | Exposure area, cm² |
| F | Full dose per 100 cm², set per group: [D](dust.md#full-dose), [G](grit.md#full-dose) |
| p | Cumulative fraction of the full dose for the level (see [Scale](#scale)) |

1. Every dose shall be weighed. The weighed mass is the dose.
2. Volume measures may be used as rough guidance only (see [Volume Conversions](../appendix/volume-conversions.md)).

> **Note (informative):** Powders pack differently depending on the product and how they are scooped. One tablespoon (15 mL) of dry sand weighs roughly 23 g, but a tablespoon of fine powder can weigh anywhere from about 5 to 15 g. This is why doses are weighed rather than measured by volume.

### Example doses (informative)

| Device | A | D, lvl 1 | D, lvl 5 | D, lvl 9 | G, lvl 1 | G, lvl 5 | G, lvl 9 |
|---|---|---|---|---|---|---|---|
| Phone, 16 × 7.5 cm | 120 cm² | 0.6 g | 7.5 g | 30 g | 2.4 g | 30 g | 120 g |
| Book foldable, 16 × 12.5 cm unfolded | 200 cm² | 1.0 g | 12.5 g | 50 g | 4.0 g | 50 g | 200 g |
| Tablet, 24 × 17 cm | 408 cm² | 2.0 g | 25.5 g | 102 g | 8.2 g | 102 g | 408 g |

## Scale

Levels are **cumulative**: each level adds more medium and more cycles on top of the previous level, with no cleaning in between.

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

For each level, the dose increment shall be the difference between that level's cumulative dose and the previous level's, and the cycles run shall be the difference between their cumulative cycles.

> **Note (informative):** Cumulative levels reproduce debris building up over time.

## Cycle

One cycle means operating every moving part through its full range once, at about one cycle every 2 seconds:

| Moving part | One cycle |
|---|---|
| Hinges and slides | Fully closed to fully open and back |
| Buttons and keys | Pressed once each. For keyboards, a fixed set of keys defined in the report |
| Crowns and dials | One full turn each way |
| Port covers and trays | Opened and closed once every 10 cycles |
| Ports | A plug inserted and removed once every 10 cycles |

## Procedure

Procedure steps are written in the imperative and are requirements unless they say otherwise. Equipment is listed in [Kits](../equipment/kits.md) and safety requirements in [Safety](../testing/safety.md).

### Before testing

1. Remove cases, covers and screen protectors.
2. Record the unit's condition (age, visible wear, prior repairs). Lab units shall be preconditioned to their assigned wear levels per [U: Usage](usage.md) [TBD].
3. Record temperature and humidity.
4. Measure the exposure area and calculate the dose for every level.
5. Take [baseline measurements](../testing/measurements.md) for every applicable effect.
6. Home tier: the tester may choose a maximum level in advance.

### Each level

1. **Weigh** the dose increment for this level.
2. **Place the unit** inside the bin in its most open state (hinged devices fully open; slab devices front face up).
3. **Apply half** the increment, sprinkled evenly from about 10 cm above. The medium may be shaken through the #20 sieve to give an even spread.
4. **Brush** each seam, hinge line and port opening with 5 light strokes.
5. **Run half** the level's cycles.
6. **Turn the unit over** (hinged devices: close it). Apply the other half of the increment to the exposed faces, edges and ports, brush, and run the remaining cycles.
7. **Shed loose material:** hold the unit edge-down and tap it 3 times on each long edge onto a folded towel. Do not blow or wipe the seams at this stage.
8. **Measure** every applicable effect (see [Measurements](../testing/measurements.md)) and record the results.
9. **Grade the level** (see [Grading](#grading)) and decide whether to continue (see [Stop rules](#stop-rules)).

### Stop rules

| Tier | Continue to the next level unless… |
|---|---|
| **Home** | Any effect other than `i` appeared at this level, the chosen maximum level was reached, or level 9 was completed |
| **Lab** | The level was failed (an uppercase effect appeared), or level 9 was completed |

> **Note (informative):** Home testers stop at the first sign of degradation to give the device the best chance of surviving.

### After testing

| Tier | Requirement |
|---|---|
| Home | [Recovery cleaning](../testing/tiers.md#home-tier-recovery-cleaning) |
| Lab | [Teardown](../testing/tiers.md#lab-tier-teardown) |

## Grading

1. A level is **passed** if no uppercase effect appeared after it.
2. The **digit** is the highest level passed (0 if level 1 failed).
3. Effect letters and the failure letter shall be written per [Code Format](../rating/code-format.md#effect-letters), including the failure-letter priority order and the meaning of an absent failure letter.
4. Enclosure breaches found at teardown are handled per [D: Dust](dust.md#enclosure-breach-found-at-teardown).

### Examples (hypothetical)

| Code | Tier | Meaning |
|---|---|---|
| `D5r` | Home | Passed moderate dust; rough motion appeared at level 5, so testing stopped to protect the device |
| `G3` | Home | Passed light grit with no effects; the tester's chosen maximum was 3 |
| `D9` | Lab | Passed buried fine dust with nothing getting in |
| `D7iE` | Lab | Passed heavy fine dust with debris visible in seams but no effect; electrical fault at level 8 |
| `G6rC` | Lab | Passed moderate grit with rough motion; at level 7 the hinge would not close |
| `G3hrR` | Lab | Passed light grit with loosened hold and rough motion; at level 4 the hinge bound |
