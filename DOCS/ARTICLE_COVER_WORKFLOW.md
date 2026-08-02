# VIRVOX Article Cover Workflow

## Purpose

This document defines the practical workflow for creating a cover for a specific VIRVOX article.

It operationalizes the existing cover, visual, category, article, content, template, and registry rules without replacing them.

## Authority and related documents

Use these documents as the governing sources for the corresponding layer:

- `BRAND/BRAND_BOOK/06_COVER_SYSTEM.md` — cover system specification and required cover components.
- `BRAND/BRAND_BOOK/04_VISUAL_SYSTEM.md` — visual system, typography, color, grid, and safe-zone rules.
- `BRAND/BRAND_BOOK/05_CATEGORY_SYSTEM.md` — category IDs, labels, and category visual treatment.
- `DOCS/ARTICLE_TEMPLATE.md` — article object structure and asset references.
- `DOCS/CONTENT_WORKFLOW.md` — general content lifecycle and approval workflow.
- `DOCS/REGISTRY_STRUCTURE.md` — registry relationships and registration requirements.
- `REGISTRY/TEMPLATE_REGISTRY.yaml` — approved template records.
- `REGISTRY/ASSET_REGISTRY.yaml` — approved asset records.
- `REGISTRY/CANVA_REGISTRY.yaml` — Canva design references.
- `REGISTRY/ARTICLE_REGISTRY.yaml` — article records and article-level metadata.

This workflow does not invent or override exact visual measurements, coordinates, fonts, colors, or other production presets that are not yet formally specified by the governing Brand Book documents.

## Cover production flow

```text
Article ID
    ↓
Article metadata
    ↓
category_id
    ↓
Category resolution
    ↓
Approved cover template
    ↓
Approved assets
    ↓
Canva master / editable design source
    ↓
Article-specific cover copy and visual content
    ↓
Category treatment
    ↓
Composition and safe-zone check
    ↓
Brand and visual-system check
    ↓
Canva Design ID registration
    ↓
Article ↔ Cover relationship update
    ↓
Registry / asset metadata update
    ↓
Final verification
    ↓
Approved cover
```

## Step 1 — Identify the article

Start with the registered or proposed article ID, for example `ART-001`.

Confirm the article record and identify the article's `category_id` before beginning visual production.

Do not create a cover without knowing which article object the cover belongs to.

## Step 2 — Resolve the category

Use the article's `category_id` to resolve:

- category ID;
- category label;
- approved category visual treatment;
- related category asset references.

The category system is authoritative for category identity and category-to-visual mapping.

## Step 3 — Select the approved cover template

Select the appropriate approved cover template from the template system and registry.

Verify:

- template ID;
- template purpose;
- supported format;
- current status;
- Canva Design ID, when applicable.

Do not create a new visual structure when an approved template already serves the required purpose.

## Step 4 — Verify approved assets

Select only approved or explicitly permitted assets for the cover.

Verify the relevant asset IDs and source information in the asset registry.

When an asset is not registered or its status is unclear, stop and resolve the asset status before treating the cover as production-ready.

## Step 5 — Open the editable Canva source

Use the registered Canva Design ID associated with the approved template or visual asset.

The editable Canva source is the authoritative editable visual source for Canva-based design work.

Create or duplicate the article-specific working design according to the project's Canva workflow. Preserve the master/template source unless the operation is explicitly intended to modify the master.

## Step 6 — Build the cover composition

The cover must use the cover-system component hierarchy:

```text
Cover
├── Background / visual field
├── Brand identifier (logo or monogram)
├── Category marker
├── Main title
├── Optional supporting text
└── Safe margins / composition grid
```

Populate the article-specific content while preserving the approved template structure and visual hierarchy.

## Step 7 — Apply category treatment

Apply the category treatment defined by the category system.

The category marker must remain visually consistent with the approved category system. Do not invent a new category color, label, badge, or visual treatment for an individual article unless the category system itself has been formally updated.

## Step 8 — Apply article content

Insert the approved article title and any permitted supporting text.

Keep the hierarchy defined by the visual system and cover system.

Do not introduce additional text elements merely to fill empty space.

## Step 9 — Check composition and safe zones

Before approval, verify:

- all required cover components are present;
- composition follows the approved template;
- text remains inside safe areas;
- the visual field does not interfere with legibility;
- logo or monogram placement follows brand rules;
- category marker is correctly placed;
- the main title has clear visual priority;
- no element is unintentionally clipped or obscured.

Exact dimensions and production presets must come from the governing template or approved Brand Book specification. Do not infer missing values.

## Step 10 — Check visual and brand compliance

Verify the finished cover against:

- `BRAND/BRAND_BOOK/04_VISUAL_SYSTEM.md`;
- `BRAND/BRAND_BOOK/05_CATEGORY_SYSTEM.md`;
- `BRAND/BRAND_BOOK/06_COVER_SYSTEM.md`;
- the selected approved template;
- approved asset records.

The cover should be treated as a composition of approved components rather than a one-off design.

## Step 11 — Register the Canva Design ID

Record the Canva Design ID for the article-specific cover when the cover has been created as an editable Canva design.

The Design ID must be connected to the appropriate asset or article-level record according to the registry structure.

## Step 12 — Link the cover to the article

Update the article's asset references so that the relationship between the article and its cover is explicit.

Where the article object uses `assets.yaml`, include the relevant asset ID and Canva Design ID according to the established metadata format.

## Step 13 — Update registries

Update the appropriate registry records when the cover becomes a meaningful registered project object.

At minimum, preserve the relationships among:

```text
Article ID
    ↕
Cover / Asset ID
    ↕
Template ID
    ↕
Canva Design ID
    ↕
Category ID
```

Do not create conflicting duplicate IDs or competing authoritative records.

## Step 14 — Final verification

Before marking the cover approved, verify:

- article ID is correct;
- category ID is correct;
- template is approved and current;
- assets are approved or explicitly permitted;
- visual hierarchy is correct;
- category treatment is correct;
- brand rules are satisfied;
- Canva Design ID is recorded;
- article-to-cover relationship is recorded;
- registry references are consistent;
- final output has been visually checked.

## Status model

Use the project's existing status vocabulary where available. Do not invent a conflicting status system specifically for covers.

A cover should not be treated as production-ready merely because a Canva design exists. It must also satisfy the relevant visual, category, template, asset, and registration requirements.

## Important limitation

This workflow defines the operational sequence, but it does not establish exact visual specifications that are not currently present in the governing Brand Book or approved template documentation.

If the required template, Cover Master, dimensions, typography, colors, safe-zone values, or other production presets are missing or not approved, the correct action is to identify the missing specification rather than invent it.
