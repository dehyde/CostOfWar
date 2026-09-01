# Israeli Political Leadership Accountability Library — configuration

## Canonical systems

### Google Sheets
- Spreadsheet: `Israeli Political Leadership Accountability Dataset`
- Spreadsheet ID: `1ONc8tdStg-nGS_GAtAPy74goVRsN7k8lCJxCeRYgHG4`
- Tabs: `README`, `Lookups`, `Events`, `Sources`, `Media`, `People`
- Source of truth: settle event facts, evidence, legal status, outcome and provenance here first.

### Notion
- Database: `Israeli Political Leadership Accountability Library`
- Database ID: `137dbc8e9b5a4d968081ccb0ad554e60`
- Data source ID: `b46a0984-424b-45d2-bd41-8e5297009a49`
- Gallery view ID: `3cef9fbd-425f-81be-a725-000cb13c0f63`
- Cover property: `Preview`

### GitHub
- Repository: `dehyde/CostOfWar`
- Root: `leadership-accountability/`
- Manifest: `leadership-accountability/manifest.json`
- Preview path: `leadership-accountability/previews/<media_id>.jpg`
- Shared workflow: `.github/workflows/build-accountability-previews.yml`

## Initial core subjects
- Benjamin Netanyahu
- Bezalel Smotrich
- Itamar Ben-Gvir

Expand to other prominent right-wing party leaders only when they are nationally prominent or materially relevant. Keep `People` as the canonical subject list.

## Unit of analysis

One distinct statement, decision, commitment/outcome pair, official finding, legal/ethical episode, documented management failure or personal-conduct episode = one event. Multiple reports belong as Sources, not duplicate Events.

## Categories

Use the narrowest supported category:
- `False / misleading statement`
- `Broken commitment / contradiction`
- `Governance / management failure`
- `Conflict / political self-interest`
- `Legal / ethical issue`
- `Documented personal misconduct`
- `Operational / preparedness failure`
- `Other documented accountability issue`

## Neutral evidence discipline

This is an accountability archive, not a persuasion scorecard. Do not write entries merely because a policy is unpopular or ideological.

Separate:
1. what the leader said/did or was responsible for;
2. what credible evidence establishes;
3. documented outcome/consequence;
4. any concern/interpretation;
5. the leader's response/defense when material;
6. legal status when applicable.

### Failures
A bad outcome alone is insufficient. A governance/management/operational failure should have a documented responsibility link: authority over the area, explicit commitment, ignored warning, audit/inquiry finding, operational decision, documented management breakdown, or similarly concrete evidence.

### Political self-interest / conflicts
Do not infer motive from political disagreement. Include when there is specific evidence of a conflict, personal/political incentive, contemporaneous statement, institutional finding, or credible reporting that directly establishes the tension with the public interest. Phrase the event as the documented facts, not as mind-reading.

### Legal / ethical matters
Preserve exact status: allegation, investigation, charge/indictment, finding/ruling, conviction, acquittal/dismissal, or ongoing/unresolved. Never describe an allegation or indictment as proof of guilt. Include important defenses, acquittals, dismissals or later reversals.

### False statements
Treat like fact-checking: factual assertion + strong contradictory evidence. Opinion, prediction and rhetoric are not false statements merely because they are controversial.

## Evidence sources

Prefer official/state records, court documents, State Comptroller or inquiry findings, Knesset/government documents, primary statements, police/legal records, reputable Israeli/international reporting, and strong research evidence.

Social posts can supply exact original statements/media and discovery clues but do not by themselves prove contested factual claims, failures, motives or guilt.

For high-stakes or highly contestable entries, prefer at least two independent evidence routes and record contrary evidence/response.

## Media

Actual media is critical. Preserve exact speech/interview video, official announcement, photo, court/inquiry document, recording or event footage when recoverable.

Fields remain distinct:
- `Source Article` — provenance/context;
- `Original Media` — closest original statement/event/document;
- `Direct Media URL` — direct playable/downloadable asset;
- `Open Media` — direct asset > original public source > source article;
- `Preview` — exact still/frame/page from that exact event/document.

Never use generic portraits as a substitute for event evidence.

## Notion card contract

Gallery display order:
`Card Summary`, `Subject`, `Category`, `Legal Status`, `Verification`, `Media Type`, `Open Media`, `Date`.

`Card Summary` is one factual sentence. `Documented concern` explains the accountability issue without advocacy. `Response / defense` should be populated when the subject materially disputes the framing or facts.

## Verification after writes

Query all affected Sheet and Notion records after every batch. A published card should have Preview when exact media exists, Event ID, Date, Subject, Category, Card Summary, What happened, Documented concern, Verification, Media Type and Open Media. Legal Status must be accurate whenever legal proceedings are relevant.
