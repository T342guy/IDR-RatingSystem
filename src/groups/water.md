# W: Water

## What W tests

W tests resistance to fresh water at increasing depth and duration, with moving parts operating.

## Medium

1. W tests shall use fresh, potable tap water.
2. Distilled, deionized, salt and pool (chlorinated) water shall not be used.
3. Water temperature shall be recorded at each step.

> **Note (informative):** Distilled and deionized water conduct electricity poorly and can hide electrical faults that tap water would cause. Salt and pool water are planned as future groups.

## Scale

W is graded on two scales.

| Depth tier | Depth |
|---|---|
| 1 | Spray / splash |
| 2 | 1 m |
| 3 | 2 m |
| 4 | 4 m |
| 5 | 6 m |

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

1. Each step shall be a separate exposure.
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

1. **Expose the unit.**
   - Depth tier 1: spray or splash, by a method [TBD].
   - Depth tiers 2–5: immerse the unit with its lowest point at the tier's depth. The lab tier may instead use a pressure vessel at the hydrostatic pressure of fresh water at that depth.
2. **Cycle moving parts** during the exposure, [TBD] cycles per step (see [cycle](particulate.md#cycle)). If the unit cannot be reached (for example, in a pressure vessel), run the cycles immediately before and immediately after the exposure, and record this in the report.
3. **Hold** for the time tier's duration.
4. **Remove and dry the exterior:** shake out water and wipe with a lint-free cloth. Do not use heat or compressed air.
5. **Measure** every applicable effect (see [Measurements](../testing/measurements.md)). Measure `m` after the drying period [TBD].
6. **Grade the step** (see [Grading](#grading)) and decide whether to continue (see [Stop rules](#stop-rules)).

### After testing

| Tier | Requirement |
|---|---|
| Home | Leave the unit to dry for the drying period [TBD] before charging (see [Safety](../testing/safety.md)) |
| Lab | [Teardown](../testing/tiers.md#lab-tier-teardown) |

## Grading

1. W shall be written `W{depth}{time}`.
2. A step is **passed** if no uppercase effect appeared after it.
3. The **depth digit** is the deepest depth tier whose time tier 1 step was passed.
4. The **time digit** is the longest time tier passed at that depth tier.
5. A unit that fails the first step shall be written `W0` with its failure letter and no time digit.
6. Effect letters record the effects present after the rated step, per [Code Format](../rating/code-format.md#effect-letters).
7. The failure letter names the failure at the next step on the ladder, per [Code Format](../rating/code-format.md#failure-letter).

### Examples (hypothetical)

| Code | Meaning |
|---|---|
| `W52E` | Passed 6 m for 10 and 30 minutes; electrical fault at 1 h |
| `W22F` | Passed 1 m for 10 and 30 minutes; fogging beyond tolerance at 2 m, 10 minutes |
| `W31F` | Passed 2 m for 10 minutes; fogging beyond tolerance at 2 m, 30 minutes |

## Water-specific effects

| Letter | Effect |
|---|---|
| `f` | Fogging or condensation inside a lens or display |
| `m` | Audio impaired after the drying period [TBD] |

Thresholds for both are in [Effect Letters](../rating/effect-letters.md).
