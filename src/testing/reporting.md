# Reporting

## Report contents

A test report shall contain the items below for every group tested. A fill-in [report template](../appendix/report-template.md) is provided.

### All groups

| Item | Tier |
|---|---|
| Tier (home or lab) and spec version | Both |
| Device model, firmware version, number of units, serial numbers | Both |
| Condition, prior repairs and U digit of each unit (see [U: Usage](../groups/usage.md#u-digit-by-unit-condition)) | Both |
| Unit state during exposure: power, screen timeout, auto-lock (see [Test Conditions](conditions.md#unit-state)) | Both |
| Groups skipped | Both |
| Temperature and humidity at the start of each group | Both |
| Baseline and per-level or per-step measurements for every applicable effect, and each measurement's change from the first baseline | Both |
| Ambient and measured sound levels for `r` and `m` | Both |
| Photos, audio and video for every level or step | Both |
| Whether judgement calls were confirmed by a second person (see [Measurements](measurements.md#judgement-calls)) | Both |
| Whether cycling and wear actions were done by hand or by rig | Both |
| Between-group cleaning records | Both |
| Chosen maximum levels or tiers, why testing stopped, and measurements after recovery cleaning | Home |
| UV photographs taken after D; teardown findings, liquid contact indicator states, breach attributions and photos for every unit | Lab |
| Verification units: model, U level, group, claimed level and teardown result | Lab |
| Full code for each unit | Both |
| Headline code and IDRS code, with the derivation of each IDRS digit | Lab |

### U

| Item | Tier |
|---|---|
| Target level and level reached | Both |
| Wear actions performed at each level, with counts, and any recorded as N/A | Both |
| Drop orientations, and any damage after each drop | Both |
| For real-wear units: days since first use, battery cycle count, and the resulting equivalent level | Both |

### D and G

| Item | Tier |
|---|---|
| Kit and media used: sources, sieve fractions, carbonate check, tracer | Both |
| Exposure area and calculated doses | Both |

### W

| Item | Tier |
|---|---|
| Water source, and water and room temperature at each step | Both |
| Spray flow rate and distance (depth tier 1) | Both |
| Immersion method (open water, tank or pressure vessel) and measured depth or pressure | Both |
| Depth tier, time tier and result of every step | Both |
| How moving parts were cycled (during exposure, or before and after) | Both |
| Fogging observations immediately after each step and at the end of the drying period | Both |

An IDRS code is valid only when the report is published alongside it (see [IDRS Short Code](../rating/idrs.md#eligibility)).

## Combining multiple units

1. A lab report shall publish each unit's full code alongside its wear condition.
2. The **headline code** is the full code of the eligible unit (see [IDRS Short Code](../rating/idrs.md#eligibility)) with the lowest wear level.
3. If several eligible units share that wear level, the headline code is the one with the lowest digits, compared in the order D, G, W.
4. If no unit is eligible, no headline code is published. Each unit's full code is still published.
5. The IDRS code is derived from all eligible units per [IDRS Short Code](../rating/idrs.md#derivation-rules).

> **Note (informative):** The headline code represents a unit in standard condition. The IDRS code takes the lowest digit across all eligible units, so it never claims more than the most worn eligible unit achieved.
