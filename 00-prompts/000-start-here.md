# Prompt 000 — Start Here

Operate in planning/discussion mode. Do not implement project deliverables.

1. Locate and read the playbook root `README.md` and all files in `01-governance/` except unused YAML examples.
2. Resolve the project root and default output root `docs/project-design/` without changing existing source layout.
3. If no project control files exist, report that initialization is required and continue with prompt 010 only after the user confirms the project title and requirements-source location when known.
4. If control files exist, validate their YAML structure, referenced scopes/artifacts, Markdown status consistency, and pending gate.
5. Report the project ID, mode, active scope, active stage, authorization, blockers, and legal next prompt.
6. Never infer approval or repair inconsistent state silently.

Expected stop: the user sees the one legal next action; no implementation has begun.

