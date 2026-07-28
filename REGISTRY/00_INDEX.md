# VIRVOX Registry System

## Purpose

The Registry System is the authoritative index of VIRVOX objects and their relationships.

## Architecture

```text
REGISTRY/
├── 00_INDEX.md
├── MASTER_REGISTRY.yaml
├── ASSET_REGISTRY.yaml
├── CATEGORY_REGISTRY.yaml
├── ARTICLE_REGISTRY.yaml
├── TEMPLATE_REGISTRY.yaml
└── CANVA_REGISTRY.yaml

CONTENT/
└── ARTICLES/
    └── ART-XXX/
        ├── article.md
        ├── metadata.yaml
        ├── sources.yaml
        └── assets.yaml
```

## Principle

Registries contain structured metadata and references. Long-form article text is stored separately in `CONTENT/ARTICLES/` and is referenced by `content_file`.

## Registry roles

- `MASTER_REGISTRY.yaml` — cross-object index and relationships.
- `ASSET_REGISTRY.yaml` — brand and production assets.
- `CATEGORY_REGISTRY.yaml` — official content categories.
- `ARTICLE_REGISTRY.yaml` — article metadata and links to article folders.
- `TEMPLATE_REGISTRY.yaml` — reusable templates.
- `CANVA_REGISTRY.yaml` — verified Canva Design IDs linked to internal assets.

## Article storage model

Each article is a self-contained content package. The registry points to the package; it does not contain the full article text.

## Source of truth

GitHub is the source of truth for registry data and article text. Canva is the source of truth for editable visual designs referenced by Canva IDs.
