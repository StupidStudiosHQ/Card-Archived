# CardArchived Repository Architecture

CardArchived separates source evidence, canonical object records, public presentation, and reusable system definitions.

## Structure

- `records/SL-######/` — permanent home for each archived physical object.
- `assets/SL-######/` — reference photography, fingerprint maps, measurement diagrams and other evidence assets when migrated into GitHub.
- `schemas/` — machine-readable definitions governing archive records.
- `templates/` — reusable starting records for new submissions.
- `index/records.json` — master registry of archive IDs and permanent paths.
- `docs/` — system documentation and methodology.

## Record principles

1. An archive ID identifies a specific archived object/specimen, not merely a card design.
2. Permanent archive paths must not be recycled.
3. Source-derived claims must remain distinguishable from later research.
4. Unknown creative attribution is recorded as `Attribution Under Research`; attribution is never invented.
5. Fingerprint definitions are frozen before blind identity comparison when a record is marked locked.
6. Holder, grade and certification may be recorded as context but are not specimen fingerprint evidence.
7. Shared printed design alone cannot establish specimen identity.
8. Photography limitations and evidence quality must be retained.
9. Public presentation may evolve without silently changing the underlying locked specimen evidence.
10. Version changes must be explicit.

## New-record workflow

1. Assign next permanent `SL-######` identifier.
2. Copy `templates/archive-record.json` into the new record directory.
3. Preserve submitted source evidence.
4. Populate object identity and contextual metadata.
5. Research creative attribution; unresolved attribution remains `Attribution Under Research`.
6. Establish image-derived fingerprint features and evidence limitations.
7. Freeze fingerprint definitions before any blind comparison.
8. Add story, art, subject, notables, significance, provenance, market and research layers without altering frozen evidence.
9. Add the record to `index/records.json`.
10. Publish the collector-facing page at its permanent archive route.
