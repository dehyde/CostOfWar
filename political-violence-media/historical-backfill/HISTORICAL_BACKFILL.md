# Historical backfill — 2022-08-17 through 2026-08-17

This file defines the systematic historical-search layer that sits above the existing incident-research and media-publishing skills.

## Goal

Build a defensible, as-comprehensive-as-practical incident dataset by processing every month in the target period across multiple independent source lanes. Do not call a month complete until every lane is checked and all discovered candidates are resolved as accepted, duplicate, rejected, or unresolved.

Within every month, discovery effort should first maximize well-sourced, showcaseable evidence/media of violence, credible threats, intimidation and targeted harassment against Israelis, especially Israeli protesters/activists, anti-government or liberal activists, LGBTQ people/events/organizations, peace/coexistence activists, human-rights activists, journalists/media workers and other civil-society targets. Violence against Palestinians remains important and all normal source lanes must still be completed.

Priority changes search order and effort only. Apply the same verification, corroboration, provenance, political-attribution, deduplication and uncertainty standards to every target group.

## Source lanes

Check each lane independently for every month. A source can be useful for discovery, corroboration, media recovery, or political-attribution evidence; no single source is automatically authoritative for every field.

1. **Israeli civil-society / target-specific discovery** — explicit Hebrew and English searches for attacks, threats, intimidation and harassment targeting Israeli protesters/activists, anti-government or liberal activists, LGBTQ people/events/organizations, peace/coexistence activists, human-rights activists, journalists/media workers and other civil-society targets. Search Israeli media, local reporting, relevant NGOs/organizations, participant/original social posts, and police/court material when useful.
2. **OCHA** — settler-related incident dashboards, reports and protection updates.
3. **B'Tselem** — settler-violence updates, investigations, video and photo archives.
4. **Yesh Din** — settler violence, law-enforcement and case documentation.
5. **Reuters** — high-reliability international reporting and incident video/photo provenance.
6. **Associated Press** — high-reliability international reporting and visual corroboration.
7. **The Guardian / other major international reporting** — useful for named actors, ideological characterization and investigations.
8. **+972 Magazine / Local Call** — detailed Israeli-Palestinian reporting, field reporting and source discovery.
9. **The Times of Israel** — Israeli incidents, police reporting, protest violence, media attacks and embedded social footage.
10. **Haaretz** — Israeli and West Bank incidents, settler violence, political actors, journalists and protest coverage.
11. **Israeli broadcasters/news** — N12, Kan, Ynet, Walla and other credible Israeli outlets.
12. **Palestinian/local reporting** — credible local outlets and field sources, used with explicit source-quality notes and corroboration where possible.
13. **Original social / entity searches** — original posts, participant footage, named actors/groups, journalists, activists, organizations and recurring locations.

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

Prefer candidates with exact recoverable photo/video/audio/original-post evidence when deciding which otherwise comparable candidates to pursue first, but do not reject a strongly evidenced incident solely because exact media is unavailable.

## Search method

For each source lane, use more than one query pattern when needed:
- date/month + protester attacked / demonstrator attacked / protest violence / activist threatened / activist harassed;
- date/month + liberal / anti-government / democracy protest + attack / threat / intimidation / harassment;
- date/month + LGBTQ / Pride / queer / gay / trans + attack / threat / harassment / vandalism;
- date/month + journalist attacked / media worker threatened / camera crew attacked;
- date/month + peace activist / human-rights activist / coexistence activist + attack / threat / harassment;
- date/month + settler attack / settler violence / extremist / right-wing / far-right;
- recurring actors and groups found in earlier months;
- locations and victims found from OCHA/B'Tselem candidates;
- exact incident names to recover independent corroboration and original media.

Search in English and Hebrew. Use Palestinian/local-language sources as discovery/corroboration where accessible.

## Completeness discipline

A high candidate count is not a success metric. The success metric is source-lane coverage plus candidate resolution. However, because the library is intended to support a large visual showcase, recoverable exact media is a meaningful secondary optimization criterion after evidence quality.

For every month, record:
- lane statuses, including the Israeli civil-society / target-specific lane;
- candidate count;
- accepted incident count;
- media-complete accepted count;
- duplicates/rejections;
- unresolved attribution/media gaps;
- short notes on search limitations.

## Output rules

Canonical incident/source/actor/media records go to Google Sheets first. Notion remains the visual/search layer and GitHub the stable preview store.

If exact media cannot be verified, preserve the incident without fabricating visual completeness. If politics cannot be established, use the existing unclear/needs-more-sourcing treatment.
