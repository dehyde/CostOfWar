# Channel 14 Fact-Check Library — configuration

## Canonical systems

### Google Sheets
- Spreadsheet: `Channel 14 Fact-Check Dataset`
- Spreadsheet ID: `150brXQotcZlptyCn19dj5_IedcFOh5mHRawFKuIknBs`
- Tabs: `README`, `Lookups`, `Claims`, `Sources`, `Media`
- Source of truth: settle claim wording, verdict, evidence and provenance here first.

### Notion
- Database: `Channel 14 Fact-Check Library`
- Database ID: `3cf0d8b466b04d769c9fa7d76b36d928`
- Data source ID: `a12e5e02-aa4c-44a1-ae69-a8510ab60d03`
- Gallery view ID: `3cef9fbd-425f-81f0-94d7-000c50777451`
- Cover property: `Preview`

### GitHub
- Repository: `dehyde/CostOfWar`
- Root: `channel14-factcheck/`
- Manifest: `channel14-factcheck/manifest.json`
- Preview path: `channel14-factcheck/previews/<media_id>.jpg`
- Shared workflow: `.github/workflows/build-accountability-previews.yml`

## Unit of analysis

One materially distinct factual claim = one canonical claim. Repeated broadcasts/posts may be additional sources/media on the same claim unless the wording or evidence changes materially.

## Inclusion

Include factual assertions that can be checked and that are materially important enough to document. Opinion, rhetoric, parody, predictions and value judgments are not false claims merely because they are objectionable.

A claim can be retained as a candidate when the original media is found but the verdict is unresolved.

## Verdicts

Use the narrowest supported verdict:
- `False` — reliable evidence directly contradicts the central factual assertion.
- `Misleading` — some literal elements may be true but presentation materially creates a false impression.
- `Unsupported` — a material assertion is presented as fact without adequate evidence and credible checking does not substantiate it.
- `Missing context` — omitted material facts substantially alter the meaning.
- `Outdated` — information once true is presented as current after materially changing.
- `Unverifiable` — available evidence cannot responsibly resolve the claim.
- `Accurate / no issue` — candidate was checked and does not belong in the misinformation library; retain only when useful for audit/rejection history, not the public gallery.

## Evidence threshold

Counter-evidence must include at least one strong non-social source that directly addresses the claim: official data/records, court or legal material, primary documents, state inquiries/audits, reputable independent reporting with identifiable sourcing, academic/research evidence, or similarly strong documentation.

Social posts can provide original media, discovery clues or attributable statements. They are not enough by themselves to establish the verdict.

For high-materiality claims, prefer two independent evidence routes whenever reasonably available.

## Media

Actual Channel 14 media is critical. Preserve separately:
- `Source Article` — provenance/context page;
- `Original Media` — closest original Channel 14 post/clip/page;
- `Direct Media URL` — direct playable/downloadable asset when stable enough;
- `Open Media` — direct playable > original public post/page > source page;
- `Preview` — exact still/frame from that exact Channel 14 claim.

Never use generic Channel 14 branding, presenter portraits or unrelated footage as the preview.

## Notion card contract

Gallery display order:
`Card Summary`, `Verdict`, `Topic`, `Speaker`, `Materiality`, `Verification`, `Open Media`, `Date`.

`Card Summary` should read naturally, e.g. `Channel 14 claimed X; official records show Y.` Keep it short. `Correction Summary` contains the concise correction and `Counter-evidence` contains the strongest evidence basis.

## Verification after writes

Query affected Sheet and Notion records after every batch. A published card should have an exact Preview, Claim ID, Date, Claim, Card Summary, Verdict, Correction Summary, Counter-evidence, Verification, Media Type and Open Media when media exists.
