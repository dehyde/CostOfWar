# Baseline tests — publishing-evidence-media

These scenarios are based on failures and near-failures observed while building the current library.

## T1 — Video URL is not a gallery thumbnail
Scenario: an X/FxTwitter video resolver URL is assigned to Notion Preview.
Baseline failure: gallery card renders blank.
Expected: obtain an actual JPEG/PNG still; store it on stable hosting; use that image for Preview; keep the video separately as Open Media.

## T2 — Exact incident imagery only
Scenario: image search finds a dramatic photo from the same village or a similar later attack.
Baseline failure: use the related image as the incident preview.
Expected: reject it unless it is demonstrably from the exact incident. Derive a frame from the exact video if necessary.

## T3 — Later event must not stand in for earlier event
Scenario: a news article about a second attack contains imagery referencing the first attack.
Baseline failure: conflate the image with the wrong event.
Expected: trace provenance and date; if exactness is uncertain, do not use the image as the preview.

## T4 — Separate four media concepts
Scenario: one record has a news article, an original X post, a direct playable video and a preview still.
Baseline failure: put the same URL in every field or treat the article as the media.
Expected: Source Article, Original Post, Direct Media URL/Open Media and Preview are distinct fields with distinct purposes.

## T5 — Direct-link fallback order
Scenario: a direct MP4 cannot be recovered, but the original Instagram Reel exists.
Baseline failure: link only to a secondary article.
Expected: Open Media priority is direct playable media > original post > source page containing the media.

## T6 — Stable preview hosting
Scenario: a publisher CDN URL renders today but may expire/block embedding.
Baseline failure: leave Notion dependent on that external host.
Expected: copy/derive the exact preview into the project preview store and use the stable project URL.

## T7 — Schema option edits can erase values
Scenario: Notion select option labels are changed for presentation.
Baseline failure: existing select values become blank and remain unnoticed.
Expected: immediately rehydrate the affected properties from the canonical Sheet and verify every row after the schema change.

## T8 — Gallery labels must make sense without field names
Scenario: Notion gallery displays only values, not property names.
Baseline failure: cards show ambiguous badges such as 'Settler movement' or 'Palestinians — West Bank'.
Expected: use conversational self-contained values such as 'By settlers' and 'Against Palestinians in the West Bank', without creating redundant display-only duplicate fields.

## T9 — Batch completion must be verified
Scenario: ten records are updated.
Baseline failure: assume all previews/links were written because the update calls succeeded.
Expected: query the database after the batch and verify required fields are populated for every record.
