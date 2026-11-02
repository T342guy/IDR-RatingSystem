# Open Issues

## Design questions

1. **Timing of enclosure breaches.** Teardown shows that dust got into a sealed compartment, but not at which level. One possible fix is a separate **verification unit** taken straight to a claimed level and then torn down. See [D: Dust](../groups/dust.md#enclosure-breach-found-at-teardown).
2. **Combining multiple units.** To be defined alongside the wear metric in [U: Usage](../groups/usage.md). Interim rule: [Reporting](../testing/reporting.md#combining-multiple-units).
3. **Calibration.** The doses and thresholds are starting points. After testing a range of devices, adjust them so real devices spread across levels 1–9. If almost everything scores 0 or 9, the scale is set wrong.
4. **Home vs lab equivalence.** Test the same model with both kits and compare.
5. **Cycling consistency.** Hand cycling varies between testers. A motorized cycling rig with a fixed speed and range would make results more repeatable.
6. **Recovery and teardown timing.** The D and G draft places home recovery cleaning and lab teardown "after testing", but the [core principle](../introduction.md#core-principle) tests U, D, G and W in sequence on the same unit. When cleaning and teardown happen in that sequence needs defining. See [Test Tiers](../testing/tiers.md).
7. **W failure letters.** The source worked example `W52` failed at 1 h but carries no failure letter, while a unit failing depth tier 1 is written `W0` with a failure letter. When a failure letter is written above `W0` needs defining. See [W: Water](../groups/water.md#grading).
8. **Absent failure letter for U and W.** The rule for D and G (digit below 9 with no failure letter means testing stopped) has no counterpart for U and W. The source example `U2` carries no failure letter. See [Code Format](../rating/code-format.md#absent-failure-letter).
9. **U level for home-tier units.** Home units are tested in any condition, recorded as found, and are not preconditioned. Which U digit they receive is undefined.
10. **Future water groups.** Salt and chlorinated water are planned as future groups.

## `[TBD]` register

| Item | Chapter |
|---|---|
| U wear cycle counts per level (U1–U4) | [U: Usage](../groups/usage.md#scale) |
| U procedure, including how wear condition is measured | [U: Usage](../groups/usage.md#procedure), [Measurements](../testing/measurements.md) |
| Lab-unit preconditioning to assigned wear levels | [D and G: Particulate Testing](../groups/particulate.md#before-testing) |
| Standard wear level for IDRS (provisionally U2) | [IDRS Short Code](../rating/idrs.md#eligibility) |
| How the IDRS dust digit is written when teardown found an enclosure breach | [IDRS Short Code](../rating/idrs.md#derivation-rules) |
| Definition of "passed cleanly" for the IDRS water digit | [IDRS Short Code](../rating/idrs.md#derivation-rules) |
| How results from several units combine into one code | [Reporting](../testing/reporting.md#combining-multiple-units) |
| Failure-letter priority of `F` and `M` | [Code Format](../rating/code-format.md#failure-letter) |
| Meaning of an absent failure letter for U and W | [Code Format](../rating/code-format.md#absent-failure-letter) |
| Thresholds for `f` and `m` | [Effect Letters](../rating/effect-letters.md) |
| Application of the D and G thresholds to U and W | [Effect Letters](../rating/effect-letters.md) |
| Drying period for `m` | [Effect Letters](../rating/effect-letters.md), [W: Water](../groups/water.md) |
| Measurement methods for `f` and `m` | [Measurements](../testing/measurements.md) |
| W procedure, including the spray/splash method and operating moving parts | [W: Water](../groups/water.md#procedure) |
| W failure letters above `W0` | [W: Water](../groups/water.md#grading) |
| Recovery cleaning and teardown after W tests | [Test Tiers](../testing/tiers.md) |
| Timing of recovery cleaning and teardown within the U, D, G, W order | [Test Tiers](../testing/tiers.md) |
| Report contents for U and W; report template | [Reporting](../testing/reporting.md) |
