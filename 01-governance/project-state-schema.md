# Project State Schema

The control plane consists of six YAML files in `docs/project-design/`:

- `project.yaml`: stable project configuration.
- `workflow-state.yaml`: active scope, stage, artifact, authorization, and next prompt.
- `scope-registry.yaml`: MAIN and approved/proposed subscopes.
- `artifact-index.yaml`: identity, path, type, scope, version, and status for every artifact.
- `requirements-source-registry.yaml`: authoritative source metadata.
- `requirements-index.yaml`: requirement-to-scope and traceability metadata.

The model maintains these files after explicit user decisions. Full requirements stay in their authoritative source or an approved Markdown snapshot; YAML stores metadata and references.

Before any transition, validate required keys, unique IDs, referenced paths, legal status transitions, active-scope existence, pending gate, and consistency between YAML and Markdown.

