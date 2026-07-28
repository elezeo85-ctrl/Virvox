# VIRVOX Project Map

```text
VIRVOX
│
├── BRAND/       Brand Book and visual identity
├── ASSETS/      Registered project assets
├── CONTENT/     Articles and content production
├── TEMPLATES/   Reusable content and design templates
├── REGISTRY/    Authoritative object registries
├── SYSTEM/      Commands, workflows, and automation
└── DOCS/        Project knowledge and governance
        │
        └── GitHub = documentation source of truth

Canva
│
├── Logos
├── Category master assets
├── Covers
└── Other editable visual designs
        │
        └── Canva = editable design source of truth

Content production
│
├── Articles
├── Covers
├── Stories
├── Reels
├── Telegram
├── YouTube
└── Site
```

## Core relationships

1. A visual asset receives an internal ID and, where applicable, a Canva Design ID.
2. The asset is recorded in `REGISTRY/ASSET_REGISTRY`.
3. Categories are recorded in `REGISTRY/CATEGORY_REGISTRY` and linked to `BA-CAT-001`.
4. Templates reference approved assets and categories rather than duplicating their definitions.
5. Content references categories and templates through stable IDs.
6. Documentation records the rules and relationships governing the system.

## Operational flow

`Idea → Content object → Category assignment → Template selection → Asset resolution → Production → Registration → Publication`
