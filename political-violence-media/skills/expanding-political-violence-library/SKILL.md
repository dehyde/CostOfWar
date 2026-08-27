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

## Collection priority

For this project, discovery effort is intentionally asymmetric while evidence standards remain symmetric.

1. **Highest discovery priority:** maximize well-sourced, showcaseable evidence/media of violence, credible threats, intimidation and targeted harassment against Israelis, especially Israeli protesters/activists, anti-government or liberal activists, LGBTQ people/events/organizations, peace/coexistence activists, human-rights activists, journalists/media workers and other civil-society targets.
2. **Also important:** continue collecting violence, threats, intimidation and targeted harassment against Palestinians when they satisfy the same inclusion and evidence rules.
3. **Same evidentiary threshold for every target group.** Search priority must never weaken corroboration, provenance, attribution, deduplication or uncertainty standards.
4. **Media-first pursuit within otherwise comparable candidates.** Prefer candidates with exact recoverable photo/video/audio/original-post evidence because the library is intended to be showcaseable, but do not reject a strongly evidenced incident solely because exact media is unavailable.
5. Search proactively in Hebrew and English. For the highest-priority lane, explicitly search mainstream Israeli media, local reporting, NGOs/civil-society organizations, participant/original social posts, police/court material when useful, and reputable international reporting. Do not rely on passive discovery from Palestinian-focused monitoring sources.

## Continuous freshness lane

For recurring expansion runs, the fresh-content scan is mandatory and separate from historical backfill.

1. **Always run a freshness pass first.** Search for relevant incidents that occurred since the previous successful expansion run and for relevant reporting/media newly published since that run, including material about older incidents.
2. **Never allow a gap from the monitoring start date.** For this project, treat **2026-08-18** as the continuous-monitoring start date. If run history is unavailable or uncertain, search from 2026-08-18 through the current run date.
3. **Use a rolling lookback.** Re-scan at least the previous 14 days on every run so delayed reporting, late uploads, reposts pointing to originals, police/court follow-up and newly indexed material are not missed.
4. **Search both incident date and publication date.** A newly surfaced exact video/photo/post for an incident already known is a valid fresh candidate even when no new incident row is needed.
5. **Use explicit current-event lanes.** Search Hebrew and English mainstream Israeli media, local outlets, NGOs/civil-society sources, participant/original social posts, police/court updates and reputable international reporting for fresh items. Search the high-priority Israeli/civil-society lane most aggressively while still checking Palestinian-target lanes.
6. **Deduplicate before writing.** Freshness discovery must be checked against existing incident/media records; add new media or sourcing to an existing incident rather than creating duplicates.
7. **Backfill does not satisfy freshness.** Historical coverage work may run in parallel, but a recurring expansion run is incomplete if the freshness pass was skipped.

## Batch workflow

1. **Define the batch.** Time window, geography, target populations, violence threshold and requested search focus. Apply the project collection priority above unless the user explicitly overrides it. For recurring runs, include the mandatory continuous freshness lane.
2. **Discover candidates.** Search broadly and deliberately across target-specific source lanes. Keep a candidate list separate from accepted incidents.
3. **Research and deduplicate.** Apply `researching-political-violence-incidents` to every candidate worth pursuing.
4. **Write canonical records.** Create/update incident, source, actor and media rows in the canonical dataset. Do not let Notion become the source of truth.
5. **Recover and publish media.** Apply `publishing-evidence-media` for each accepted media item. Pursue the closest original media and exact incident preview aggressively for high-priority Israeli/civil-society incidents.
6. **Keep weak cases honest.** If the incident is verified but political attribution is not, retain only when useful and label it unclear/needs-more-sourcing with the caveat visible.
7. **Never fake visual completeness.** A media gap is preferable to a non-exact image.
8. **Verify end to end.** Query both canonical data and visual records after the batch.

## Batch completion report

Report only after verification:
- Israeli/civil-society incidents and media added or updated first;
- Palestinian-target incidents and media added or updated;
- candidates rejected/duplicates;
- cases still needing sourcing;
- media-complete vs media-incomplete records;
- any unresolved provenance or attribution issue that affects interpretation.

Keep the user-facing report concise unless a detailed audit is requested.

## Stop conditions

Do not call a batch complete if:
- the mandatory freshness pass was skipped on a recurring run;
- the high-priority Israeli/civil-society discovery lane was skipped without an explicit reason;
- duplicate checks were skipped;
- political attribution relies only on context;
- canonical records and Notion disagree;
- a published card lacks required media/display fields;
- a preview is not proven to belong to the exact incident;
- schema changes may have cleared values and no re-query was performed.
