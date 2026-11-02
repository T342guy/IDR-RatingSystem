# Open Issues

## Design questions

1. **Timing of enclosure breaches.** Teardown shows that dust or water got into a sealed compartment, but not at which level or step. Water can also carry D medium further in. One possible fix is a separate **verification unit** taken straight to a claimed level and then torn down. See [Test Tiers](../testing/tiers.md#attributing-an-enclosure-breach).
2. **Combining multiple units.** An interim rule (per-unit codes plus a headline code) is defined in [Reporting](../testing/reporting.md#combining-multiple-units). Revisit it once [U: Usage](../groups/usage.md) defines a wear metric.
3. **Calibration.** The doses and thresholds are starting points. After testing a range of devices, adjust them so real devices spread across levels 1–9. If almost everything scores 0 or 9, the scale is set wrong.
4. **Home vs lab equivalence.** Test the same model with both kits and compare.
5. **Cycling consistency.** Hand cycling varies between testers. A motorized cycling rig with a fixed speed and range would make results more repeatable.
6. **Real-wear units.** Units with real wear are written `UX` and cannot contribute to IDRS until a wear metric maps real wear onto U levels. See [U: Usage](../groups/usage.md#u-digit-by-unit-condition).
7. **Objective rough-motion threshold.** `r` currently relies on what is heard or felt. A sound-level comparison against the baseline recording could replace it. See [Measurements](../testing/measurements.md#judgement-calls).
8. **Definitions to confirm.** The definitions of *sealed compartment*, *rigid section* and *tolerance* were written during the v0.2 restructure, not taken from the drafts, and need the author's confirmation. See [Definitions](../rating/definitions.md).
9. **Future water groups.** Salt and pool (chlorinated) water are planned as future groups.

## `[TBD]` register

| Item | Chapter |
|---|---|
| U wear cycle counts per level (U1–U4) | [U: Usage](../groups/usage.md#scale) |
| U procedure, including how wear condition is measured | [U: Usage](../groups/usage.md#procedure), [Measurements](../testing/measurements.md) |
| Standard wear level (provisionally U2) | [U: Usage](../groups/usage.md#standard-wear-level) |
| Wear metric mapping real wear onto U levels | [U: Usage](../groups/usage.md#u-digit-by-unit-condition) |
| Failure-letter priority of `F` and `M` | [Code Format](../rating/code-format.md#failure-letter) |
| Thresholds for `f` and `m` | [Effect Letters](../rating/effect-letters.md) |
| Measurement methods for `f` and `m` | [Measurements](../testing/measurements.md) |
| Objective threshold for `r` | [Measurements](../testing/measurements.md#judgement-calls) |
| Drying period (for `m` and before charging) | [W: Water](../groups/water.md), [Safety](../testing/safety.md) |
| Spray/splash method for depth tier 1 | [W: Water](../groups/water.md#each-step) |
| Number of cycles per W step | [W: Water](../groups/water.md#each-step) |
| Report contents for U; report template | [Reporting](../testing/reporting.md) |
