# VIRVOX Canonical Repository Structure

## Purpose

This document defines the canonical physical structure of the VIRVOX repository. It is the reference tree used to determine where project files and directories belong and is maintained from the approved architecture, Brand Book repository model, documentation, and actual repository state.

- `ARCHITECTURE.md` explains **how the system is organized conceptually**.
- `REPOSITORY_STRUCTURE.md` defines **where files and directories physically belong**.
- `REPOSITORY_STRUCTURE_RULES.md` defines **the rules for creating, moving, renaming, or deleting structural elements**.
- `REPOSITORY_STRUCTURE_UPDATE.md` defines **the required procedure for updating this document whenever the repository changes**.
- `ARTICLE_TEMPLATE.md` defines the canonical internal structure of an article object.
- `ARTICLE_COVER_WORKFLOW.md` defines the practical production workflow for creating an article cover.
- `BRAND/BRAND_BOOK/09_GITHUB_STRUCTURE.md` defines the Brand Book's relationship to the repository architecture.

## Canonical top-level tree

```text
VIRVOX/
├── DOCS/
├── BRAND/
│   └── BRAND_BOOK/
├── ASSETS/
├── CONTENT/
│   └── ARTICLES/
│       └── ART-XXX/
├── TEMPLATES/
├── REGISTRY/
└── SYSTEM/
```

## Canonical documentation tree

```text
DOCS/
├── 00_INDEX.md
├── 00_AI_START_HERE.md
├── AI_COMMANDS.md
├── PROJECT_MANIFEST.md
├── PROJECT_RULES.md
├── PROJECT_MAP.md
├── ARCHITECTURE.md
├── REPOSITORY_STRUCTURE.md
├── REPOSITORY_STRUCTURE_RULES.md
├── REPOSITORY_STRUCTURE_UPDATE.md
├── FILE_REFERENCE.md
├── KNOWLEDGE_BASE.md
├── DECISIONS.md
├── ROADMAP.md
├── VERSION_HISTORY.md
├── CHANGELOG.md
├── ID_RULES.md
├── CONTENT_WORKFLOW.md
├── ARTICLE_TEMPLATE.md
├── ARTICLE_COVER_WORKFLOW.md
├── ARTICLE_COVER_MASTER_SPEC.md
└── REGISTRY_STRUCTURE.md
```

## Canonical Brand Book tree

```text
BRAND/
├── README.md
└── BRAND_BOOK/
    ├── 00_INDEX.md
    ├── 01_DNA.md
    ├── 02_NAMING.md
    ├── 03_LOGO.md
    ├── 04_VISUAL_SYSTEM.md
    ├── 05_CATEGORY_SYSTEM.md
    ├── 06_COVER_SYSTEM.md
    ├── 07_ASSET_LIBRARY.md
    ├── 08_CANVA_REGISTRY.md
    ├── 09_GITHUB_STRUCTURE.md
    ├── 10_FILE_REFERENCE.md
    └── CHANGELOG.md
```

When a new Brand Book module is created, it must be added to both the Brand Book `00_INDEX.md` and `10_FILE_REFERENCE.md`, and its structural addition must be reflected here.

## Canonical article object tree

Each approved article is a package, not a single file:

```text
CONTENT/
└── ARTICLES/
    └── ART-XXX/
        ├── article.md
        ├── metadata.yaml
        ├── sources.yaml
        └── assets.yaml
```

Rules for article objects:

- `ART-XXX` is the stable article object directory and uses the stable article ID.
- `article.md` contains the editorial content.
- `metadata.yaml` contains structured metadata required by the content workflow and registry.
- `sources.yaml` records source references when applicable.
- `assets.yaml` records related asset IDs and Canva Design IDs when applicable.
- The article is registered in `REGISTRY/ARTICLE_REGISTRY.yaml`.
- The article ID is stable and must not be reused for another article.
- Additional article subdirectories or files must not be introduced by convention alone; they require an explicit architectural decision and an update to this structure document.

## Canonical registry tree

```text
REGISTRY/
├── 00_INDEX.md
├── MASTER_REGISTRY.yaml
├── ASSET_REGISTRY.yaml
├── CATEGORY_REGISTRY.yaml
├── ARTICLE_REGISTRY.yaml
├── TEMPLATE_REGISTRY.yaml
├── CANVA_REGISTRY.yaml
├── ASSET_REGISTRY/
└── CATEGORY_REGISTRY/
```

The six top-level YAML registries are authoritative registry files. The `ASSET_REGISTRY/` and `CATEGORY_REGISTRY/` directories are subordinate registry structures and must be documented before new files are added inside them.

## Directory responsibilities

### `DOCS/`
Canonical project-wide documentation, governance, architecture, rules, workflows, and historical records.

### `BRAND/`
Brand identity, Brand Book, visual standards, category presentation rules, and related brand governance.

### `ASSETS/`
Approved project assets and their organization. Asset identity and metadata are governed by the asset registry.

### `CONTENT/`
Editorial and content objects, including articles and other approved or in-process content entities.

### `TEMPLATES/`
Reusable content and production templates.

### `REGISTRY/`
Authoritative structured registries and stable object relationships.

### `SYSTEM/`
Operational commands, workflows, automation, and system-level implementation material.

## Authority and relationship model

The repository architecture follows the conceptual model defined by `DOCS/ARCHITECTURE.md` and the Brand Book repository model:

```text
PROJECT MANIFEST
      ↓
PROJECT RULES
      ↓
BRAND + SYSTEM RULES
      ↓
ARCHITECTURE + DOCUMENTATION
      ↓
REGISTRIES
      ↓
TEMPLATES
      ↓
CONTENT OBJECTS
      ↓
OUTPUTS
```

For physical repository organization:

```text
BRAND/BRAND_BOOK/  → defines brand standards
REGISTRY/          → identifies objects and relationships
TEMPLATES/         → defines reusable production structures
CONTENT/           → stores content objects
ASSETS/            → stores or references approved assets
SYSTEM/            → supports operational workflows
DOCS/              → governs and documents the project
```

Canva remains the editable design source for visual assets referenced by the Brand Book and registries.

## Required structural principles

1. `DOCS/` is the single canonical project-wide documentation directory.
2. A parallel lowercase `docs/` directory must not be created for project-wide documentation.
3. Directory names and file names must preserve the canonical case defined here.
4. Every new project-wide directory must have a documented purpose before it is added to the repository.
5. Every new canonical file must have a defined owner directory and role.
6. Structural changes must be recorded in this document in the same change set as the repository change.
7. Structural changes must also be recorded in the appropriate history or changelog document when they are meaningful architectural changes.
8. Temporary files must not be added to the canonical tree unless their temporary status and cleanup plan are explicit.
9. Files must not be duplicated across canonical directories merely to avoid updating references.
10. When a file is moved or renamed, references to the old path must be updated in the same change set whenever possible.
11. Article package structure must follow `ARTICLE_TEMPLATE.md` and this document; ad hoc article file layouts are not canonical.
12. A new directory or file must not be considered part of the canonical architecture until its purpose, owner, path, and update dependencies are documented.

## Repository audit model

The canonical structure is reconstructed and maintained from four sources:

```text
BRAND BOOK
    +
DOCS ARCHITECTURE
    +
APPROVED CONTENT / REGISTRY MODELS
    +
ACTUAL GITHUB TREE
    ↓
CANONICAL REPOSITORY STRUCTURE
```

Audits should classify differences as:

- `MATCH` — expected and present at the canonical path.
- `MISSING` — defined by the architecture but absent from the repository.
- `UNDOCUMENTED` — present in the repository but not defined by the canonical structure.
- `MISLOCATED` — present but stored at a path that conflicts with the canonical architecture.
- `DUPLICATE` — multiple paths represent the same canonical responsibility.
- `CASE_ERROR` — path differs only by capitalization from the canonical name.
- `TEMPORARY` — intentionally non-canonical material with an explicit cleanup plan.

## Source of truth

The actual GitHub repository is the physical source of truth. This document is the canonical declared structure against which the repository should be audited.

If the actual repository and this document differ, the discrepancy must be reported and resolved. The difference must not be silently ignored.
