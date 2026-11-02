# Overview

An IDR rating is written in one of two forms.

| Form | Example (hypothetical) | Used for |
|---|---|---|
| Full code (**IDR**) | `IDR1 U2 D3 G2rC W52E` | Spec sheets, reviews, test reports |
| Short code (**IDRS**) | `IDRS1 315` | Packaging and marketing |

Every IDRS code shall be derived from a full IDR test report, using the rules in [IDRS Short Code](idrs.md). While the specification is a draft, both forms use version 0 (see [Code Format](code-format.md#version-prefix)).

## Reading a full code

Hypothetical example: `IDR1 U2 D3 G2rC W52E`

| Slot | Example | Meaning |
|---|---|---|
| Prefix | `IDR1` | Ingress & Durability Rating, spec version 1, lab tier (no `*`) |
| Usage | `U2` | Tested after level-2 simulated wear, no effects |
| Dust | `D3` | Passed fine dust at level 3 (light), no ingress |
| Grit | `G2rC` | Passed grit at level 2 (trace) with rough motion; at level 3 it would not close |
| Water | `W52E` | Passed 6 m (depth tier 5) for 30 minutes (time tier 2); electrical fault at 1 h |

The grammar is defined in [Code Format](code-format.md) and the letters in [Effect Letters](effect-letters.md).

## Reading a short code

Hypothetical example: `IDRS1 315`, read "I-D-R-S one, three-one-five". It is derived from the same hypothetical test as the full code above.

| Part | Group | Meaning |
|---|---|---|
| `1` | (version) | Spec version 1 |
| `3` | Dust | Highest level passed with no effect letters other than `i`: level 3 |
| `1` | Grit | Highest level passed with no effect letters other than `i`: level 1 |
| `5` | Water | Deepest depth tier passed cleanly for 30 minutes: 6 m |

The full derivation is shown in the [worked example](idrs.md#worked-example-hypothetical).
