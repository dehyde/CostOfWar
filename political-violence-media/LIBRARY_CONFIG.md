# Political Violence Media Library — project configuration

This file contains project-specific IDs, mappings and publishing conventions. Reusable skills should reference this file rather than hard-code these values.

## Canonical systems

### Google Sheets — source of truth
- Spreadsheet: `Political Violence in Israel — Incident Dataset`
- Spreadsheet ID: `1eP4b4RE72kf-Wbmu0Acn_UmOltwa7lFedYxm8fOKU1w`
- Tabs: `README`, `Lookups`, `Incidents`, `Sources`, `Incident Actors`, `Media`
- Canonical rule: settle structured incident/source/media facts here before treating the visual library as final.

### Notion — visual/searchable library
- Database: `Political Violence Media Library`
- Database ID: `530d54e4-bd47-4765-a998-df595dfa9676`
- Data source ID: `1099c1d9-b407-4232-b424-55a556aa58a8`
- Gallery view ID: `3bff9fbd-425f-81be-ab38-000cbc386258`
- Gallery cover property: `Preview`

### GitHub — stable preview store
- Repository: `dehyde/CostOfWar`
- Root: `political-violence-media/`
- Preview path: `political-violence-media/previews/<media_id>.jpg`
- Manifest: `political-violence-media/manifest.json`
- Workflow: `.github/workflows/build-political-violence-previews.yml`
- Temporary repository only; preserve folder structure so it can be migrated later.

## Collection priority

- **Highest discovery priority:** violence, credible threats, intimidation and targeted harassment against Israelis, especially Israeli protesters/activists, anti-government or liberal activists, LGBTQ people/events/organizations, peace/coexistence activists, human-rights activists, journalists/media workers and other civil-society targets.
- **Also important:** violence, credible threats, intimidation and targeted harassment against Palestinians.
- Priority controls search effort and ordering only. Apply the same verification, corroboration, provenance, political-attribution, deduplication and uncertainty standards to all target groups.
- Prefer exact recoverable photo/video/audio/original-post evidence when deciding which otherwise comparable candidates to pursue first. Do not reject a strongly evidenced incident solely because exact media is unavailable.
- Search the Israeli/civil-society lane proactively in Hebrew and English across Israeli news, local reporting, NGOs/civil-society organizations, participant/original social posts, police/court material when useful, and reputable international reporting.

## Inclusion scope

- In-scope conduct includes physical violence and serious violence-adjacent conduct such as credible targeted threats, menacing with weapons, coercive intimidation, property attacks and sustained or targeted harassment when it is materially threatening/intimidating and politically relevant.
- Ordinary insults, vague rhetoric, generalized online hostility and minor interpersonal disputes are not enough on their own.
- Preserve the most specific victim/target identity supported by sources in summaries/notes even when the canonical Target select uses a broader existing category.
- Do not invent new canonical select values ad hoc. If a more specific schema is desired, update the Sheet lookup/schema deliberately and then rehydrate presentation values.

## Data principles

- Unit of analysis is the **incident**, not the article/post.
- One incident may have many sources, actors and media items.
- Google Sheets is canonical. Notion is a presentation/review layer.
- Candidate discovery does not equal verification.
- Never infer right-wing affiliation from victim, location, neighborhood politics, settlement residence or surrounding rhetoric alone.
- Keep incident fact, actor identity, political affiliation, affiliation basis, verification status and confidence conceptually separate.
- Weak-attribution cases may remain in the dataset as `Unclear / unknown` / `Needs more sourcing` with an explicit caveat.

## Notion presentation mappings

Sheet values remain formal. Notion values should read naturally without property labels.

### Political affiliation
- `Mainstream right` -> `By mainstream-right actors`
- `Far right` -> `By far-right activists`
- `Religious-nationalist` -> `By religious-nationalist activists`
- `Settler movement` -> `By settlers`
- `Kahanist / Kach-related` -> `By Kahanist / Kach-related actors`
- `Right-aligned activist group` -> `By right-wing activist group`
- `Unclear / unknown` -> `Perpetrator politics unclear`
- `Other` -> `Other affiliation`

### Target
- `Palestinians — West Bank` -> `Against Palestinians in the West Bank`
- `Palestinians — East Jerusalem` -> `Against Palestinians in East Jerusalem`
- `Palestinians — Israel` -> `Against Palestinian citizens in Israel`
- `Palestinians — Gaza` -> `Against Palestinians in Gaza`
- `Israeli protesters / activists` -> `Against Israeli protesters / activists`
- `Israeli Jewish civilians` -> `Against Israeli Jewish civilians`
- `Israeli Arab / Palestinian citizens` -> `Against Palestinian / Arab citizens of Israel`
- `Property / institution` -> `Against an institution / property`
- `Other` -> `Against another target`

For LGBTQ people/events/organizations, peace/human-rights activists, journalists/media workers and other specific civil-society targets, use the closest supported existing canonical Target value and preserve the specific target identity in `Card Summary` and source/incident notes until a deliberate schema expansion is made.

### Other card fields
Keep these values concise and unprefixed because they are already self-explanatory:
- Media Type: `Video`, `Static image`, `Screenshot`, `Document`, `Other`
- Violence Type: existing classification labels
- Severity: existing classification labels
- Verification: existing verification labels

## Gallery display order

`Card Summary`, `Media Type`, `Affiliation`, `Target`, `Violence Type`, `Severity`, `Verification`, `Open Media`, `Date`, `Location`

`Card Summary` is one short human-readable sentence describing what happened. Prefer concrete actors/targets when supported, e.g. `Settler pepper-sprays Palestinian villager in Susiya.` Do not duplicate every badge in the summary.

## Media field semantics

- `Source Article`: reporting/source page establishing provenance/context.
- `Original Post`: original public social/participant post when available.
- `Direct Media URL`: closest recoverable direct playable/downloadable media URL.
- `Open Media`: best public click target using priority below.
- `Preview`: exact incident-specific static image stored on stable hosting.

### Open Media priority
1. Direct playable media.
2. Original public post/reel.
3. Source page containing/embedding the media.

### Preview rule
A gallery preview must be an actual JPEG/PNG/WebP representing the exact incident. Never use a video URL, generic location photo, similar incident, later incident, or illustrative stock image. If an exact still is not independently available, derive one from the exact video.

## X/Twitter media

When an original X post exists:
- preserve the original `x.com/.../status/...` URL;
- use FxTwitter/FxEmbed resolver/API where useful for direct playable media and video thumbnails;
- do not rely on temporary `video.twimg.com` CDN URLs as the durable canonical link;
- store/derive the preview into the GitHub preview store.

## Verification after writes

After every batch:
- query all affected Sheet rows and Notion records;
- verify required identifiers and incident links;
- verify every published media card has `Preview`, `Media Type`, `Open Media`, `Card Summary`, `Affiliation`, `Target`, `Violence Type`, `Severity`, `Verification`, `Date`, and `Location` as applicable;
- verify preview URLs point to the correct `media_id` file;
- verify no select-property schema change silently cleared existing values.
