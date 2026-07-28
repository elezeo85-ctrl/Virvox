# VIRVOX Category System v1.0

**Status:** Approved
**Master Asset:** `BA-CAT-001`

## Official categories

| ID | Display name | Status |
|---|---|---|
| `CAT-001` | Разбор мифов | Approved |
| `CAT-002` | Взгляд женщины | Approved |
| `CAT-003` | Мужской взгляд | Approved |
| `CAT-004` | Из жизни | Approved |
| `CAT-005` | Практика | Approved |
| `CAT-006` | Исследование | Approved |
| `CAT-007` | Размышление | Approved |
| `CAT-008` | Диалог | Approved |
| `CAT-009` | Ответы на вопросы | Approved |
| `CAT-010` | Мудрые мысли | Approved |

## Usage rule

The category ID is the stable machine-readable reference. The display name is the human-facing label.

A content object should reference `category_id`, not hard-code the category definition in multiple places.

Example:

```yaml
article_id: ART-001
category_id: CAT-003
```

The production system resolves `CAT-003` to the approved display name and the corresponding category visual treatment.

## Master asset relationship

`BA-CAT-001` is the master category design asset. Individual category outputs should remain visually consistent with the approved master system.

## Change control

Changing a category name or visual treatment requires an update to the Category Registry and, where relevant, the Brand Book changelog. IDs should remain stable unless the category itself is fundamentally replaced.
