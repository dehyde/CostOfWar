# Political Violence Media

Temporary project home for the Political Violence in Israel incident/media library. The folder is intentionally self-contained so it can be migrated to a dedicated repository later.

## Architecture

- Google Sheets: canonical structured data.
- Notion: visual/searchable media library.
- GitHub: stable preview-image hosting and extraction workflow.

See `LIBRARY_CONFIG.md` for the current project IDs, field mappings and publishing rules.

## Reusable skills

- `skills/researching-political-violence-incidents/` — candidate discovery, verification, attribution and deduplication.
- `skills/publishing-evidence-media/` — original-media recovery, stable previews and gallery publication.
- `skills/expanding-political-violence-library/` — end-to-end batch orchestration using the two skills above.

Each skill has baseline regression scenarios in `TESTS.md`. `skills/VERIFICATION.md` records the current green checks against the live library.

## Media files

Preview images are keyed by media ID under `previews/`. `manifest.json` and the GitHub Actions workflow build/refresh those stable preview files.
