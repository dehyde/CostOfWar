---
name: publishing-evidence-media
description: Use when recovering, validating, previewing, storing, or publishing photos/videos/posts for an evidence library, especially when social-platform links, video embeds, CDN images, or gallery previews are unreliable.
---

# Publishing Evidence Media

## Overview

Separate provenance, original post, direct media and gallery preview. A reliable gallery needs an **exact static preview image** even when the evidence itself is video.

For this project, read `political-violence-media/LIBRARY_CONFIG.md` before writing.

## Publishing priority

When several already-verified incidents/media items are waiting for recovery or publication, process the project's highest-priority Israeli/civil-society lane first: violence, credible threats, intimidation and targeted harassment against Israeli protesters/activists, anti-government or liberal activists, LGBTQ people/events/organizations, peace/coexistence activists, human-rights activists, journalists/media workers and other civil-society targets. Continue publishing Palestinian-target incidents as well.

This affects processing order only. Exactness, provenance and verification standards are identical for every target group.

## Media model

Maintain distinct fields:
- **Source Article** — reporting/provenance page.
- **Original Post** — original public social/participant post.
- **Direct Media URL** — closest recoverable playable/downloadable asset.
- **Open Media** — best public click target.
- **Preview** — stable exact incident-specific static image.

Never substitute one field for all the others.

## Workflow

1. **Start from the verified incident/media candidate.** Confirm the media belongs to that incident before publishing it.
2. **Recover the closest original.** Prefer participant/original posts over secondary embeds when available. Search aggressively for the exact original on high-priority Israeli/civil-society incidents.
3. **Resolve playable media when practical.** For X/Twitter, preserve the original X URL and use FxTwitter/FxEmbed for direct media/thumbnail recovery when useful. Avoid treating temporary CDN URLs as durable canonical links.
4. **Choose Open Media by priority:** direct playable media > original public post/reel > source page containing the media.
5. **Build the Preview separately.** Use an exact JPEG/PNG/WebP from the incident. If none exists, derive a frame from the exact video.
6. **Reject merely related imagery.** Same village, same actor, similar attack, later attack or generic illustrative photo is not acceptable evidence for the card.
7. **Store the preview on stable project hosting.** Use the configured preview path keyed by `media_id`; do not leave the gallery dependent on an arbitrary publisher/social CDN.
8. **Publish the visual record.** Card summary should be one short natural sentence. Preserve the most specific supported target identity in the summary, especially when the canonical Target value is broader. Display classification values so they make sense without field labels, e.g. `By settlers`, `Against Palestinians in the West Bank`.
9. **Do not create redundant display-only badge fields.** Prefer conversational values in the existing presentation properties while keeping the canonical Sheet values formal.
10. **After schema-option edits, rehydrate immediately.** Notion select-option changes can clear existing values; restore from the canonical dataset before continuing.
11. **Verify the batch.** Query every affected record after writes rather than trusting successful update calls.

## Completion contract

A published media card should have, when applicable:
- exact `Preview`;
- `Media Type`;
- `Open Media`;
- `Card Summary`;
- conversational `Affiliation` and `Target`;
- `Violence Type`, `Severity`, `Verification`;
- `Date` and `Location`;
- provenance/original/direct-media links preserved separately.

## Common mistakes

- Putting a video URL in a gallery image field.
- Using a related but non-exact photo.
- Conflating a later incident's still with an earlier incident.
- Linking only to an article when an original/direct media target exists.
- Lowering exactness/provenance standards because a target group is a collection priority.
- Assuming a Notion write rendered correctly without querying it afterward.
