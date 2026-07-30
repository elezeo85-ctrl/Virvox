# VIRVOX Repository Structure Update Procedure

## Purpose

This document defines the mandatory procedure for keeping `DOCS/REPOSITORY_STRUCTURE.md` synchronized with the actual GitHub repository.

The rule is simple:

> Every permanent addition, removal, move, or rename of a canonical file or directory must update the repository structure map in the same change set.

## When this procedure is required

Use this procedure whenever:

- a new directory is created;
- a new permanent file is created;
- a file or directory is moved;
- a file or directory is renamed;
- a canonical file or directory is deleted;
- the ownership or purpose of a directory changes;
- a temporary structure is promoted to canonical status.

## Standard update sequence

### Step 1 — Inspect the current structure

Read:

1. `DOCS/REPOSITORY_STRUCTURE.md`
2. `DOCS/REPOSITORY_STRUCTURE_RULES.md`
3. `DOCS/FILE_REFERENCE.md`
4. `DOCS/00_INDEX.md` when the change concerns documentation.

Then inspect the actual GitHub path being changed.

### Step 2 — Define the change

Record:

- old path, if applicable;
- new path, if applicable;
- file or directory name;
- purpose;
- parent directory;
- authority/source of truth;
- permanent or temporary status.

### Step 3 — Make the repository change

Create, move, rename, or delete the actual repository file or directory.

Do not update the structure map first and leave the physical repository inconsistent.

### Step 4 — Update the canonical structure map

Immediately update `DOCS/REPOSITORY_STRUCTURE.md` so the declared tree matches the new intended state.

For a new file or directory, add it in the correct location.

For a move or rename, replace the old path with the new path.

For a deletion, remove the obsolete path.

### Step 5 — Update navigation and references

Update as applicable:

- `DOCS/FILE_REFERENCE.md`;
- `DOCS/00_INDEX.md`;
- `DOCS/ARCHITECTURE.md`;
- registry documentation;
- internal links and path references.

Not every structural change requires every document to change. Only relevant references should be updated.

### Step 6 — Update history

For meaningful architectural or structural changes, update:

- `DOCS/VERSION_HISTORY.md`;
- `DOCS/CHANGELOG.md`.

Small routine file additions may only require the structure map and relevant navigation updates.

### Step 7 — Verify

Before considering the change complete, verify:

```text
Actual GitHub Path
        =
REPOSITORY_STRUCTURE.md
        =
FILE_REFERENCE.md / INDEX references where applicable
```

Check for:

- wrong capitalization;
- stale old paths;
- duplicate authoritative files;
- missing structure entries;
- broken internal links.

## New file checklist

When adding a new permanent file:

- [ ] Correct parent directory selected.
- [ ] Canonical case confirmed.
- [ ] Purpose defined.
- [ ] Authority defined.
- [ ] Added to `REPOSITORY_STRUCTURE.md`.
- [ ] Added to `FILE_REFERENCE.md` if relevant.
- [ ] Added to `00_INDEX.md` if it is a project-wide document.
- [ ] History/changelog updated if structurally meaningful.
- [ ] References verified.

## New directory checklist

When adding a new permanent directory:

- [ ] Purpose defined.
- [ ] Existing directory overlap checked.
- [ ] Parent directory confirmed.
- [ ] Canonical case confirmed.
- [ ] Added to `REPOSITORY_STRUCTURE.md`.
- [ ] Added to `FILE_REFERENCE.md` if relevant.
- [ ] `ARCHITECTURE.md` updated if conceptual architecture changes.
- [ ] History/changelog updated if structurally meaningful.
- [ ] References verified.

## Move / rename checklist

- [ ] New path created or established.
- [ ] References to old path identified.
- [ ] `REPOSITORY_STRUCTURE.md` updated.
- [ ] `FILE_REFERENCE.md` updated.
- [ ] `00_INDEX.md` updated if applicable.
- [ ] Internal references updated.
- [ ] Old path removed after verification.
- [ ] History/changelog updated if meaningful.

## Deletion checklist

- [ ] Obsolescence or replacement confirmed.
- [ ] References checked.
- [ ] `REPOSITORY_STRUCTURE.md` updated.
- [ ] Navigation and file references updated.
- [ ] History/changelog updated if meaningful.
- [ ] Deletion verified in the actual repository.

## AI operating rule

When an AI assistant is asked to create, move, rename, or delete a repository file or directory, it must treat `REPOSITORY_STRUCTURE.md` as a required dependency of the operation.

The assistant should not finish a structural change without either:

1. updating the canonical structure map in the same change set; or
2. explicitly reporting why the update could not be completed.

## Structural audit command concept

The project may later implement an automated audit that compares:

```text
ACTUAL GITHUB TREE
        ↓
Canonical Repository Structure
        ↓
Expected Tree
        ↓
Difference Report
```

Until such automation exists, this document defines the manual procedure.
