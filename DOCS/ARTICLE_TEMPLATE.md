# ARTICLE TEMPLATE

## Purpose

Canonical structure for VIRVOX articles. This document defines the content model used inside an article object and the minimum editorial structure required for rendering.

## Article object

Each approved article is represented as:

```text
CONTENT/ARTICLES/ART-XXX/
├── article.md
├── metadata.yaml
├── sources.yaml
└── assets.yaml
```

The article is indexed by `REGISTRY/ARTICLE_REGISTRY.yaml`.

## Editorial structure

The main `article.md` should contain, as applicable:

1. Title
2. Short description or lead
3. Main text
4. Main idea / key takeaway
5. Question or engagement prompt for the reader

The exact section structure may be extended when required by the approved content format or template.

## Metadata

`metadata.yaml` should contain the structured information required by the registry and content workflow, including the stable article ID and applicable category, status, dates, and relationships.

## Sources

`sources.yaml` records source references used to create or substantiate the article when applicable.

## Assets

`assets.yaml` records related visual and media assets, including relevant asset IDs and Canva Design IDs where applicable.

## Rendering

Approved article content is rendered through the applicable template and must follow the brand rules and output requirements. Rendering does not create a new article identity.

## Registration rule

An approved article must be registered in `ARTICLE_REGISTRY.yaml`. The article ID is stable and must not be reused for another article.
