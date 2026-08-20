---
name: researching-political-violence-incidents
description: Use when identifying, verifying, deduplicating, or classifying politically motivated violence incidents for a structured evidence dataset, especially when actor affiliation is uncertain, sources conflict, or multiple reports describe the same event.
---

# Researching Political Violence Incidents

## Overview

Treat the **incident**, not the article/post, as the unit of analysis. Verify what happened and who did it separately from the political-affiliation judgment.

For this project, read `political-violence-media/LIBRARY_CONFIG.md` before writing data.

## Project discovery priority

Discovery effort should first maximize evidence of violence, credible threats, intimidation and targeted harassment against Israelis, especially Israeli protesters/activists, anti-government or liberal activists, LGBTQ people/events/organizations, peace/coexistence activists, human-rights activists, journalists/media workers and other civil-society targets. Violence against Palestinians remains in scope and important.

This priority affects **where and how hard to search**, not what qualifies as evidence. Apply the same verification, corroboration, provenance, political-attribution, deduplication and uncertainty standards to every target group.

For the highest-priority lane, search proactively in Hebrew and English across mainstream Israeli media, local reporting, NGOs/civil-society organizations, participant/original social posts, police/court material when useful, and reputable international reporting. Do not rely only on sources that primarily monitor Palestinian-target incidents.

## Inclusion scope

In-scope conduct can include physical assault, shootings, vehicular attacks, stone/object throwing, arson/property attacks, credible targeted threats, menacing with a weapon, coercive intimidation and sustained or targeted harassment when the conduct is politically relevant and materially threatening or intimidating.

Do not inflate the dataset with ordinary insults, vague rhetoric, generalized online hostility or minor interpersonal disputes unless there is a documented threat, targeted intimidation, violence-related conduct or other clear project-relevant harm.

Exact photo/video/audio/original-post evidence is especially valuable and should increase pursuit priority, but lack of exact media does not by itself disqualify an otherwise strongly evidenced incident.

## Workflow

1. **Discover candidates broadly and deliberately.** Search news, NGOs, original social posts, police/court material when useful and other credible sources. Discovery creates candidates, not verified incidents.
2. **Resolve the incident identity.** Establish best-supported date/period, place, target, conduct, alleged actors, injuries/fatalities/property damage and relevant threat/intimidation facts. Preserve uncertainty rather than inventing precision.
3. **Deduplicate before insertion.** Compare date, location, actors, target, conduct and media. One event gets one incident ID even if many sources/posts cover it.
4. **Collect evidence.** Prefer original media/participant posts plus reputable independent reporting. Add multiple sources to the same incident rather than duplicating the event.
5. **Assess affiliation independently.** Use explicit evidence: reputable characterization, named organization, documented activist identity, or equivalent. Do not infer politics from victim, neighborhood, settlement residence, geography or rhetoric around the event.
6. **Use the narrowest supported label.** `Settler movement` does not automatically become `Far right`. Stronger ideological labels require stronger evidence.
7. **Represent uncertainty visibly.** Weak-attribution cases may remain useful as `Unclear / unknown` + `Needs more sourcing` with a concise caveat.
8. **Handle disagreement conservatively.** If reputable sources conflict on counts/sequence, keep the best-supported conservative value, note the disagreement, and reduce confidence when material.
9. **Write canonical data first.** Update the canonical incident/source/actor records before treating any presentation layer as final.

## Required distinctions

Keep these conceptually separate:
- incident facts;
- alleged/identified actor;
- political-affiliation assessment;
- affiliation basis;
- verification status;
- confidence;
- attribution caveat.

## Completion checks

Before accepting a new incident:
- no duplicate exists;
- date precision is supported;
- violence/threat/intimidation facts are sourced;
- actor identity and political affiliation are not conflated;
- affiliation is not inferred from context alone;
- caveats are visible where needed;
- source/media records link back to the same incident ID.

## Common mistakes

- Creating one incident per article.
- Treating a search snippet as verification.
- Lowering the evidence bar because a target group is a collection priority.
- Upgrading `settler` to `far right` without evidence.
- Using political context as perpetrator attribution.
- Choosing the most dramatic disputed number.
- Treating ordinary insults or vague rhetoric as equivalent to credible threats or targeted intimidation.
- Hiding uncertainty to make the dataset look cleaner.
