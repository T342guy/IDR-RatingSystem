# W: Water

## What W tests

W tests resistance to fresh water at increasing depth and duration, with moving parts operating.

## Medium

1. W tests shall use fresh, potable tap water.
2. Distilled, deionized, salt and pool (chlorinated) water shall not be used.
3. At the start of each step, the water temperature shall be within 5 °C of room temperature. Water and room temperature shall be recorded at each step.

> **Note (informative):** Distilled and deionized water conduct electricity poorly and can hide electrical faults that tap water would cause. The 5 °C limit follows IEC 60529: a large temperature difference makes air inside the device expand or contract, which pushes or draws water through seals independently of the depth. Salt and pool water are planned as future groups.

## Scale

W is graded on two scales.

| Depth tier | Depth | Equivalent gauge pressure (pressure vessel) |
|---|---|---|
| 1 | Spray / splash | n/a |
| 2 | 1 m | 9.8 kPa |
| 3 | 2 m | 19.6 kPa |
| 4 | 4 m | 39.2 kPa |
| 5 | 6 m | 58.9 kPa |

| Time tier | Duration |
|---|---|
| 1 | 10 min |
| 2 | 30 min |
| 3 | 1 h |
| 4 | 4 h |

## Ladder

A **step** is one exposure at one depth tier for one time tier. Steps run in this order:

| Order | Depth tier | Time tiers, in order |
|---|---|---|
| 1 | 1 | 1, 2 |
| 2 | 2 | 1, 2 |
| 3 | 3 | 1, 2 |
| 4 | 4 | 1, 2 |
| 5 | 5 | 1, 2 |
| 6 | The deepest depth tier tested | 3, 4 |

1. Each step shall be a separate exposure, followed by the drying period.
2. Time tiers 3 and 4 shall be run only at the deepest depth tier tested, and never at depth tier 1.

> **Note (informative):** Steps are cumulative, like D and G levels: each exposure adds to the ones before it. Running time tier 2 at every depth lets the IDRS water digit be derived from the report.

### Stop rules

| Tier | Continue to the next step unless… |
|---|---|
| **Home** | Any effect other than `i` appeared at this step, the chosen maximum was reached, or the last step was completed |
| **Lab** | The step was failed (an uppercase effect appeared), or the last step was completed |

## Procedure

Procedure steps are written in the imperative and are requirements unless they say otherwise.

### Before testing

1. Confirm the unit meets [Test Conditions](../testing/conditions.md), including its W baseline.
2. Home tier: the tester may choose a maximum depth tier and a maximum time tier in advance. Only depth tiers the tester can physically perform may be claimed.

### Each step

1. **Expose the unit** by [spray](#spray-depth-tier-1) (depth tier 1) or [immersion](#immersion-depth-tiers-25) (depth tiers 2–5).
2. **Cycle moving parts** per the [cycling schedule](#cycling-schedule).
3. **Hold** for the time tier's duration.
4. **Remove and dry the exterior:** shake out water and wipe with a lint-free cloth. Do not use heat or compressed air.
5. **Inspect for fogging** (`f`) immediately (see [Measurements](../testing/measurements.md)).
6. **Wait out the [drying period](#drying-period).**
7. **Measure** every applicable effect, including `f` again and `m`, and record the results.
8. **Grade the step** (see [Grading](#grading)) and decide whether to continue (see [Stop rules](#stop-rules)).

### Spray (depth tier 1)

1. Use a handheld shower head or spray nozzle delivering 9–11 L/min. Measure the flow by timing how long it takes to fill a container of known volume.
2. Place the unit on the rack, or hold it, in its most open state.
3. Hold the nozzle 30–50 cm from the unit.
4. Spray each of six orientations (front face, back face, top, bottom, left and right edges) for an equal share of the time tier's duration.

> **Note (informative):** The flow rate and distance follow the IEC 60529 spray-nozzle test (10 L/min at 300–500 mm), adapted to equipment a home tester has.

### Immersion (depth tiers 2–5)

1. Hold the unit horizontal, front face up (hinged devices in their most open state), with its lowest point at least at the tier's depth and no more than 10 cm below it.
2. In open water or a pool, lower and retrieve the unit on a line (see [Safety](../testing/safety.md#water)).
3. The lab tier may instead use a pressure vessel at the gauge pressure in the [scale table](#scale), held for the time tier's duration.

### Cycling schedule

Run 10 cycles at the start of each step, then 10 more at the end of every 10 minutes.

| Time tier | Cycles per step |
|---|---|
| 1 (10 min) | 20 |
| 2 (30 min) | 40 |
| 3 (1 h) | 70 |
| 4 (4 h) | 250 |

1. In W, a cycle covers hinges, slides, buttons, keys, crowns and dials (see [cycle](particulate.md#cycle)). Ports are not plugged, and port covers and trays stay closed throughout.
2. If the unit cannot be reached (for example, in a pressure vessel), run half the step's cycles immediately before the exposure and half immediately after, and record this in the report.

> **Note (informative):** Users press buttons and fold devices around water, but do not open port covers or plug in cables underwater.

### Drying period

The **drying period** is **2 hours**.

1. Stand the unit upright on an edge, ports facing down, on a dry cloth at room temperature.
2. Do not use heat, compressed air, rice or desiccant.
3. The unit stays powered on, unless it has shut itself down.

### After testing

| Tier | Requirement |
|---|---|
| Home | Charging restrictions apply (see [Safety](../testing/safety.md#device)) |
| Lab | [Teardown](../testing/tiers.md#lab-tier-teardown) |

## Grading

1. W shall be written `W{depth}{time}`.
2. A step is **passed** if no uppercase effect appeared after it, up to the end of its drying period.
3. The **depth digit** is the deepest depth tier whose time tier 1 step was passed.
4. The **time digit** is the longest time tier passed at that depth tier.
5. A unit that fails the first step shall be written `W0` with its failure letter and no time digit.
6. Effect letters record the effects present after the rated step, per [Code Format](../rating/code-format.md#effect-letters).
7. The failure letter names the failure at the next step on the ladder, per [Code Format](../rating/code-format.md#failure-letter).

### Examples (hypothetical)

| Code | Meaning |
|---|---|
| `W52E` | Passed 6 m for 10 and 30 minutes; electrical fault at 1 h |
| `W22F` | Passed 1 m for 10 and 30 minutes; fogging that had not cleared after drying at 2 m, 10 minutes |
| `W31mM` | Passed 2 m for 10 minutes with slightly reduced audio; audio failed at 2 m, 30 minutes |

## Water-specific effects

| Letter | Effect |
|---|---|
| `f` | Fogging or condensation inside a lens or display |
| `m` | Audio impaired after the drying period |

Thresholds for both are in [Effect Letters](../rating/effect-letters.md).
