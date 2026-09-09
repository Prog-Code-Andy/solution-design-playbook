# Project Design

This directory contains the canonical Markdown design artifacts and YAML workflow state for this project.

## Resume

1. Read `../../solution-design-playbook/README.md` (adjust only when `project.yaml` configures another playbook root).
2. Read `workflow-state.yaml`.
3. Validate the active scope, pending approval gate, and `next_prompt`.
4. Run only that prompt or an explicitly requested read-only review.

## Control files

- `project.yaml`
- `workflow-state.yaml`
- `scope-registry.yaml`
- `artifact-index.yaml`
- `requirements-source-registry.yaml`
- `requirements-index.yaml`

Do not manually approve artifacts by editing YAML. Approval is recorded only after an explicit user message.

