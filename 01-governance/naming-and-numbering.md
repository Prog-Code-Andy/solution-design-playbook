# Naming and Numbering

- Number top-level playbook directories with two digits.
- Number workflow prompts in increments of ten (`000`, `010`, `020`) so intermediate prompts can be inserted.
- Use stable uppercase artifact IDs: `DISC-MAIN-001`, `EDR-001`, `API-001`, `SDD-MAIN-001`, `TDD-ENTRA-001`, `PHASE-00`, `TASK-001`, `REM-001`.
- Treat `project_id`, `scope_id`, `requirement_id`, and `artifact_id` as distinct identifiers.
- Preserve source-defined requirement identifiers. Generate `LOCAL-REQ-NNN` only when the source provides none.
- Use lowercase kebab-case for paths and filenames after the identifier.
- Never renumber an accepted or published artifact.

