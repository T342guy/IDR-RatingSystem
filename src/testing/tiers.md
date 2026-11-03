# Test Tiers

IDR has two test tiers:

- **Home:** for an individual testing one device they intend to keep.
- **Lab:** for testers who can sacrifice and tear down two or more devices.

| | Home | Lab |
|---|---|---|
| **Units** | 1 | 2 or more |
| **Device fate** | Kept: the tester intends to keep it working | Sacrificed |
| **Device condition** | Any, from new to heavily used; shall be recorded as found | Shall be spread across wear: at least one `U0` unit and one `U4` unit (simulated, or real wear at an equivalent level of U4). Further units should fill U1–U3, preferably including U2 |
| **U digit** | Per [unit condition](../groups/usage.md#u-digit-by-unit-condition) | Per [unit condition](../groups/usage.md#u-digit-by-unit-condition) |
| **Ladders** | Stop at the first effect, or at the tester's chosen maximum ([D and G](../groups/particulate.md#stop-rules), [W](../groups/water.md#stop-rules)) | Run to failure or the top ([D and G](../groups/particulate.md#stop-rules), [W](../groups/water.md#stop-rules)) |
| **Cleaning** | [Between groups and after the last group](conditions.md#between-group-cleaning) | [Between groups](conditions.md#between-group-cleaning) |
| **Teardown** | No | Yes, every unit, after the last group tested |
| **Can detect enclosure breach (`E`)** | Electrical faults only | Yes |
| **Code prefix** | `IDR1*` (see [code format](../rating/code-format.md#home-tier-marker)) | `IDR1` |
| **Published codes** | One full code | One full code per unit, plus a [headline code](reporting.md#combining-multiple-units) |
| **IDRS short code** | Cannot be issued | Can be issued ([IDRS](../rating/idrs.md)) |

> **Note (informative):** Home results are useful for comparing devices and spotting weak points, but they cannot confirm sealing. This is why the `*` marks them as never equivalent to lab results.

## Lab tier: teardown

After the last group tested, every lab-tier unit shall be torn down as follows.

1. Tear down the unit. Inspect each sealed compartment for debris and liquid, and photograph it under UV light.
2. Record the state of every liquid contact indicator the device has.
3. Inspect hinge and mechanism internals for debris, scoring and damaged parts. Photograph and describe them.
4. Record any enclosure breach with its location, and attribute it (see below).

The exterior UV photographs taken after D (see [Between-group cleaning](conditions.md#between-group-cleaning)) form part of the teardown record.

## Attributing an enclosure breach

| Evidence inside a sealed compartment | Attributed to |
|---|---|
| UV-fluorescent debris (traced D medium) | D |
| Non-fluorescent sand grains in the G medium's size range | G |
| Liquid, water marks, corrosion, or a tripped liquid contact indicator | W |

1. Every group whose evidence is found shall be attributed.
2. If the evidence does not identify a group, every group tested on that unit shall be attributed.
3. Each attributed group's result for that unit shall be marked unverified in the report. The code digit stands as tested.
4. No IDRS digit for an attributed group shall be taken from that unit, unless the result is confirmed by a [verification unit](#verification-unit) (see [IDRS Short Code](../rating/idrs.md#derivation-rules)).

> **Note (informative):** A teardown cannot show at which level or step a breach happened, which is why the result is marked unverified rather than regraded. Water can also carry D medium further into the device, so a D breach found after W may have been helped by the water.

## Verification unit

A lab tester may add a verification unit to confirm a result marked unverified.

1. Use a unit of the same model, at the same U level as the unit whose result is to be verified.
2. Take it through the attributed group's ladder only, from the first level or step up to the claimed rated level or step, following that group's procedure.
3. Tear it down immediately, following [Lab tier: teardown](#lab-tier-teardown).
4. If no breach is attributed to that group, the claimed result is **verified** for that wear level. The report shall record this, and the original unit's digit for that group may then contribute to the IDRS code.
5. If a breach is attributed to that group, the claimed result stays unverified. The tester may verify a lower level with another verification unit.
6. A verification unit's own codes are not published as unit results.

> **Note (informative):** The verification unit skips the groups before the attributed one, so it receives less total exposure than the original unit. This makes verification slightly lenient, which is accepted in exchange for knowing whether the claimed level itself is sealed.
