# Skill verification

Verified against the live library after authoring the skills.

## Research skill

- **T1 context is not attribution — PASS.** Hatikva Market remains `Perpetrator politics unclear` + `Needs more sourcing`; Channel 12 and Haaretz vandalism are likewise not upgraded from contextual evidence.
- **T2 one incident/many sources — PASS.** Current structure keeps incident IDs separate from source/media IDs.
- **T3 approximate dates — PASS.** Qusra siege retains uncertainty in canonical notes rather than presenting unsupported source precision as certainty.
- **T4 settler != far right — PASS.** Settler incidents remain `Settler movement` in the canonical Sheet and display as `By settlers` in Notion unless stronger evidence supports `Far right`.
- **T5 candidate != verified — PASS.** Weak-attribution cases use needs-more-sourcing rather than verified labels.

## Media skill

- **T1 actual previews — PASS.** All 10 Notion media records have populated `Preview` values backed by stable project-hosted JPGs.
- **T4 field separation — PASS.** Direct media/original/source/preview concepts remain separate in the schema.
- **T5 fallback order — PASS.** X cases use direct FxTwitter links where available; Ras Ein al-Auja uses the original Instagram Reel; Qusra siege falls back to the Reuters media/report page.
- **T7 schema rehydration — PASS.** After conversational taxonomy changes, all 10 records were repopulated from the canonical Sheet and re-queried.
- **T8 conversational labels — PASS.** Gallery records use values such as `By settlers`, `By far-right activists`, `Perpetrator politics unclear`, and `Against Palestinians in the West Bank` without redundant display-only badge properties.
- **T9 batch verification — PASS.** Query confirmed every current record has Card Summary, Media Type, Affiliation, Target, Violence Type, Severity, Verification, Open Media, Preview, Date and Location.

## Orchestration skill

- **Canonical-first model — PASS.** Google Sheets remains the formal source of truth; Notion is the visual/search layer; GitHub stores stable preview images.
- **Weak cases stay visible — PASS.** Ambiguous political attribution is preserved with explicit status rather than silently excluded or overstated.
- **End-to-end check — PASS.** Current 10-record seed batch has complete required visual fields after post-write query.

## Regression rule

Any future workflow/schema change that affects attribution, preview handling, field semantics, or gallery presentation should add/update a test scenario before changing the skill, then re-run the relevant checks against at least one strong-attribution case and one ambiguous-attribution case.
