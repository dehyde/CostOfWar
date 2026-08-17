# Baseline tests — expanding-political-violence-library

## T1 — Canonical-first writes
Scenario: a batch of new incidents has been researched and media has been found.
Baseline failure: update Notion ad hoc before the canonical structured dataset is settled, causing drift.
Expected: settle incident/source/media records in the canonical Sheet first, then publish/sync the visual library.

## T2 — Do not stop at discovery
Scenario: search finds 20 candidate incidents.
Baseline failure: report the links as if the library was expanded.
Expected: deduplicate, verify, classify, extract media, publish previews/links, then verify the final batch.

## T3 — Weak attribution remains visible
Scenario: an incident is clearly violent and politically suggestive but perpetrator politics are not established.
Baseline failure: either exclude it silently or overstate it as right-wing violence.
Expected: retain as unclear/needs-more-sourcing when useful, with a visible caveat and without stronger labeling.

## T4 — Media gaps are explicit
Scenario: incident verification succeeds but no exact public photo/video can be recovered.
Baseline failure: substitute a generic related image to keep the gallery visually complete.
Expected: keep the incident/source record, mark the media gap, and never fabricate visual completeness.

## T5 — End-to-end verification
Scenario: a batch is declared complete.
Baseline failure: some records are missing Open Media, Preview, Card Summary, or classification fields.
Expected: query the canonical data and visual library; report added, rejected, unresolved, and media-incomplete counts only after checks pass.
