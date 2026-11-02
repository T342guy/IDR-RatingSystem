# Test Conditions

This chapter defines the conditions that apply to every group: test order, the unit's state, baselines, and cleaning between groups.

## Test order

1. The groups tested on a unit shall be tested in the order U, D, G, W (see the [core principle](../introduction.md#core-principle)).
2. A group that is skipped is written `X` (see [Code Format](../rating/code-format.md#untested-groups)). The remaining groups are still tested in order.
3. The report shall state which groups were skipped.

> **Note (informative):** A skipped group changes the unit's condition for the groups after it. For example (hypothetical), a unit tested `DX G5` reached G with less prior exposure than one tested `D9 G5`.

## Unit state

1. Before the first group, record the unit's condition (age, visible wear, prior repairs) and remove cases, covers and screen protectors.
2. The unit shall be powered on, with the screen on, during every exposure. The screen timeout should be set to its longest value, and auto-lock disabled where the device allows it.
3. Button presses during cycling may change the unit's state (screen off, locked, an app opened). Before each measurement, the unit shall be woken, unlocked and returned to its home screen.
4. The unit shall have enough charge to stay powered on through each group. Charging restrictions are in [Safety](safety.md).
5. Temperature and humidity shall be recorded at the start of each group.

> **Note (informative):** A powered unit shows electrical faults (`E`), touch faults (`s`) and button faults (`b`) as they happen.

## Baselines

1. Baseline measurements (see [Measurements](measurements.md)) shall be taken immediately before each group's exposure begins, after any between-group cleaning.
2. Thresholds in [Effect Letters](../rating/effect-letters.md) compare against that group's baseline.
3. The report shall also record each measurement's change from the first baseline taken on the unit.

> **Note (informative):** Per-group baselines stop damage from an earlier group being counted again in a later one. The comparison with the first baseline keeps the cumulative picture.

## Between-group cleaning

This procedure applies at both tiers after D and after G. At the home tier it also applies after the last group tested, as recovery cleaning. Drying after W is defined in [W: Water](../groups/water.md#after-testing).

1. Lab tier, after D only: photograph every face, seam and port under UV light before cleaning.
2. Tap out loose material on every edge.
3. Use the hand air blower **across** seams, grilles and ports, not straight into them, while operating moving parts slowly to work debris out.
4. Brush seams and ports gently with the soft brush.
5. Clean the screen with a dry lint-free cloth.
6. Do **not** use liquids or canned air.
7. Measure every applicable effect and record the results. Between groups, these are the next group's baseline. After the last group, they are the home tier's after-recovery measurements.

> **Note (informative):** The UV photographs keep the evidence of where traced dust reached before cleaning removes it. Canned air is high pressure and can drive debris deeper. An effect that remains after cleaning is likely permanent, which is useful to report.
