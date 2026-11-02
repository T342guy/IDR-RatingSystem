# Code Format

This chapter defines the grammar of the full IDR code. The short code is defined in [IDRS Short Code](idrs.md).

## Grammar

```
IDR{version}{tier marker} U… D… G… W…
```

Each group segment is written as:

**group letter + level digit(s) + effect letters (lowercase, optional) + failure letter (uppercase, optional)**

## Version prefix

1. The code shall begin with `IDR` followed immediately by the major spec version, with no space (`IDR1`).
2. Codes from different major versions are not comparable.
3. While this specification is a draft (version 0.x), codes shall use major version 0: `IDR0` and `IDR0*`.

> **Note (informative):** Examples in this specification use `IDR1` to show the format codes will take under version 1. Draft-era `IDR0` codes are not comparable with version 1 codes.

## Home-tier marker

1. Home-tier codes shall carry `*` immediately after the version: `IDR1*`.
2. Lab-tier codes shall carry no marker: `IDR1`.
3. A code marked `*` is never equivalent to a lab-tier code.
4. In Markdown and similar markup, a code shall be written in code formatting (`` `IDR1* …` ``) or with the `*` escaped (`IDR1\*`), so that it is not read as emphasis.

The tiers are defined in [Test Tiers](../testing/tiers.md).

## Groups

1. A full code shall contain all four groups, in the order U, D, G, W.
2. Groups shall be separated by single spaces.

| Group | Level digits | Scale |
|---|---|---|
| U | One | [U: Usage](../groups/usage.md) |
| D | One, 0–9 | [D and G: Particulate Testing](../groups/particulate.md#scale) |
| G | One, 0–9 | [D and G: Particulate Testing](../groups/particulate.md#scale) |
| W | Two (depth, time), or one for `W0` | [W: Water](../groups/water.md) |

## Untested groups

1. `X` shall replace the level digit(s) of a group that was not tested (`GX`).
2. An untested group shall carry no letters.

## Effect letters

1. Effect letters shall be lowercase and taken only from the closed list in [Effect Letters](effect-letters.md).
2. Every effect present at the rated level shall be recorded, in alphabetical order.
3. `i` shall be used only when no other effect is present.
4. A group with no effect letters had no ingress and no effect at the rated level.

## Failure letter

1. At most one failure letter shall be written, after the effect letters.
2. The failure letter names the failure at the next level above the rated level (for W, the next step on the [W ladder](../groups/water.md#ladder)).
3. If several failures appear at once, the most severe shall be used, in this priority order:

| Priority | Letter |
|---|---|
| 1 (most severe) | `E` |
| 2 | `S` |
| 3 | `C` |
| 4 | `R` |
| 5 | `H` |
| 6 (least severe) | `B` |

The priority of the water letters `F` and `M` is [TBD].

## Absent failure letter

No failure letter means no failure was reached: either the top of the scale was passed, or testing stopped first. Stopping first is normal for home-tier tests.

| Group | Top of the scale |
|---|---|
| U | U4 |
| D, G | Level 9 |
| W | The last step of the [W ladder](../groups/water.md#ladder) |
