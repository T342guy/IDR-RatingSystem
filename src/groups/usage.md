# U: Usage

## What U tests

U applies simulated wear to a unit before all other groups are tested (see the [core principle](../introduction.md#core-principle)).

## Scale

| Level | Meaning |
|---|---|
| U0 | Tested new, no preconditioning |
| U1 to U4 | Increasing wear: fold cycles, button presses, port insertions, drops. Cycle counts per level [TBD] |

## Standard wear level

The **standard wear level** is U2 [TBD]. IDRS codes are issued only from units at or above it (see [IDRS Short Code](../rating/idrs.md#eligibility)).

## U digit by unit condition

| Unit condition | U digit |
|---|---|
| New, not preconditioned | `U0` |
| Preconditioned with simulated wear | The highest wear level completed (`U1`–`U4`) |
| Used (real wear), not preconditioned | `UX`, with the unit's condition recorded in the report |

Real-wear units are written `UX` until a wear metric maps real wear onto U levels [TBD].

> **Note (informative):** `UX` uses the existing "not tested" marker: no preconditioning was performed, and the unit's real condition is in the report. Most home-tier units are `U0` or `UX`.

## Procedure

[TBD]. This includes how a unit's wear condition is measured, which the lab tier uses to spread units across wear (see [Test Tiers](../testing/tiers.md)).

## Grading

1. The digit is the highest wear level completed.
2. Effect letters record effects seen after wear. Example (hypothetical): `U2h` means hold force had dropped after level-2 wear.
3. If a unit fails during preconditioning, the failure letter records why. The remaining groups shall then be tested on a fresh unit preconditioned to the last completed level.

How a lab test with several units is published is defined in [Reporting](../testing/reporting.md#combining-multiple-units).
