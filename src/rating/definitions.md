# Definitions

Every term below is used with exactly this meaning throughout the specification.

| Term | Definition |
|---|---|
| **Baseline measurement** | A measurement of an effect taken immediately before a group's exposure begins, against which that group's later measurements are compared. See [Test Conditions](../testing/conditions.md#baselines) |
| **Cycle** | One operation of every moving part through its full range. Rate and per-part rules: [D and G: Particulate Testing](../groups/particulate.md#cycle) |
| **Depth tier** | One step of the W depth scale. See [W: Water](../groups/water.md#scale) |
| **Dose** | The mass of test medium, in grams, applied to a unit. Calculated per [D and G: Particulate Testing](../groups/particulate.md#dose) |
| **Effect** | A change in a unit observed during or after testing, recorded with an effect letter |
| **Effect letter** | A letter from the closed list in [Effect Letters](effect-letters.md). Lowercase means the effect is within tolerance; uppercase means it is a failure |
| **Drying period** | The fixed wait after each W step before final measurements. See [W: Water](../groups/water.md#drying-period) |
| **Eligible unit** | A lab-tier unit at or above the standard wear level, never opened for repair, from which IDRS digits can be derived. See [IDRS Short Code](idrs.md#eligibility) |
| **Equivalent level** | The U level assigned to a unit with real wear, from its equivalent days. See [U: Usage](../groups/usage.md#equivalent-level-for-real-wear) |
| **Enclosure breach** | Dust or liquid inside a sealed compartment |
| **Exposure area** (*A*) | The sum of length × width of the largest face of each rigid section of a device, in cm² |
| **Failure** | An effect that meets its uppercase threshold. A level or step at which a failure appears is failed |
| **Failure letter** | The uppercase effect letter naming the failure at the level or step above the rated level |
| **Full code** | The complete IDR code covering all four groups, e.g. `IDR1 U2 D3 G2rC W52E` (hypothetical). Grammar: [Code Format](code-format.md) |
| **Full dose** (*F*) | The dose per 100 cm² of exposure area at level 9 (100% cumulative dose). Set separately for [D](../groups/dust.md) and [G](../groups/grit.md) |
| **Group** | One of the four test categories, U (usage), D (dust), G (grit) and W (water), each written as one segment of the full code |
| **Headline code** | The single full code published for a lab-tier test. See [Reporting](../testing/reporting.md#combining-multiple-units) |
| **Ingress** | Test medium or water visible inside a unit's openings (ports, grilles, holes, button gaps, display or hinge gaps), below the outer surface. Medium resting on the outer surface is not ingress |
| **Ladder** | The ordered sequence of levels (U, D, G) or steps (W) that a unit is taken through |
| **Level** | One step on a group's scale: 0–9 for D and G, U0–U4 for U. W is graded by depth tier and time tier |
| **Medium** (test medium) | The particulate material applied in a D or G test. See [Test Media](../equipment/media.md) |
| **Moving part** | Any part that moves in normal use: hinges, slides, buttons and keys, ports and port covers, trays, and rotating crowns or dials |
| **Rated level** | The level reported by a group's digit(s): the highest level passed, or for W the rated depth and time tiers |
| **Rigid section** | A part of a device's body that does not fold or slide relative to itself. A slab phone has one; a foldable or laptop has two |
| **Sealed compartment** | An interior part of a device that its seals are intended to keep dust and liquid out of |
| **Short code** | The IDRS code, e.g. `IDRS1 315` (hypothetical). See [IDRS Short Code](idrs.md) |
| **Simulated day** | The unit of U wear: one day's worth of the wear actions in [U: Usage](../groups/usage.md#wear-actions) |
| **Standard wear level** | The minimum wear level an IDRS code is issued from: U2. See [U: Usage](../groups/usage.md#standard-wear-level) |
| **Step** (W) | One exposure at one depth tier for one time tier. See [W: Water](../groups/water.md#ladder) |
| **Test tier** (tier) | The class of test, home or lab. "Tier" used alone always means test tier. See [Test Tiers](../testing/tiers.md) |
| **Time tier** | One step of the W duration scale. See [W: Water](../groups/water.md#scale) |
| **Tolerance** | The range in which an effect is recorded in lowercase: from its lowercase threshold up to, but not including, its uppercase threshold |
| **Unit** | One physical device under test |
| **Verification unit** | An extra lab unit taken through one group up to a claimed level, then torn down, to confirm a result marked unverified. See [Test Tiers](../testing/tiers.md#verification-unit) |
