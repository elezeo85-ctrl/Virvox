# VIRVOX Project Manifest

**Document status:** Approved baseline
**System version:** v1.0

## Purpose

VIRVOX is a structured brand and content ecosystem. Its documentation, assets, templates, registries, and workflows are maintained as a coherent system rather than as isolated files.

## Foundational principles

1. **Preservation:** approved knowledge and assets are never silently discarded.
2. **Traceability:** important objects receive stable internal IDs and are linked to their source files.
3. **Versioning:** meaningful changes create a new version or a documented change in Git history.
4. **Separation of concerns:** GitHub stores project knowledge and structured metadata; Canva stores editable visual designs.
5. **Single source of truth:** each class of information has a clearly defined authoritative location.
6. **Consistency:** brand, categories, assets, templates, and content must remain mutually compatible.
7. **Recoverability:** project decisions and previous states should remain reconstructable from history.

## Source-of-truth model

| Domain | Authoritative source |
|---|---|
| Project documentation | GitHub |
| Architecture and rules | GitHub |
| Registries and internal IDs | GitHub |
| Editable visual design | Canva |
| Published content | Registered project content |

## Governance

The project is governed through documented decisions, registries, version history, and change logs. New standards should be approved before becoming mandatory project rules.

## Core identity system

The VIRVOX visual system includes approved logos, category assets, typography, color rules, cover rules, and related design components. These are documented in the Brand Book and linked to the asset registries.

## Category system

VIRVOX has ten approved content categories. Each category has a stable internal ID (`CAT-001` through `CAT-010`) and is associated with the master category asset `BA-CAT-001`.

## Change policy

When a rule, asset, or structure changes, the change should be reflected in the relevant documentation and, when appropriate, in `DECISIONS.md`, `VERSION_HISTORY.md`, and `CHANGELOG.md`.
