---
name: publishing-factcheck-media
description: Use when recovering, validating, previewing, storing or publishing Channel 14 claim media and its fact-check evidence card.
---

# Publishing Fact-Check Media

Read `channel14-factcheck/LIBRARY_CONFIG.md` before writing.

## Media model

Keep separate:
- Source Article — provenance/context;
- Original Media — closest original Channel 14 clip/post/page;
- Direct Media URL — playable/downloadable asset when available;
- Open Media — direct asset > original public source > containing page;
- Preview — stable exact still/frame from the exact claim.

## Workflow

1. Confirm media contains the canonical claim or exact segment.
2. Recover the closest original Channel 14 source before relying on reposts.
3. Preserve the speaker/origin distinction; a guest claim is not automatically a Channel 14 editorial claim.
4. Build a Preview from the exact claim media. Never use generic Channel 14 logos, presenter portraits or unrelated footage.
5. Add preview manifest entry under `channel14-factcheck/manifest.json`; use the shared GitHub preview workflow.
6. Publish the Notion card only from settled canonical Sheet values.
7. Card Summary should be a short factual contrast, e.g. `Channel 14 claimed X; official records show Y.`
8. Preserve the strongest credible counter-evidence source separately from the original claim media.
9. Query the Notion record after writing and verify Preview, Open Media, Verdict and evidence fields.

## Required card fields

Claim ID, Date, Claim, Claim Origin, Card Summary, Verdict, Correction Summary, Counter-evidence, Verification, Confidence, Media Type, Open Media and exact Preview when media exists.
