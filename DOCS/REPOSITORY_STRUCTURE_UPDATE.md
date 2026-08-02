# VIRVOX Repository Structure Update Procedure

## AI initialization

1. Open `AI_START_HERE.md` in the repository root.
2. Read `DOCS/REPOSITORY_STRUCTURE.md`.
3. Use the documented tree as the canonical map.
4. Do not rely on recursive GitHub scanning.
5. Produce an audit before structural changes.

## Structural update sequence

```text
Change request
      ↓
Update REPOSITORY_STRUCTURE.md
      ↓
Update FILE_REFERENCE.md
      ↓
Update indexes and changelog
      ↓
Apply repository changes
      ↓
Verify consistency
```

## Structural completeness

A structural change is complete only when the physical repository and its canonical documentation are synchronized.

The minimum completion requirement is:

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

## AI operational rule

For any operation that creates, moves, renames, or deletes a canonical file or directory, `DOCS/REPOSITORY_STRUCTURE.md` is a mandatory dependency of the operation.

The AI must not treat a structural change as complete until the canonical structure map has been updated or an explicit reason has been documented for why the update cannot yet be performed.

The canonical structure document is the source of truth for the intended repository tree. Automatic recursive scanning of GitHub is not itself a source of truth; repository contents should be checked against the canonical structure when performing an audit or validation.

## Structural audit

After a structural change, verify the physical repository against `DOCS/REPOSITORY_STRUCTURE.md` and check for:

- missing required directories;
- unexpected directories;
- missing required files;
- unexpected canonical files;
- incorrect capitalization;
- duplicate authoritative locations;
- stale or broken internal references;
- obsolete paths remaining after moves or renames.

Until automated structural auditing is available and verified, this audit remains a manual procedure.
