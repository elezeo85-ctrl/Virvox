# VIRVOX Project Rules

## Mandatory rules

1. Approved assets are not deleted without a documented replacement or deprecation record.
2. Every registered object must have a stable internal ID.
3. Canva Design IDs must be recorded for visual assets that originate in Canva.
4. GitHub is the authoritative source for documentation, registries, architecture, and project rules.
5. Canva is the authoritative source for editable visual design files.
6. Changes to approved standards must be documented and versioned.
7. New assets and templates must be registered before being treated as production standards.
8. Category names shown to users are controlled by `CATEGORY_REGISTRY`; internal IDs remain stable even if display text changes.
9. No information should be invented when the authoritative source is unavailable; uncertainty must be marked explicitly.
10. Important project decisions must be recorded in `DECISIONS.md`.
11. Major structural changes must be reflected in `VERSION_HISTORY.md` and `CHANGELOG.md`.
12. Documentation should link related objects by stable IDs rather than relying only on display names.

## Naming conventions

- `BA-` — Brand Asset.
- `CAT-` — Content Category.
- `ART-` — Article.
- `TPL-` — Template.
- `DOC-` — Document.

## Status vocabulary

- `Draft` — work in progress.
- `Pending` — awaiting confirmation.
- `Approved` — approved for production use.
- `Deprecated` — retained for history but no longer used for new work.

## Versioning

Use semantic-style versions where practical: `MAJOR.MINOR.PATCH`.

- Major: structural or compatibility-breaking change.
- Minor: new approved capability or section.
- Patch: correction or clarification without structural impact.
