# VIRVOX Repository Structure Rules

## Purpose

This document defines the mandatory rules for maintaining the physical repository structure.

The canonical tree is defined in `DOCS/REPOSITORY_STRUCTURE.md`.
The update procedure is defined in `DOCS/REPOSITORY_STRUCTURE_UPDATE.md`.

## 1. Canonical naming and case

- Use the exact directory and file names defined by the canonical repository structure.
- Case is significant and must be preserved.
- `DOCS/` is canonical. Do not create a parallel lowercase `docs/` directory for project-wide documentation.
- Do not create alternative spellings or aliases of canonical directories.

## 2. New directories

Before creating a new directory:

1. Define its purpose.
2. Identify its parent directory.
3. Confirm that an existing canonical directory does not already serve the same purpose.
4. Determine whether it is a permanent or temporary directory.
5. Add it to `REPOSITORY_STRUCTURE.md` in the same change set.
6. Add or update its description in `FILE_REFERENCE.md` when appropriate.
7. Update `ARCHITECTURE.md` if the directory changes the conceptual architecture.

## 3. New files

Before creating a new canonical file:

1. Define its role and authority.
2. Place it in the correct canonical directory.
3. Use the canonical naming convention.
4. Add it to `REPOSITORY_STRUCTURE.md`.
5. Add it to `FILE_REFERENCE.md` when it is a meaningful project file.
6. Add it to `DOCS/00_INDEX.md` if it is a navigable project-wide document.
7. Update relevant history or changelog records for meaningful structural changes.

## 4. Moving or renaming

When moving or renaming a file or directory:

1. Update the canonical structure map.
2. Update all known references to the old path.
3. Update `FILE_REFERENCE.md`.
4. Update `DOCS/00_INDEX.md` when applicable.
5. Record the structural change in history or changelog when meaningful.
6. Remove the obsolete path after the replacement is verified.

## 5. Deleting

Before deleting a canonical file or directory:

1. Confirm that it is obsolete or intentionally replaced.
2. Check for references to the path.
3. Update the canonical structure map.
4. Update file references and indexes.
5. Record the deletion when it is architecturally meaningful.

## 6. Temporary files

Temporary files must:

- be clearly named as temporary or draft material;
- have a documented purpose;
- have a cleanup or promotion plan;
- never become accidental sources of truth.

Temporary files must be removed or formally promoted before a structural migration is considered complete.

## 7. Duplicate structures

Do not maintain two directories with the same conceptual authority.

Examples of prohibited parallel structures include:

- `DOCS/` and `docs/` both serving as project-wide documentation sources;
- duplicate registries containing conflicting authoritative IDs;
- duplicate canonical templates in multiple locations without an explicit ownership rule.

If duplication is required for technical reasons, one location must be explicitly designated as authoritative.

## 8. Authority and inheritance

```text
PROJECT MANIFEST
        ↓
PROJECT RULES
        ↓
BRAND / SYSTEM RULES
        ↓
ARCHITECTURE + REPOSITORY STRUCTURE
        ↓
REGISTRIES
        ↓
TEMPLATES
        ↓
CONTENT OBJECTS
        ↓
OUTPUTS
```

A lower-level file must not silently redefine the authority of a higher-level structural rule.

## 9. Audit requirement

After a structural change, the repository should be checked against `REPOSITORY_STRUCTURE.md` for:

- missing required directories;
- unexpected directories;
- missing required files;
- unexpected canonical files;
- incorrect capitalization;
- duplicate authoritative locations;
- broken references caused by moves or renames.

## 10. Rule of structural completeness

A repository structure change is complete only when:

```text
Physical Repository Change
        +
Canonical Structure Update
        +
Reference / Index Update
        +
History / Changelog Update (when meaningful)
        =
Complete Structural Change
```

## Additional AI rules

- The canonical source of structure is `DOCS/REPOSITORY_STRUCTURE.md`.
- Automatic recursive scanning of GitHub is not a source of truth.
- The root file `AI_START_HERE.md` is the mandatory entry point for AI systems.
- Structural changes must update documentation and repository in the same change set.

See `DOCS/REPOSITORY_STRUCTURE_UPDATE.md` for the update sequence.
