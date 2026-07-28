# VIRVOX Architecture

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
Contains project-wide knowledge, architecture, decisions, rules, roadmap, and history.

## Hierarchy principle

Higher-level standards define constraints for lower-level objects. A template may reference an approved asset; a content object may reference a template and category; a published output is generated from those approved dependencies.

```text
PROJECT MANIFEST
      ↓
PROJECT RULES
      ↓
BRAND BOOK / SYSTEM RULES
      ↓
REGISTRIES
      ↓
TEMPLATES
      ↓
CONTENT
      ↓
OUTPUTS
```

## ID principle

Stable IDs identify objects independently of their display names. Display names can change under controlled versioning while IDs remain stable whenever the underlying object remains the same.

## Version principle

Changes are recorded in Git history. Major changes should also be reflected in the project version documents and relevant registries.
