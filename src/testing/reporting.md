# Reporting

## Report contents

A test report shall contain the items below for every group tested.

### All groups

| Item | Tier |
|---|---|
| Tier (home or lab) | Both |
| Device model, firmware version, number of units, serial numbers | Both |
| Condition and U digit of each unit (see [U: Usage](../groups/usage.md#u-digit-by-unit-condition)) | Both |
| Unit state during exposure: power, screen timeout, auto-lock (see [Test Conditions](conditions.md#unit-state)) | Both |
| Groups skipped | Both |
| Temperature and humidity at the start of each group | Both |
| Baseline and per-level or per-step measurements for every applicable effect, and each measurement's change from the first baseline | Both |
| Photos, audio and video for every level or step | Both |
| Whether judgement calls were confirmed by a second person (see [Measurements](measurements.md#judgement-calls)) | Both |
| Between-group cleaning records | Both |
| Chosen maximum levels or tiers, why testing stopped, and measurements after recovery cleaning | Home |
| UV photographs taken after D; teardown findings, liquid contact indicator states, breach attributions and photos for every unit | Lab |
| Full code for each unit | Both |
| Headline code and IDRS code | Lab |

### D and G

| Item | Tier |
|---|---|
| Kit and media used: sources, sieve fractions, carbonate check, tracer | Both |
| Exposure area and calculated doses | Both |

### W

| Item | Tier |
|---|---|
| Water source and temperature | Both |
| Spray method (depth tier 1); immersion method (open water, tank or pressure vessel) and measured depth | Both |
| Depth tier, time tier and result of every step | Both |
| How moving parts were cycled (during exposure, or before and after) | Both |
| Drying period used before measuring `m` | Both |

### U

Report contents for U are [TBD], pending the U procedure. A report template is also [TBD].

An IDRS code is valid only when the report is published alongside it (see [IDRS Short Code](../rating/idrs.md#eligibility)).

## Combining multiple units

1. A lab report shall publish each unit's full code alongside its wear condition.
2. The **headline code** is the full code of the eligible unit (see [IDRS Short Code](../rating/idrs.md#eligibility)) with the lowest wear level.
3. If several eligible units share that wear level, the headline code is the one with the lowest digits, compared in the order D, G, W.
4. If no unit is eligible, no headline code is published. Each unit's full code is still published.
5. The IDRS code is derived from all eligible units per [IDRS Short Code](../rating/idrs.md#derivation-rules).

> **Note (informative):** The headline code represents a unit in standard condition. The IDRS code takes the lowest digit across all eligible units, so it never claims more than the most worn eligible unit achieved. This rule may be revisited once the U chapter defines a wear metric.
