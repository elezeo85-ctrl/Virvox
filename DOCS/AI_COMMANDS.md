# AI COMMANDS

## Purpose

Canonical reference for AI-facing commands used to operate the VIRVOX content and registry system.

## Article commands

- `ARTICLE FIND` — search the article registry by ID, title, or keyword.
- `MC.CREATE ARTICLE` — create a new article object using the canonical article structure and assign a unique article ID.
- `MC.UPDATE ARTICLE` — update an existing article while preserving its ID and registry relationships.
- `MC.RENDER ARTICLE` — prepare an approved article for rendering using the applicable template and brand rules.

## Registry commands

- `REGISTRY FIND` — locate an object in the appropriate registry.
- `REGISTRY UPDATE` — update an existing registry record without creating duplicate identities.
- `REGISTRY VERIFY` — validate registry consistency, required fields, IDs, and relationships.

## Design commands

- `DESIGN FIND` — locate a registered visual design or Canva asset.
- `DESIGN UPDATE` — update metadata or registry information for an existing design.
- `DESIGN EXPORT` — prepare an approved design for export according to the applicable output rules.

## Command principles

1. Check the canonical documentation and relevant registry before creating or modifying an object.
2. Never reuse an existing ID for a different object.
3. Preserve traceability between articles, assets, templates, categories, and Canva designs.
4. Registry data remains canonical in the authoritative registry files; Markdown documents describe structure and usage.
5. Any command that changes project state must leave the relevant registry and documentation consistent.
