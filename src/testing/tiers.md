# Test Tiers

IDR has two test tiers:

- **Home:** for an individual testing one device they intend to keep.
- **Lab:** for testers who can sacrifice and tear down two or more devices.

| | Home | Lab |
|---|---|---|
| **Units** | 1 | 2 or more |
| **Device fate** | Kept: the tester intends to keep it working | Sacrificed |
| **Device condition** | Any, from new to heavily used; shall be recorded as found | Shall be spread across wear: one new, one heavily used (real or simulated), and further units filling in the levels between |
| **D and G ladder** | Stops at the first effect, or at the tester's chosen maximum level ([stop rules](../groups/particulate.md#stop-rules)) | Runs to failure or level 9 ([stop rules](../groups/particulate.md#stop-rules)) |
| **Teardown** | No | Yes, every unit |
| **Can detect enclosure breach (`E`)** | Electrical faults only | Yes |
| **Code prefix** | `IDR1*` | `IDR1` ([code format](../rating/code-format.md#home-tier-marker)) |
| **IDRS short code** | Cannot be issued | Can be issued ([IDRS](../rating/idrs.md)) |

How device condition is measured is [TBD] (see [U: Usage](../groups/usage.md)). How results from several units combine is covered in [Reporting](reporting.md#combining-multiple-units).

> **Note (informative):** Home results are useful for comparing devices and spotting weak points, but they cannot confirm sealing. This is why the `*` marks them as never equivalent to lab results.

## Home tier: recovery cleaning

After D and G testing, home-tier units shall be cleaned as follows. When this happens relative to the U, D, G, W test order is [TBD].

1. Tap out loose material on every edge.
2. Use the hand air blower **across** seams, grilles and ports, not straight into them, while operating moving parts slowly to work debris out.
3. Brush seams and ports gently with the soft brush.
4. Clean the screen with a dry lint-free cloth.
5. Do **not** use liquids or canned air.
6. **Repeat the measurements** (see [Measurements](measurements.md)) and record them.

> **Note (informative):** Canned air is high pressure and can drive debris deeper.

> **Note (informative):** An effect that remains after cleaning is likely permanent, which is useful to report.

## Lab tier: teardown

After D and G testing, every lab-tier unit shall be torn down as follows. When this happens relative to the U, D, G, W test order is [TBD].

1. Photograph every face, seam and port under UV light.
2. Tear down the unit. Inspect each sealed compartment for debris and photograph it under UV light.
3. Inspect hinge and mechanism internals for debris, scoring and damaged parts. Photograph and describe them.
4. Record any enclosure breach (`E`) with its location (see [D: Dust](../groups/dust.md#enclosure-breach-found-at-teardown)).

Recovery cleaning and teardown after W tests are [TBD].
