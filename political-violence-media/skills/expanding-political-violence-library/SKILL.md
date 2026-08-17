---
name: expanding-political-violence-library
description: Use when expanding, refreshing, or batch-maintaining a political-violence evidence library from candidate discovery through structured records and published media cards.
---

# Expanding Political Violence Library

## Overview

Run the library as a pipeline, not as a pile of links. Canonical structured data is settled first; the visual/media layer is published from it and verified afterward.

**REQUIRED SUB-SKILL:** Use `researching-political-violence-incidents` for candidate verification and classification.

**REQUIRED SUB-SKILL:** Use `publishing-evidence-media` for original-media recovery, previews and gallery publication.

For this project, read `political-violence-media/LIBRARY_CONFIG.md` first.

## Batch workflow

1. **Define the batch.** Time window, geography, target populations, violence threshold and any requested search focus.
2. **Discover candidates.** Search broadly. Keep a candidate list separate from accepted incidents.
3. **Research and deduplicate.** Apply `researching-political-violence-incidents` to every candidate worth pursuing.
4. **Write canonical records.** Create/update incident, source, actor and media rows in the canonical dataset. Do not let Notion become the source of truth.
5. **Recover and publish media.** Apply `publishing-evidence-media` for each accepted media item.
6. **Keep weak cases honest.** If violence is verified but political attribution is not, retain only when useful and label it unclear/needs-more-sourcing with the caveat visible.
7. **Never fake visual completeness.** A media gap is preferable to a non-exact image.
8. **Verify end to end.** Query both canonical data and visual records after the batch.

## Batch completion report

Report only after verification:
- incidents added;
- incidents updated;
- candidates rejected/duplicates;
- cases still needing sourcing;
- media-complete vs media-incomplete records;
- any unresolved provenance or attribution issue that affects interpretation.

Keep the user-facing report concise unless a detailed audit is requested.

## Stop conditions

Do not call a batch complete if:
- duplicate checks were skipped;
- political attribution relies only on context;
- canonical records and Notion disagree;
- a published card lacks required media/display fields;
- a preview is not proven to belong to the exact incident;
- schema changes may have cleared values and no re-query was performed.
