# VIRVOX Decision Log

## D-001 — GitHub as project knowledge source of truth

**Status:** Approved

GitHub is the authoritative location for documentation, registries, architecture, rules, and version history.

## D-002 — Canva as editable visual source of truth

**Status:** Approved

Canva remains the authoritative location for editable visual design files. GitHub stores their internal IDs, Canva Design IDs, descriptions, relationships, and status metadata.

## D-003 — Stable internal IDs

**Status:** Approved

Assets, categories, articles, templates, and other registered objects receive stable IDs. Display names do not replace IDs.

## D-004 — Ten-category VIRVOX system

**Status:** Approved

The official category system contains ten categories, including `Из жизни` and `Мудрые мысли`. The categories are represented by `CAT-001` through `CAT-010` and connected to master asset `BA-CAT-001`.

## D-005 — Modular Brand Book

**Status:** Approved

The Brand Book is maintained as a collection of focused documents rather than one monolithic file, with an index providing navigation.

## D-006 — DOCS knowledge system

**Status:** Approved

A dedicated `DOCS/` directory is part of the project architecture and contains project-wide documentation, knowledge, decisions, roadmap, and history.

## D-007 — Preserve history

**Status:** Approved

Approved knowledge and assets are not silently deleted. Changes are versioned and documented so prior states remain recoverable through Git history.

## D-008 — YAML as canonical registry format

**Status:** Approved

All authoritative VIRVOX registries use YAML (`.yaml`) as their canonical structured data format. Markdown files in `REGISTRY/` are reserved for navigation, documentation, instructions, and explanations. Long-form article text is stored separately in article packages under `CONTENT/ARTICLES/ART-XXX/article.md` and is referenced by `ARTICLE_REGISTRY.yaml`.
