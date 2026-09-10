# Prompt 025 — Materialize Requirements Foundation

Use this bridge only when Windsurf Plan Mode has produced a reviewed implementation plan for prompts 010 and 020 but has not yet created the project-design files. This prompt authorizes planning-artifact writes, not project implementation.

## Authorization

- Allowed writes: `docs/project-design/**` only.
- Project source code, tests, runtime configuration, infrastructure, deployment, and unrelated documentation: prohibited.
- `implementation_allowed` must remain `false`.
- `planning_artifact_writes_allowed` may be `true` only for the bounded write, then returns to `false` at the stop.
- No requirements, discovery, decision, design, roadmap, phase, or task approval is included.

## Preconditions

1. Read the playbook root README, `01-governance/`, prompts 010 and 020, and the complete reviewed Windsurf plan.
2. Confirm that the plan contains only project initialization and requirements registration/analysis artifacts.
3. Inventory existing `docs/project-design/**` files and preserve them. Stop on conflicting initialized state rather than overwriting it.
4. Confirm the user explicitly authorized materializing the reviewed 010/020 plan.

## Actions

1. Create or update the six YAML control files and project-design README defined by prompt 010.
2. Create only the requirements intake, source register, requirements analysis draft, and related indexes defined by prompt 020.
3. Preserve source-defined requirement IDs and source references. Do not invent inaccessible requirements.
4. Keep Requirements Baseline status `Draft` or `Proposed`; do not mark it Approved.
5. Set `active_scope: MAIN`, `active_stage: main_discovery`, and `next_prompt: 030-main-discovery`.
6. Set `authorization.mode: discussion_only`, `implementation_allowed: false`, and `planning_artifact_writes_allowed: false` at completion.
7. Validate YAML syntax, unique IDs, referenced paths, Markdown/YAML status consistency, and the exact changed-file boundary.
8. Produce a concise Prompt 010/020 materialization status report under `docs/project-design/12-reports/` only if the reviewed plan already requires that report.

## Stop condition

Report created/updated files, validation results, unresolved requirements questions, and the exact next prompt. Stop. Do not begin prompt 030 or switch to project implementation.

