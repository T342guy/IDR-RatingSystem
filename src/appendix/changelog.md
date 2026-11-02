# Changelog

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
