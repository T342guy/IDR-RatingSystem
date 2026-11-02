# Effect Letters

1. Testers shall use only the letters in this list.
2. A lowercase letter means the effect was observed and is within tolerance.
3. An uppercase letter means the effect caused failure.
4. The thresholds apply to every group the letter is listed for.

How letters are placed in a code is defined in [Code Format](code-format.md). How each effect is measured is defined in [Measurements](../testing/measurements.md).

## Closed list

| Letter | Effect | Groups | Lowercase threshold (within tolerance) | Uppercase threshold (failure) |
|---|---|---|---|---|
| `b` / `B` | Buttons, keys or ports impaired | All | Stiff or gritty; plug meets resistance | Does not register; plug cannot seat |
| `c` / `C` | Closure gap | All | Increase of more than 0.3 mm over baseline | Increase of more than 1.0 mm, or will not stay closed |
| `E` | Enclosure breach (dust or liquid inside a sealed compartment) or electrical fault | D, G, W | n/a (no lowercase form) | Electrical fault (reboots, charging failure, sensor errors). A breach found at lab teardown is recorded in the report, not the code (see [attribution](../testing/tiers.md#attributing-an-enclosure-breach)) |
| `f` / `F` | Fogging or condensation inside a lens or display | W | [TBD] | [TBD] |
| `h` / `H` | Hold or closing force changed (magnets, detents, latches) | All | Change of more than 15% from baseline | Change of more than 40%, or no hold |
| `i` | Ingress only, no measurable effect | D, G, W | Medium or water visible inside an opening, below the outer surface, with no other effect | n/a (no uppercase form) |
| `m` / `M` | Audio impaired after the drying period [TBD] | W | [TBD] | [TBD] |
| `r` / `R` | Rough motion: grinding or crunching during movement | All | Grinding or crunching heard at 30 cm or felt | Moving part binds: cannot complete its full range with normal hand force |
| `s` / `S` | Screen marks, pressure points, dead pixels or touch faults | All | Marks or pressure points visible on grey at 45° | Dead pixels, lines, cracks, or touch dead zones |

> **Note (informative):** All thresholds are provisional and will be adjusted once real devices have been tested. See [Open Issues](../appendix/open-issues.md).

> **Note (informative):** Medium resting on the outer surface or in the outer lip of a seam is not ingress. Sprinkled medium always lands there, so counting it would put `i` on nearly every test.

> **Note (informative):** Rough motion uses `r` rather than `g` because an uppercase `G` would collide with the G group letter.
