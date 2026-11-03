# U: Usage

## What U tests

U applies simulated wear to a unit before all other groups are tested (see the [core principle](../introduction.md#core-principle)), and records any effects the wear itself causes.

## Scale

Wear is measured in **simulated days** of use. Levels are cumulative: each level continues the wear of the level before it.

| Level | Simulated days | Approximate real use |
|---|---|---|
| U0 | 0 | New, no preconditioning |
| U1 | 90 | 3 months |
| U2 | 360 | 1 year |
| U3 | 720 | 2 years |
| U4 | 1,440 | 4 years |

## Wear actions

| Wear action | Per simulated day | U1 total | U2 total | U3 total | U4 total |
|---|---|---|---|---|---|
| Hinge or slide cycles: foldable and slider phones | 100 | 9,000 | 36,000 | 72,000 | 144,000 |
| Hinge cycles: laptops and other hinged devices | 10 | 900 | 3,600 | 7,200 | 14,400 |
| Presses of each button or key | 25 | 2,250 | 9,000 | 18,000 | 36,000 |
| Turns of each crown or dial, each way | 20 | 1,800 | 7,200 | 14,400 | 28,800 |
| Plug insertions into each port | 1 | 90 | 360 | 720 | 1,440 |
| Openings of each port cover | 1 | 90 | 360 | 720 | 1,440 |
| Ejections of each tray | 1 per 30 days | 3 | 12 | 24 | 48 |
| Drops | 1 per 60 days | 2 | 6 | 12 | 24 |

1. Totals are cumulative. Drops are rounded up to whole drops.
2. Wear actions for parts the device does not have shall be recorded as N/A.
3. For keyboards, presses apply to the fixed set of keys defined in the report (as for a [cycle](particulate.md#cycle)).

> **Note (informative):** About 100 folds a day is the usage figure foldable makers use for fold-durability claims. One plug insertion a day matches daily charging. Laptops are opened far less often than foldable phones are folded. The drop rate assumes an occasional drop rather than heavy abuse.

## Standard wear level

The **standard wear level** is **U2** (one simulated year). IDRS codes are issued only from units at or above it (see [IDRS Short Code](../rating/idrs.md#eligibility)).

## U digit by unit condition

| Unit condition | U digit |
|---|---|
| New, not preconditioned | `U0` |
| Preconditioned with simulated wear | The highest level completed (`U1`–`U4`) |
| Real wear, days since first use known | The [equivalent level](#equivalent-level-for-real-wear) |
| Real wear, days since first use unknown | `UX` |

### Equivalent level for real wear

1. The unit's **equivalent days** are its days since first use. If the device reports a battery cycle count, the equivalent days are the lower of the two.
2. The equivalent level is the highest level whose simulated days do not exceed the equivalent days.
3. The report shall state that the unit has real wear, and the basis for its equivalent days (for example, purchase date and battery cycle count).

> **Note (informative):** Taking the lower figure keeps the estimate conservative. One battery cycle is roughly one day of use. Real wear includes an unknown number of drops, so the report keeps real-wear and simulated-wear units distinct.

## Procedure

Procedure steps are written in the imperative and are requirements unless they say otherwise.

### Before testing

1. Confirm the unit meets [Test Conditions](../testing/conditions.md), including its U baseline.
2. Record the target level. Lab tier: the unit's assigned level. Home tier: the tester may choose one.

### Each level

1. **Hinges and slides:** run the level's increment of cycles through the full range, at no more than 1 cycle per second.
2. **Buttons and keys:** press each one its increment of times, fully actuating it, at no more than 2 presses per second.
3. **Crowns and dials:** turn each one its increment of full turns each way.
4. **Ports and port covers:** fully insert and remove a matching plug in each port, and open and close each port cover, for their increments.
5. **Trays:** eject and reinsert each tray for its increment.
6. **Drops:** perform the level's increment of [drops](#drops).
7. **Measure** every applicable effect (see [Measurements](../testing/measurements.md)) and record the results.
8. **Grade the level** (see [Grading](#grading)) and decide whether to continue (see [Stop rules](#stop-rules)).

Wear actions may be performed by hand or by a motorized rig. A rig should be used for hinge cycles and button presses at U2 and above. The report shall state which method was used for each action.

### Drops

1. Close hinged devices before dropping them. The unit stays powered on.
2. Release the unit from rest, with no throw, with its lowest point 1.0 m above the surface.
3. Drop onto 18 mm plywood laid flat on a concrete floor.
4. Rotate the impact orientation in this order, repeating as needed: front face, back face, top edge, bottom edge, left edge, right edge.
5. Inspect the unit after each drop. If a failure appears, stop the level.

> **Note (informative):** Plywood over concrete is the impact surface used by the MIL-STD-810H transit drop test. It is more repeatable and less destructive than bare concrete. 1.0 m is about pocket and table height.

### Stop rules

| Tier | Continue to the next level unless… |
|---|---|
| **Home** | Any effect appeared at this level, or the target level or U4 was reached |
| **Lab** | The level was failed (an uppercase effect appeared), or the target level was reached |

## Grading

1. A level is **passed** if no uppercase effect appeared during or after it. The digit is the highest level passed.
2. Effect letters record effects seen after wear. Example (hypothetical): `U2h` means hold force had changed after level-2 wear.
3. If a unit fails during preconditioning, the failure letter records why. The remaining groups shall then be tested on a fresh unit preconditioned to the last completed level.

How a lab test with several units is published is defined in [Reporting](../testing/reporting.md#combining-multiple-units).
