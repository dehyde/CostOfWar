# Historical backfill — 2022-08-17 through 2026-08-17

This file defines the systematic historical-search layer that sits above the existing incident-research and media-publishing skills.

## Goal

Build a defensible, as-comprehensive-as-practical incident dataset by processing every month in the target period across multiple independent source lanes. Do not call a month complete until every lane is checked and all discovered candidates are resolved as accepted, duplicate, rejected, or unresolved.

## Source lanes

Check each lane independently for every month. A source can be useful for discovery, corroboration, media recovery, or political-attribution evidence; no single source is automatically authoritative for every field.

1. **OCHA** — settler-related incident dashboards, reports and protection updates.
2. **B'Tselem** — settler-violence updates, investigations, video and photo archives.
3. **Yesh Din** — settler violence, law-enforcement and case documentation.
4. **Reuters** — high-reliability international reporting and incident video/photo provenance.
5. **Associated Press** — high-reliability international reporting and visual corroboration.
6. **The Guardian / other major international reporting** — useful for named actors, ideological characterization and investigations.
7. **+972 Magazine / Local Call** — detailed Israeli-Palestinian reporting, field reporting and source discovery.
8. **The Times of Israel** — Israeli incidents, police reporting, protest violence, media attacks and embedded social footage.
9. **Haaretz** — Israeli and West Bank incidents, settler violence, political actors, journalists and protest coverage.
10. **Israeli broadcasters/news** — N12, Kan, Ynet, Walla and other credible Israeli outlets.
11. **Palestinian/local reporting** — credible local outlets and field sources, used with explicit source-quality notes and corroboration where possible.
12. **Original social / entity searches** — original posts, participant footage, named actors/groups, journalists, activists, organizations and recurring locations.

## Coverage unit

Process one calendar month at a time, except:
- 2022-08 covers 2022-08-17 through 2022-08-31.
- 2026-08 covers 2026-08-01 through 2026-08-17.

Always resume the oldest month whose status is not `Complete`. Do not advance merely because one run ended; leave the month `In progress` and continue it on the next run.

## Lane status

Use one of:
- `Pending`
- `In progress`
- `Complete`
- `No results`
- `Blocked`

`Blocked` means the lane could not be meaningfully checked because of access/index limitations. Record what was attempted. A month with a blocked lane may be marked `Complete with gaps`, not `Complete`.

## Candidate handling

Every candidate discovered in any lane must be resolved using the latest versions of:
- `political-violence-media/skills/researching-political-violence-incidents/SKILL.md`
- `political-violence-media/skills/publishing-evidence-media/SKILL.md`
- `political-violence-media/skills/expanding-political-violence-library/SKILL.md`
- `political-violence-media/LIBRARY_CONFIG.md`

Never infer right-wing politics from location, victim identity, settlement residence, Likud support, anti-media rhetoric, protest context, or other circumstantial context alone.

## Search method

For each source lane, use more than one query pattern when needed:
- date/month + settler attack / settler violence / extremist / right-wing / far-right;
- date/month + protester attacked / journalist attacked / activist attacked / political violence;
- recurring actors and groups found in earlier months;
- locations and victims found from OCHA/B'Tselem candidates;
- exact incident names to recover independent corroboration and original media.

Search in English and Hebrew when useful; use Palestinian/local-language sources as discovery/corroboration where accessible.

## Completeness discipline

A high candidate count is not a success metric. The success metric is source-lane coverage plus candidate resolution.

For every month, record:
- lane statuses;
- candidate count;
- accepted incident count;
- media-complete accepted count;
- duplicates/rejections;
- unresolved attribution/media gaps;
- short notes on search limitations.

## Output rules

Canonical incident/source/actor/media records go to Google Sheets first. Notion remains the visual/search layer and GitHub the stable preview store.

If exact media cannot be verified, preserve the incident without fabricating visual completeness. If politics cannot be established, use the existing unclear/needs-more-sourcing treatment.
