# 00 — Numbered Workflow Prompts

These prompts are model-independent entry points. Numbers express the normal lifecycle, not authority. Always validate `docs/project-design/workflow-state.yaml`; loops and remediation may make the legal next prompt non-numeric.

## Usage

```text
Read solution-design-playbook/README.md and run 00-prompts/000-start-here.md.
```

Each prompt must read governance, relevant templates, and current state; distinguish facts from assumptions; update only authorized artifacts; show required approvals; and stop before implementation unless a separately approved execution phase explicitly authorizes it.

| Prompt | Purpose |
|---:|---|
| 000 | Resolve paths and determine new/existing workflow |
| 010 | Initialize project-design control files |
| 020 | Register and inspect requirements sources |
| 025 | Materialize an approved Windsurf 010/020 planning foundation |
| 030 | Conduct Main Discovery |
| 035 | Recover the required interactive Main Discovery when prompt 030 skipped user discussion |
| 040 | Review Main Discovery |
| 045 | Review and approve the Requirements Baseline |
| 050 | Propose and approve scope decomposition |
| 060 | Activate a registered scope |
| 070 | Conduct scoped discovery |
| 080 | Draft necessary EDRs |
| 090 | Review and record decision acceptance |
| 100 | Define and review contracts |
| 110 | Create Main Solution Design/baseline |
| 120 | Create a component or integration TDD |
| 130 | Review the integrated design |
| 140 | Build the roadmap |
| 150 | Build phase specifications |
| 160 | Build task packages and traceability |
| 170 | Review the complete execution package |
| 180 | Review delivered work and evidence |
| 190 | Classify and plan remediation |

Prompts `025`, `035`, and `045` are intentional inserted gates. Prompt 025 is a Windsurf Plan-to-files bridge and is skipped when prompt 020 already created and validated the artifacts. Prompt 035 is a recovery path, used only when prompt 030 generated Main Discovery without interactive user discussion. Prompt 045 closes the Requirements Baseline gate before scope decomposition.
