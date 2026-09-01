---
name: publishing-accountability-media
description: Use when recovering, validating, previewing, storing or publishing exact media for a political-leadership accountability event.
---

# Publishing Accountability Media

Read `leadership-accountability/LIBRARY_CONFIG.md` before writing.

## Media model

Keep separate:
- Source Article — provenance/context;
- Original Media — closest original statement/event/document;
- Direct Media URL — playable/downloadable asset;
- Open Media — direct asset > original public source > source article;
- Preview — stable exact still/frame/page from the exact event/document.

## Workflow

1. Confirm media belongs to the exact canonical event.
2. Prefer original speeches/interviews, government/Knesset video, official documents, court/inquiry material and incident-specific footage.
3. Do not use generic leader portraits as evidence previews.
4. Add recoverable media to `leadership-accountability/manifest.json` for stable preview generation.
5. For documents, use an exact page/image when feasible; otherwise the document itself may be Open Media while the card remains without a visual preview until an exact preview is created.
6. Publish Notion only from canonical settled values.
7. Card Summary is one factual sentence. `Documented concern` carries the accountability issue; `Response / defense` carries material counter-position.
8. Query the page after writing and verify exact preview, legal status, category and media links.

## Required card fields

Event ID, Date, Subject, Category, Card Summary, What happened, Documented concern, Verification, Confidence, Legal Status, Media Type and Open Media when media exists. Include Response/defense when material.
