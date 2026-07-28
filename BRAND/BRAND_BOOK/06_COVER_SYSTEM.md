# VIRVOX Cover System

**Version:** 1.0
**Status:** Foundation specification

## Purpose

The Cover System defines how VIRVOX article and content covers are assembled from approved brand components.

## Core hierarchy

```text
Cover
├── Background / visual field
├── Brand identifier (logo or monogram)
├── Category marker
├── Main title
├── Optional supporting text
└── Safe margins / composition grid
```

## Component principle

Covers should be assembled from registered components rather than recreated manually. The category is resolved through `category_id`; the corresponding approved category treatment is then selected from the asset system.

## Category relationship

Every category-based cover should reference one of the approved category IDs `CAT-001` through `CAT-010`. The master category asset is `BA-CAT-001`.

## Layout principle

The composition should preserve hierarchy, readability, safe zones, and the visual relationship between the brand identifier and category marker. Exact measurements belong to the approved master design and production templates.

## Output principle

Different publication formats may use different dimensions, but they should inherit the same underlying visual rules. Format adaptation must not change the identity of the brand system.

## Production workflow

`Article → category_id → template → approved assets → cover composition → export → registration`

## Status

This document records the system foundation. Exact final measurements and production presets should be added when the Cover Master is formally approved.
