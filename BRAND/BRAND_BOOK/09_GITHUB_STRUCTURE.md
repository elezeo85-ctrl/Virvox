# VIRVOX GitHub Structure

## Purpose

This document explains how the Brand Book relates to the broader VIRVOX repository.

```text
VIRVOX/
├── BRAND/
│   └── BRAND_BOOK/
├── ASSETS/
├── CONTENT/
├── TEMPLATES/
├── REGISTRY/
├── SYSTEM/
└── DOCS/
```

## Relationship

- `BRAND/BRAND_BOOK/` defines brand standards.
- `ASSETS/` organizes registered assets.
- `REGISTRY/` provides authoritative object indexes and IDs.
- `TEMPLATES/` applies approved standards to repeatable production formats.
- `CONTENT/` stores content objects that use categories and templates.
- `SYSTEM/` contains operational commands and workflows.
- `DOCS/` contains project-wide governance and knowledge.

## Authority model

```text
DOCS / PROJECT RULES
        ↓
BRAND BOOK
        ↓
REGISTRIES
        ↓
TEMPLATES
        ↓
CONTENT
```

Canva remains the editable design source for visual assets referenced by the Brand Book and registries.

## Rule

Brand standards should be defined once in the Brand Book and referenced by other systems. Avoid duplicating authoritative definitions across unrelated files.
