# IDRS Short Code

## Format

```
IDRS{version} {dust}{grit}{water}
```

1. The short code shall be `IDRS`, the major spec version (as in the [full code](code-format.md#version-prefix)), a space, then three digits in the fixed order dust, grit, water.
2. A group that was not tested shall be shown as `X`.

| Example (hypothetical) | Read as |
|---|---|
| `IDRS1 315` | "I-D-R-S one, three-one-five" |
| `IDRS1 3X5` | Grit not tested |

While this specification is a draft, short codes use version 0 (`IDRS0`).

## Eligibility

1. An IDRS code shall be issued only from a lab-tier test. Home-tier tests cannot produce one (see [Test Tiers](../testing/tiers.md)).
2. An IDRS code shall be derived only from units at or above the [standard wear level](../groups/usage.md#standard-wear-level) whose enclosure has never been opened for repair. These are the **eligible units**. Units written `UX` are not eligible.
3. If no unit is eligible, no IDRS code shall be issued. The full codes can still be published.
4. An IDRS code is valid only when the full IDR codes and the test report are published alongside it.

## Derivation rules

1. **Never better than the full result.** When a rule is unclear, round down.
2. **Derived from the report, not the code.** Each digit shall be worked out from the per-level and per-step results in the test report.
3. **Dust and grit digits:** the highest level passed with no effect letters other than `i`.
4. **Water digit:** the deepest depth tier whose time tier 2 step was passed with no effect letters other than `i`. If there is none, the digit is 0.
5. **Multiple units:** the lowest digit across all eligible units shall be used.
6. **Enclosure breach found at teardown:** a unit shall not contribute a digit for a group its breach is [attributed](../testing/tiers.md#attributing-an-enclosure-breach) to, unless a [verification unit](../testing/tiers.md#verification-unit) has verified that result. If no eligible unit remains for that group, its digit is 0.

> **Note (informative):** Rule 2 exists because the full code only records effects at the rated level. Effects at lower levels, which decide the IDRS digit, appear only in the report.

> **Note (informative):** Repairs that open the enclosure replace or disturb seals, so a repaired unit no longer represents the model as sold.

## Worked example (hypothetical)

One unit is shown. It was preconditioned to U2, assumed here to be the standard wear level.

| Group | Test results | Full code | IDRS digit |
|---|---|---|---|
| U | Level 2 completed, no effects | `U2` | (eligible) |
| D | Clean at levels 1, 2 and 3 | `D3` | 3 |
| G | Level 1 clean; level 2 rough motion; level 3 would not close | `G2rC` | 1 |
| W | 6 m passed cleanly at 10 and 30 min; electrical fault at 1 h | `W52E` | 5 |

**Full code:** `IDR1 U2 D3 G2rC W52E`
**Short code:** `IDRS1 315`

> **Note (informative):** The grit digit drops from 2 to 1 because the level-2 pass came with rough motion (`r`).
