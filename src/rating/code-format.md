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

## Home-tier marker

1. Home-tier codes shall carry `*` immediately after the version: `IDR1*`.
2. Lab-tier codes shall carry no marker: `IDR1`.
3. A code marked `*` is never equivalent to a lab-tier code.

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
2. The failure letter names the failure at the next level above the rated level.
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

| Group | Digit | Meaning of no failure letter |
|---|---|---|
| D, G | 9 | The unit passed the whole ladder |
| D, G | Below 9 | Testing was stopped before any failure was reached. This is normal for home-tier tests |
| U, W | Any | [TBD] |
