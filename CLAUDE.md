# IDR Specification: mdBook Project

This repository holds the **IDR (Ingress & Durability Rating)** specification, published as an mdBook site. IDR is an independent, unofficial rating system for dust, grit, water and wear resistance of smartphones and other portable electronic devices.

The goal of this structure is that **every chapter is proper documentation of one subject.** Follow the writing rules below for all edits, not just the initial build.

---

## Writing rules

1. **One chapter, one subject.** A chapter defines one thing (a code group, the effect letters, the test tiers, the kits). If content belongs to another chapter's subject, link to that chapter instead of repeating it.
2. **Normative language** follows ISO/IEC Directives Part 2:
   - **shall** = requirement
   - **should** = recommendation
   - **may** = permission
   - **can** = possibility (not a rule)
3. **Rationale is informative, never mixed into requirements.** Put explanations ("why grams and not tablespoons") in a clearly marked note:
   ```
   > **Note (informative):** …
   ```
4. **Test-group chapters (U, D, G, W) contain only:** what the group tests, its scale, its procedure, and its grading. Equipment lists, shopping notes, safety warnings and media preparation belong in their own chapters and are linked.
5. **Never invent values, rules or thresholds.** If something is undefined, write `[TBD]` and add it to `appendix/open-issues.md`.
6. **Use defined terms consistently.** Every term in `rating/definitions.md` is used with exactly that meaning everywhere. New terms get added there first.
7. **Example codes are always labelled hypothetical.**
8. **Procedures are numbered steps. Definitions and scales are tables.** Avoid long prose for either.
9. **Record every substantive change** in `appendix/changelog.md`, with the spec version.

---

## Book structure

```
book.toml
src/
├── SUMMARY.md
├── introduction.md
├── rating/
│   ├── overview.md
│   ├── definitions.md
│   ├── code-format.md
│   ├── effect-letters.md
│   └── idrs.md
├── groups/
│   ├── usage.md
│   ├── particulate.md
│   ├── dust.md
│   ├── grit.md
│   └── water.md
├── testing/
│   ├── tiers.md
│   ├── conditions.md
│   ├── measurements.md
│   ├── reporting.md
│   └── safety.md
├── equipment/
│   ├── kits.md
│   └── media.md
└── appendix/
    ├── volume-conversions.md
    ├── report-template.md
    ├── open-issues.md
    └── changelog.md
```

### What each chapter defines

| File | Defines |
|---|---|
| `introduction.md` | What IDR is, why it exists, the core principle (tested as used: worn first, moving parts operating), spec status and version |
| `rating/overview.md` | The two forms (full IDR code and IDRS short code), one decoded example of each |
| `rating/definitions.md` | Terms: moving part, cycle, exposure area, level, effect, failure, tolerance, enclosure breach, unit, tier, etc. |
| `rating/code-format.md` | Code grammar, group order, version prefix, `*` home-tier marker, `X` for not tested, effect and failure letter rules, failure-letter priority order, meaning of a digit below 9 with no failure letter |
| `rating/effect-letters.md` | The closed list of effect letters, which groups each applies to, and lowercase/uppercase thresholds |
| `rating/idrs.md` | IDRS format and every derivation rule |
| `groups/usage.md` | U group: wear levels in simulated days, wear actions, drops, standard wear level, U digit by unit condition (including real wear), procedure, grading |
| `groups/particulate.md` | Shared by D and G: the 0–9 scale, dose formula, cycle definition, per-level procedure, stop rules, level grading |
| `groups/dust.md` | D group: what it tests (sealing), its medium (by link), its full dose, anything specific to D |
| `groups/grit.md` | G group: what it tests (mechanism tolerance), its medium (by link), its full dose, anything specific to G |
| `groups/water.md` | W group: water medium, depth and time tiers, ladder and stop rules, procedure, grading, water-specific effects |
| `testing/tiers.md` | Home and lab tiers: units, device fate, device condition, stop rules (by link), lab teardown, enclosure-breach attribution, verification units |
| `testing/conditions.md` | Conditions for every group: test order, unit state, per-group baselines, between-group cleaning (including home recovery cleaning) |
| `testing/measurements.md` | How each effect is measured (methods only; thresholds live in `effect-letters.md`) |
| `testing/reporting.md` | Report contents checklist; combining multiple units (per-unit codes and the headline code) |
| `testing/safety.md` | All safety requirements |
| `equipment/kits.md` | Home kit and lab kit contents |
| `equipment/media.md` | D and G test media: materials, sieve fractions, preparation, reuse |
| `appendix/volume-conversions.md` | Informative tablespoon conversions |
| `appendix/report-template.md` | Informative fill-in report template covering every required report item |
| `appendix/open-issues.md` | Every unresolved question, every `[TBD]`, and the provisional values register |
| `appendix/changelog.md` | Version history |
