# Open Issues

Every requirement in this specification now has a defined value. The issues below can only be settled by testing real devices or by the author's review.

## Questions for testing

1. **Calibration.** The doses, wear counts and thresholds are starting points. After testing a range of devices, adjust them so real devices spread across levels 1–9 and the W ladder. If almost everything scores 0 or 9, the scale is set wrong.
2. **Home vs lab equivalence.** Test the same model with both kits and compare.
3. **Cycling consistency.** Compare hand cycling with rig cycling on the same model. If results differ, consider making a rig mandatory at the lab tier.
4. **Verification leniency.** Verification units skip earlier groups (see [Test Tiers](../testing/tiers.md#verification-unit)). Check whether this changes outcomes enough to require the earlier groups too.
5. **Real-wear equivalence.** Compare real-wear units with simulated-wear units at the same U level. If they differ widely, revise the [equivalent level](../groups/usage.md#equivalent-level-for-real-wear) rule.

## For the author's review

6. **Definitions written during the restructure.** *Sealed compartment*, *rigid section* and *tolerance* were not in the source drafts. See [Definitions](../rating/definitions.md).
7. **Provisional values.** Every value in the register below was added in v0.3 or v0.4 to replace a `[TBD]`.
8. **Future water groups.** Salt and pool (chlorinated) water are planned as future groups.

## Provisional values register

| Value | Chapter | Basis |
|---|---|---|
| U levels: 90, 360, 720 and 1,440 simulated days | [U: Usage](../groups/usage.md#scale) | 3 months to 4 years of use; typical phone lifespans |
| 100 hinge cycles per day (foldable and slider phones) | [U: Usage](../groups/usage.md#wear-actions) | Usage figure foldable makers use for fold-durability claims |
| 10 hinge cycles per day (laptops and other hinged devices) | [U: Usage](../groups/usage.md#wear-actions) | Laptops are opened far less often than foldables are folded |
| 25 presses per button or key per day | [U: Usage](../groups/usage.md#wear-actions) | Estimate of daily button use |
| 20 crown or dial turns per day | [U: Usage](../groups/usage.md#wear-actions) | Estimate |
| 1 plug insertion and 1 port cover opening per day | [U: Usage](../groups/usage.md#wear-actions) | Daily charging |
| 1 tray ejection per 30 days | [U: Usage](../groups/usage.md#wear-actions) | Estimate |
| 1 drop per 60 days, from 1.0 m onto 18 mm plywood over concrete | [U: Usage](../groups/usage.md#drops) | Occasional drops; MIL-STD-810H transit drop surface |
| Rig rates: up to 1 hinge cycle per second, 2 presses per second | [U: Usage](../groups/usage.md#each-level) | Fast enough for rig use, slow enough to avoid heating the mechanism |
| Standard wear level: U2 | [U: Usage](../groups/usage.md#standard-wear-level) | Kept from the source draft's provisional value |
| Equivalent days: lower of days since first use and battery cycle count | [U: Usage](../groups/usage.md#equivalent-level-for-real-wear) | About one charge cycle per day; conservative |
| Lab minimum: one `U0` and one `U4` unit | [Test Tiers](../testing/tiers.md) | Source draft: one new, one heavily used |
| Failure priority: E, F, S, K, C, M, R, H, B | [Code Format](../rating/code-format.md#failure-letter) | Source order, with `F`, `K` and `M` placed by severity |
| New effect letter `k` (casing damage) and its thresholds | [Effect Letters](../rating/effect-letters.md) | Needed for the U drop test |
| `E` applies to all groups, including U | [Effect Letters](../rating/effect-letters.md) | Drops can cause electrical faults |
| `f`: fog that clears by the end of drying is lowercase; persistent fog or droplets is uppercase | [Effect Letters](../rating/effect-letters.md) | Condensation can form without ingress; persistent fog cannot |
| `m`: more than 6 dB below baseline is lowercase; more than 15 dB or no output is uppercase | [Effect Letters](../rating/effect-letters.md) | 6 dB is clearly audible; 15 dB is heavily muffled |
| `r`: peak sound at least 6 dB above baseline (replaces "heard") | [Effect Letters](../rating/effect-letters.md), [Measurements](../testing/measurements.md#rough-motion) | Objective version of "heard at 30 cm" |
| Audio method: 1 kHz tone, 10 cm, 5 s | [Measurements](../testing/measurements.md#audio) | Repeatable with a second phone |
| Drying period: 2 hours, upright, ports down | [W: Water](../groups/water.md#drying-period) | Long enough for surface water to clear from grilles |
| Charging: delay a further 24 hours after drying where possible | [Safety](../testing/safety.md#device) | Phone makers' advice that ports can take up to a day to dry |
| Water temperature within 5 °C of room temperature | [W: Water](../groups/water.md#medium) | IEC 60529 |
| Spray: 9–11 L/min at 30–50 cm, six orientations | [W: Water](../groups/water.md#spray-depth-tier-1) | IEC 60529 spray-nozzle test |
| Immersion: lowest point at depth, up to 10 cm deeper | [W: Water](../groups/water.md#immersion-depth-tiers-25) | Practical tolerance |
| Pressure-vessel equivalents (9.8 kPa per metre) | [W: Water](../groups/water.md#scale) | Hydrostatic pressure of fresh water |
| W cycling: 10 cycles at the start, then 10 every 10 minutes | [W: Water](../groups/water.md#cycling-schedule) | Regular operation without constant handling |
| Ports, covers and trays not operated in W | [W: Water](../groups/water.md#cycling-schedule) | Users do not open them underwater |
| Repaired-enclosure units not eligible for IDRS | [IDRS Short Code](../rating/idrs.md#eligibility) | Repairs disturb seals |
| Verification unit procedure | [Test Tiers](../testing/tiers.md#verification-unit) | Proposed fix for breach timing in the source draft |
