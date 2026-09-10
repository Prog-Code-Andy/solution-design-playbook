# Prompt 010 — Initialize Project

Prerequisites: project root is known; no conflicting `docs/project-design/` control plane exists.

1. Read `01-governance/project-state-schema.md` and every schema template.
2. Ask only for unresolved essentials: project title, requirements location if known, and non-default output/playbook paths.
3. Create `docs/project-design/README.md` and the six YAML files from templates.
4. Generate a stable project ID proposal, set mode to `undecided`, create MAIN, and keep implementation authorization false.
5. Record generated values as draft; do not invent stakeholders, constraints, requirements, or subscopes.
6. Validate YAML and summarize created paths.

Expected stop: `next_prompt` is `020-register-requirements`; no source code changed.

