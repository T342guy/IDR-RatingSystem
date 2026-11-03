# Changelog

## v0.4 (2026-11-02)

Replaced every remaining `[TBD]` with a defined, provisional value. Each new value and its basis is listed in the [provisional values register](open-issues.md#provisional-values-register).

### Structure

- Added the [Report Template](report-template.md) appendix.
- Open Issues now holds only questions for testing and items for the author's review, plus the provisional values register.

### Substantive changes

- **U:** defined levels in simulated days (U1 90, U2 360, U3 720, U4 1,440), wear actions and counts per level, the drop procedure, stop rules and the procedure. U2 is confirmed as the standard wear level.
- **Real wear:** units with real wear take an equivalent level from days since first use or battery cycle count, whichever is lower. `UX` is now only for units whose age is unknown.
- **Lab units:** at least one `U0` and one `U4` unit; further units should cover U1–U3.
- **Effect letters:** added `k` (casing, back glass or lens cover damage). `E` now applies to U. Defined thresholds for `f` and `m`. `r` lowercase now uses a measured sound level (at least 6 dB above baseline) instead of "heard at 30 cm".
- **Failure priority:** now E, F, S, K, C, M, R, H, B.
- **W:** defined the spray method, immersion depth tolerance, pressure-vessel equivalents, cycling schedule, the 2-hour drying period, and the 5 °C water temperature limit. Ports, covers and trays are not operated during W.
- **Measurements:** defined methods for `r` (sound level), `f`, `m` and `k`.
- **Verification units:** a lab tester may confirm an unverified result with an extra unit torn down at the claimed level. A verified result can contribute to the IDRS code.
- **IDRS:** units whose enclosure was opened for repair are not eligible.
- **Safety:** added drop, water (no diving to retrieve units), pressure-vessel and rig requirements, and the charging delay after drying.
- **Kits:** added U, W and measurement equipment.
- **Reporting:** added U items, sound levels, rig use, verification units and IDRS derivation.

## v0.3 (2026-11-01)

Resolved contradictions and gaps found in a review of v0.2.

### Structure

- Added [Test Conditions](../testing/conditions.md): test order, unit state, per-group baselines and between-group cleaning. Home recovery cleaning moved there from Test Tiers and now also applies between groups at both tiers.
- Enclosure-breach handling moved from D: Dust to [Test Tiers](../testing/tiers.md#attributing-an-enclosure-breach), because breaches can now be attributed to D, G or W.

### Substantive changes

- **Teardown** happens once, after the last group tested, so lab units can complete W. Lab units are photographed under UV after D, before cleaning.
- **Breach attribution:** breaches are attributed to D (fluorescent debris), G (coarse grains) or W (liquid, corrosion, liquid contact indicators). Attributed results are marked unverified, and those units give no IDRS digit for that group; if none remain, the digit is 0. This replaces the `[TBD]` for how the IDRS dust digit is written.
- **Lab results:** every unit's full code is published, plus a **headline code** from the least-worn eligible unit.
- **IDRS:** only units at or above the standard wear level are eligible, and rule 5 takes the lowest digit across eligible units only. This fixes the conflict with the eligibility rule. "Passed cleanly" for the water digit now means no effect letters other than `i`.
- **Versions:** draft-era codes use major version 0 (`IDR0`, `IDR0*`, `IDRS0`). The short code now carries the version (`IDRS1 315`).
- **Markup:** codes in Markdown must be in code formatting or have the `*` escaped.
- **Absent failure letter:** one rule for every group (top passed, or testing stopped first).
- **U digit:** new units are `U0`, preconditioned units take their wear level, and real-wear units are `UX`. The standard wear level is now defined in U: Usage.
- **Ingress (`i`)** now means medium or water inside an opening, below the outer surface. Medium on the outer surface no longer counts.
- **Thresholds** now apply to every group the letter is listed for, not only D and G.
- **Unit state:** units are powered on with the screen on during exposure, and are not charged during exposure or while wet.
- **Per-group baselines:** thresholds compare against a baseline taken before each group. Change from the first baseline is also reported.
- **Rack:** during D and G, the unit sits on a raised rack clear of fallen medium.
- **G medium:** home sand must be silica, checked with a vinegar carbonate check.
- **W:** defined the ladder (time tiers 1 and 2 at each depth, then 3 and 4 at the deepest), stop rules, grading, failure letter, the water type (tap; no distilled, deionized, salt or pool water), immersion depth, pressure-vessel option, cycling and drying. Depth tier 1 is not run at time tiers 3 and 4. The example code became `W52E`, because a failure at 1 h must carry a failure letter.
- **Measurements:** recordings for `b`, `r` and `s` are kept for review, with optional second-person confirmation.
- **Safety:** added UV, charging and pressure-vessel requirements.
- **Reporting:** added W items, unit state, skipped groups, judgement confirmation and teardown attribution.

## v0.2 (2026-11-01)

Restructured the specification as an mdBook, merging the Overview draft (v0.1) and the Dust and Grit test documentation (draft v0.2). Where the two conflicted, the Dust and Grit documentation was followed.

### Structure

- Split both drafts into one chapter per subject: the rating, test groups, testing, equipment and appendices.
- Added [Definitions](../rating/definitions.md).
- Moved rationale into informative notes and wrote requirements in shall/should/may form without changing their meaning.
- Collected every `[TBD]` and unresolved question in [Open Issues](open-issues.md).

### Substantive changes from v0.1

- D and G levels are now **0–9**. The v0.1 dose table (levels 0–3) was removed.
- D and G now have a defined exposure area, dose formula, cycle definition, procedure, stop rules and grading.
- The grinding letter `g` was renamed **`r`** (rough motion), to avoid uppercase `G` colliding with the G group letter.
- The G medium is now the **sieved sand blend**, replacing "ISO 12103-1 A4 plus 150–850 µm sand". The D medium gained a home-kit option (calcium carbonate).
- Added **home and lab test tiers**. Home-tier codes use the **`IDR1*`** prefix.
- Effect letters: merged into one closed list with provisional thresholds for D and G. The failure-letter priority order (E, S, C, R, H, B) was added.
- A digit below 9 with no failure letter (D and G) now means testing was stopped before failure, replacing "failure letter omitted only if the top level was passed".
- IDRS is now **lab tier only**. For multiple units, the lowest digit is used until the U chapter defines otherwise.
- The example code was updated to `IDR1 U2 D3 G2rC W52`; its D and G meanings were reinterpreted on the 0–9 scale.
- Added the safety requirements, kits, test media and report checklist.

## v0.1

Initial Overview draft: code format, U and W groups, D and G on a 0–3 dose scale, effect letters and the IDRS short code.
