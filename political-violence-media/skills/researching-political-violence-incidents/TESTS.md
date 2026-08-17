# Baseline tests — researching-political-violence-incidents

These scenarios are based on failures and near-failures observed while building the current library. They define the behavior the skill must prevent.

## T1 — Context is not attribution
Scenario: Democrats activists are attacked at Hatikva Market. Reporting notes the neighborhood is politically right-leaning, but does not identify the assailants' politics.
Baseline failure: classify the attackers as right-wing from context.
Expected: record the attack; set political affiliation to unclear/unknown; mark needs more sourcing; state the attribution caveat.

## T2 — One incident, many sources
Scenario: the same attack appears in a news report, NGO report, X post, and video.
Baseline failure: create a new incident for each source/media item.
Expected: one incident record, multiple source/media records linked to it.

## T3 — Approximate dates stay approximate
Scenario: a report says a siege began 'the previous weekend' and continued for nearly a week.
Baseline failure: invent a precise start date without evidence.
Expected: preserve uncertainty in time_or_period/review notes and use only the best-supported date field.

## T4 — Settler identity is not automatically 'far right'
Scenario: a reputable source explicitly calls the attackers settlers but gives no stronger ideological description.
Baseline failure: upgrade affiliation to far right.
Expected: classify as settler movement only; stronger labels require stronger evidence.

## T5 — Candidate discovery is not verification
Scenario: a search result or social post alleges political violence but the incident has not yet been corroborated.
Baseline failure: publish directly as verified right-wing violence.
Expected: candidate/unreviewed first; corroborate incident facts and actor attribution separately.

## T6 — Source disagreement
Scenario: two reputable sources disagree on injury count or exact sequence.
Baseline failure: silently choose the more dramatic version.
Expected: keep the conservative supported value, note the disagreement, and lower confidence/verification if material.

## T7 — Duplicate detection before insertion
Scenario: a newly found article describes an incident already present with a slightly different location label or date wording.
Baseline failure: insert a duplicate.
Expected: compare date, place, actors, target, conduct, and media before creating a new incident.
