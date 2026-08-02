# AI START HERE

## Purpose

This document is the operational entry point for AI working with the VIRVOX project documentation.

The root file `AI_START_HERE.md` must be opened first.

## Required reading order

1. `AI_START_HERE.md`
2. `DOCS/REPOSITORY_STRUCTURE.md`
3. `DOCS/REPOSITORY_STRUCTURE_RULES.md`
4. `DOCS/REPOSITORY_STRUCTURE_UPDATE.md`
5. `DOCS/00_INDEX.md`
6. `DOCS/PROJECT_MANIFEST.md`
7. `DOCS/PROJECT_RULES.md`
8. `DOCS/ARCHITECTURE.md`
9. `DOCS/FILE_REFERENCE.md`

## Core rules

- `DOCS/REPOSITORY_STRUCTURE.md` is the canonical source of repository structure.
- `DOCS/REPOSITORY_STRUCTURE_RULES.md` defines mandatory structural governance rules.
- `DOCS/REPOSITORY_STRUCTURE_UPDATE.md` defines the procedure for synchronizing structural changes with the canonical structure.
- Do not rely on automatic recursive scanning of GitHub.
- Treat GitHub as the authoritative source for documentation and registries.
- Structural changes must be documented before or together with repository changes.

## Registry lookup rules

When working with entities that have canonical registries, AI must consult the relevant registry first and must not invent or infer registered values when the registry is available.

### Article categories

The canonical article category registry is:

`REGISTRY/CATEGORY_REGISTRY.yaml`

**Mandatory rule:** when creating, indexing, editing, or re-indexing any article, AI must consult `REGISTRY/CATEGORY_REGISTRY.yaml` and select the most appropriate category from the registered categories only. A new category must not be created automatically. If no registered category is suitable, AI must report that explicitly instead of inventing a replacement.

### Article registry

The article registry is:

`REGISTRY/ARTICLE_REGISTRY.yaml`

When creating or editing an article, AI must check this registry and keep the article record consistent with it.

### ART-001

For article `ART-001`, the selected category is `CAT-002 — «Взгляд женщины»`, based on `REGISTRY/CATEGORY_REGISTRY.yaml`.

### Article workflow

When the user asks to create or edit an article:

1. Determine the repository structure from `DOCS/REPOSITORY_STRUCTURE.md`.
2. Check `DOCS/REPOSITORY_STRUCTURE_RULES.md` and related instructions.
3. Check `REGISTRY/ARTICLE_REGISTRY.yaml`.
4. Check `REGISTRY/CATEGORY_REGISTRY.yaml` and use only registered categories.
5. Check other relevant registries when applicable.
6. Only then create or edit the article materials.
