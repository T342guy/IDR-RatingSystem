# IDRS Short Code

## Format

```
IDRS {dust}{grit}{water}
```

1. The short code shall be `IDRS`, a space, then three digits in the fixed order dust, grit, water.
2. A group that was not tested shall be shown as `X`.

| Example (hypothetical) | Read as |
|---|---|
| `IDRS 315` | "I-D-R-S three-one-five" |
| `IDRS 3X5` | Grit not tested |

## Eligibility

1. An IDRS code shall be issued only from a lab-tier test. Home-tier tests cannot produce one (see [Test Tiers](../testing/tiers.md)).
2. An IDRS code shall be issued only from a test at the standard wear level (U2 [TBD]) or higher. Tests at lower wear levels can produce a full code but not an IDRS code.
3. An IDRS code is valid only when the full IDR code and the test report are published alongside it.

## Derivation rules

1. **Never better than the full result.** When a rule is unclear, round down.
2. **Derived from the report, not the code.** Each digit shall be worked out from the per-level results in the test report.
3. **Dust and grit digits:** the highest level passed with no effect letters other than `i`.
4. **Water digit:** the deepest depth tier passed cleanly for at least time tier 2 (30 minutes).
5. **Multiple units:** the lowest digit across all units shall be used, until [U: Usage](../groups/usage.md) defines otherwise.
6. **Enclosure breach found at teardown:** no IDRS dust digit shall be issued from that unit (see [D: Dust](../groups/dust.md#enclosure-breach-found-at-teardown)). How the dust digit is then written is [TBD].

> **Note (informative):** Rule 2 exists because the full code only records effects at the rated level. Effects at lower levels, which decide the IDRS digit, appear only in the report.

## Worked example (hypothetical)

Results shown for one unit.

| Group | Test results | Full code | IDRS digit |
|---|---|---|---|
| U | Level 2 completed, no effects | `U2` | (wear requirement met, if the standard level is U2) |
| D | Clean at levels 1, 2 and 3 | `D3` | 3 |
| G | Level 1 clean; level 2 rough motion; level 3 would not close | `G2rC` | 1 |
| W | 6 m passed at 10 and 30 min, failed at 1 h, no effects | `W52` | 5 |

**Full code:** `IDR1 U2 D3 G2rC W52`
**Short code:** `IDRS 315`

> **Note (informative):** The grit digit drops from 2 to 1 because the level-2 pass came with rough motion (`r`).
