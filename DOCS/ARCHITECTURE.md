# VIRVOX Project Architecture

## Purpose

This document defines the logical architecture of the VIRVOX project and the relationship between documentation, rules, brand governance, registries, templates, content objects, and outputs.

## Top-level structure

```text
VIRVOX/
├── BRAND/
├── ASSETS/
├── CONTENT/
├── TEMPLATES/
├── REGISTRY/
├── SYSTEM/
└── DOCS/
```

## Architectural layers

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

## Responsibilities

### BRAND

Defines the brand identity, Brand Book, visual rules, category system, and design standards.

### ASSETS

Contains or references approved visual and production assets.

### CONTENT

Contains articles, stories, reels, ideas, drafts, and other editorial objects.

### TEMPLATES

Contains reusable structures for articles, covers, stories, and reels.

### REGISTRY

Provides authoritative indexes for assets, categories, articles, templates, and Canva IDs.

### SYSTEM

Contains commands, workflows, automation, and operational rules.

### DOCS

`DOCS/` is the canonical project-wide documentation and governance layer. It contains project knowledge, architecture, decisions, rules, roadmaps, history, AI entry points, command references, ID rules, content workflows, article structure, and registry architecture.

Documentation describes and governs the system; it does not replace authoritative registry data, content objects, or editable Canva designs.

## Documentation versus production flow

`DOCS/` is a governance and knowledge layer. It should not be interpreted as a sequential production stage.

The production flow is:

```text
Approved Rules
      ↓
Registry IDs / Relationships
      ↓
Template Selection
      ↓
Content Object Creation
      ↓
Approval
      ↓
Rendering
      ↓
Output
```

## Source-of-truth model

- **GitHub** — authoritative source for project documentation, rules, registries, structured metadata, and version history.
- **Canva** — authoritative source for editable visual design files.
- **Brand Book** — authoritative source for visual identity and brand constraints.
- **Registries** — authoritative source for stable IDs and cross-object relationships.
- **Content objects** — authoritative source for approved editorial content.
- **Templates** — authoritative source for reusable rendering structures.

## Hierarchy principle

Higher-level standards define constraints for lower-level objects. Rules govern objects; registries identify objects and their relationships; templates define reusable rendering structures; content objects hold approved editorial material; outputs are generated from approved dependencies.

```text
PROJECT MANIFEST
        ↓
PROJECT RULES
        ↓
BRAND / SYSTEM RULES
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

No layer should silently override another layer's authority.

## ID principle

Stable IDs identify objects independently of their display names. Display names can change under controlled versioning while IDs remain stable whenever the underlying object remains the same.

## Version principle

Changes are recorded in Git history. Major changes should also be reflected in the project version documents, changelog, and relevant registries.
