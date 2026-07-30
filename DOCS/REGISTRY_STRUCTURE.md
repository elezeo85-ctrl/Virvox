# REGISTRY STRUCTURE

## Purpose

The registry system provides canonical, machine-readable indexes and relationships between VIRVOX objects.

## Canonical location

Authoritative registry data is stored in `REGISTRY/` using the approved registry formats defined by `DOCS/PROJECT_RULES.md`.

Markdown files in `REGISTRY/` are for documentation, navigation, schemas, and instructions. They are not substitutes for authoritative registry data unless explicitly designated by the architecture.

## Core registries

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

## Relationships

```text
MASTER_REGISTRY
      │
      ├── CATEGORY_REGISTRY
      ├── ARTICLE_REGISTRY
      ├── ASSET_REGISTRY
      ├── TEMPLATE_REGISTRY
      └── CANVA_REGISTRY
```

Objects should retain stable IDs and references across registries. A registry record should identify the object and its relationships; detailed content belongs in the appropriate content or asset location.

## Article registry model

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

The article registry is an index and relationship layer. The full article content is stored in the article object directory.

## Canva relationship

Visual assets created or maintained in Canva must preserve their Canva Design ID and associate it with the corresponding registered asset or design object.

## Verification

Registry changes should be checked for:

- unique IDs;
- required fields;
- valid cross-references;
- no duplicate identities;
- consistency between registry records and stored objects;
- preservation of Canva Design IDs where applicable.
