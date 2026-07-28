# VIRVOX File Reference

This document is the passport for the project documentation and top-level system structure.

| Path | Purpose | Authority / relationship |
|---|---|---|
| `BRAND/` | Brand identity and standards | Brand source documentation |
| `BRAND/BRAND_BOOK/` | Structured Brand Book | Defines approved brand rules |
| `ASSETS/` | Asset organization | Uses asset registry IDs |
| `CONTENT/` | Editorial and content objects | Uses categories and templates |
| `TEMPLATES/` | Reusable production structures | Must reference approved standards |
| `REGISTRY/` | Authoritative object indexes | Stable IDs and metadata |
| `SYSTEM/` | Commands and workflows | Operational layer |
| `DOCS/` | Project-wide knowledge | GitHub source of truth |
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
