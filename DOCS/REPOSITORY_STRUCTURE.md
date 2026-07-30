# VIRVOX Canonical Repository Structure

## Purpose

This document defines the canonical physical structure of the VIRVOX repository. It is the reference tree used to determine where project files and directories belong.

The structure is intentionally maintained separately from the conceptual architecture in `ARCHITECTURE.md`.

- `ARCHITECTURE.md` explains **how the system is organized conceptually**.
- `REPOSITORY_STRUCTURE.md` defines **where files and directories physically belong**.
- `REPOSITORY_STRUCTURE_RULES.md` defines **the rules for creating, moving, renaming, or deleting structural elements**.
- `REPOSITORY_STRUCTURE_UPDATE.md` defines **the required procedure for updating this document whenever the repository changes**.

## Canonical top-level tree

```text
VIRVOX/
├── DOCS/
├── BRAND/
│   └── BRAND_BOOK/
├── ASSETS/
├── CONTENT/
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
└── REGISTRY_STRUCTURE.md
```

## Canonical registry tree

```text
REGISTRY/
├── MASTER_REGISTRY.yaml
├── ASSET_REGISTRY.yaml
├── CATEGORY_REGISTRY.yaml
├── ARTICLE_REGISTRY.yaml
├── TEMPLATE_REGISTRY.yaml
└── CANVA_REGISTRY.yaml
```

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

## Source of truth

The actual GitHub repository is the physical source of truth. This document is the canonical declared structure against which the repository should be audited.

If the actual repository and this document differ, the discrepancy must be reported and resolved. The difference must not be silently ignored.
