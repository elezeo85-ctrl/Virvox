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
13. All authoritative registries are stored in YAML (`.yaml`) as the canonical structured data format.
14. Markdown (`.md`) in `REGISTRY/` is reserved for registry documentation, navigation, schemas, instructions, and human-readable explanations; it is not the canonical data store for registries.
15. Long-form article text is not stored inside `ARTICLE_REGISTRY.yaml`. It is stored in the corresponding article package under `CONTENT/ARTICLES/ART-XXX/article.md`.
16. Article metadata and related structured data are stored in YAML files within the article package, including `metadata.yaml`, `sources.yaml`, and `assets.yaml` where applicable.
17. Registry records must reference content and related objects by stable IDs and file paths rather than duplicating long-form content.

## Registry Data Standard v1.0

The VIRVOX Registry System uses YAML as the canonical format for all registries.

```text
REGISTRY/
├── 00_INDEX.md
├── MASTER_REGISTRY.yaml
├── ASSET_REGISTRY.yaml
├── CATEGORY_REGISTRY.yaml
├── ARTICLE_REGISTRY.yaml
├── TEMPLATE_REGISTRY.yaml
└── CANVA_REGISTRY.yaml
```

### Format responsibilities

- `.yaml` — canonical structured registry data.
- `.md` — documentation, navigation, instructions, and explanations of registry structure.
- `article.md` — canonical long-form article text; it is content, not a registry.
- `metadata.yaml` — structured article passport and metadata.
- `sources.yaml` — structured article source references.
- `assets.yaml` — structured references to visual and production assets associated with an article.

### Article architecture

```text
ARTICLE_REGISTRY.yaml
        ↓
     ART-001
        ↓
CONTENT/ARTICLES/ART-001/
├── article.md
├── metadata.yaml
├── sources.yaml
└── assets.yaml
```

The registry acts as an index and relationship layer. It must remain compact and machine-readable. Full article text belongs in the article package and is referenced from the registry through stable IDs and file paths.

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
