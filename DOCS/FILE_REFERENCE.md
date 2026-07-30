# VIRVOX File Reference

This document is the passport for the project documentation and top-level system structure.

## Top-level directories

| Path | Purpose | Authority / relationship |
|---|---|---|
| `BRAND/` | Brand identity and standards | Brand source documentation |
| `BRAND/BRAND_BOOK/` | Structured Brand Book | Defines approved brand rules |
| `ASSETS/` | Asset organization | Uses asset registry IDs |
| `CONTENT/` | Editorial and content objects | Uses categories and templates |
| `TEMPLATES/` | Reusable production structures | Must reference approved standards |
| `REGISTRY/` | Authoritative object indexes | Stable IDs and metadata |
| `SYSTEM/` | Commands, workflows, and automation | Operational layer |
| `DOCS/` | Project-wide documentation and governance | Canonical GitHub source of truth |

## Canonical documentation files

| Path | Purpose | Authority / relationship |
|---|---|---|
| `DOCS/00_INDEX.md` | Documentation entry point | Canonical navigation index |
| `DOCS/00_AI_START_HERE.md` | AI operational entry point | Required reading order for AI work |
| `DOCS/PROJECT_MANIFEST.md` | Project constitution | Foundational principles |
| `DOCS/PROJECT_RULES.md` | Mandatory operating rules | Governance |
| `DOCS/PROJECT_MAP.md` | Ecosystem map | Cross-system relationships |
| `DOCS/ARCHITECTURE.md` | Architecture | Hierarchy and dependencies |
| `DOCS/FILE_REFERENCE.md` | File passport | This document |
| `DOCS/KNOWLEDGE_BASE.md` | Durable knowledge | Lessons and standards |
| `DOCS/DECISIONS.md` | Decision log | Important approved decisions |
| `DOCS/ROADMAP.md` | Development plan | Future work |
| `DOCS/VERSION_HISTORY.md` | Major version history | Historical record |
| `DOCS/CHANGELOG.md` | Change log | Chronological updates |

## Operational documentation

| Path | Purpose | Authority / relationship |
|---|---|---|
| `DOCS/AI_COMMANDS.md` | Canonical AI command reference | Defines approved command vocabulary |
| `DOCS/ID_RULES.md` | Stable identifier rules | Defines ID creation and preservation rules |
| `DOCS/CONTENT_WORKFLOW.md` | Content lifecycle | Defines creation, approval, registration, and rendering flow |
| `DOCS/ARTICLE_TEMPLATE.md` | Canonical article structure | Defines article object and editorial hierarchy |
| `DOCS/REGISTRY_STRUCTURE.md` | Registry architecture | Defines registry relationships and data responsibilities |

## Registry files

| Path | Purpose |
|---|---|
| `REGISTRY/MASTER_REGISTRY.yaml` | Master registry and registry-level references |
| `REGISTRY/ASSET_REGISTRY.yaml` | Asset IDs and asset metadata |
| `REGISTRY/CATEGORY_REGISTRY.yaml` | Category IDs and category metadata |
| `REGISTRY/ARTICLE_REGISTRY.yaml` | Article IDs and article metadata |
| `REGISTRY/TEMPLATE_REGISTRY.yaml` | Template IDs and template metadata |
| `REGISTRY/CANVA_REGISTRY.yaml` | Canva design IDs and editable design references |

## Reference metadata standard

Where appropriate, project objects should expose:

- Internal ID
- Name
- Type
- Status
- Version
- Source system
- Canva Design ID, if applicable
- GitHub path
- Related registry
- Related objects
- Last meaningful change

## Current known core assets

- `BA-CAT-001` — VIRVOX Category Master; Canva Design ID `DAHQDbNq37k`.
- `BA-LOGO-001` — VIRVOX Monogram VX; Canva Design ID `DAHQGdFhl5k`; visual status requires confirmation before production use.
- `BA-LOGO-002` — VIRVOX Full Logo with Descriptor; Canva Design ID `DAHQIOXVfks`.
