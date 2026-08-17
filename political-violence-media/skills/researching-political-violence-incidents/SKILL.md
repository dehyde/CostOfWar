---
name: researching-political-violence-incidents
description: Use when identifying, verifying, deduplicating, or classifying politically motivated violence incidents for a structured evidence dataset, especially when actor affiliation is uncertain, sources conflict, or multiple reports describe the same event.
---

# Researching Political Violence Incidents

## Overview

Treat the **incident**, not the article/post, as the unit of analysis. Verify what happened and who did it separately from the political-affiliation judgment.

For this project, read `political-violence-media/LIBRARY_CONFIG.md` before writing data.

## Workflow

1. **Discover candidates broadly.** Search news, NGOs, original social posts and other credible sources. Discovery creates candidates, not verified incidents.
2. **Resolve the incident identity.** Establish best-supported date/period, place, target, conduct, alleged actors, injuries/fatalities/property damage. Preserve uncertainty rather than inventing precision.
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
- violence facts are sourced;
- actor identity and political affiliation are not conflated;
- affiliation is not inferred from context alone;
- caveats are visible where needed;
- source/media records link back to the same incident ID.

## Common mistakes

- Creating one incident per article.
- Treating a search snippet as verification.
- Upgrading `settler` to `far right` without evidence.
- Using political context as perpetrator attribution.
- Choosing the most dramatic disputed number.
- Hiding uncertainty to make the dataset look cleaner.
