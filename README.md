# Solution Design Playbook

A model-independent, approval-gated workflow for turning requirements into reviewed decisions, contracts, solution designs, technical designs, roadmaps, phases, tasks, verification evidence, and remediation packages.

## Start here

For a new project, give the model this instruction:

```text
Read solution-design-playbook/README.md and run 00-prompts/000-start-here.md.
Work in planning/discussion mode. Do not implement project deliverables.
```

The default project-artifact location is `docs/project-design/`. The playbook may be installed at `solution-design-playbook/` or, when configured explicitly, at `docs/solution-design-playbook/`.

## Workflow

```text
Governance → Discovery → Requirements → Decisions → Contracts → Design
→ Roadmap → Phases → Tasks → Verification → Reports
                                      ↘ Remediation when required
```

Planning is iterative, but authority is ordered. A model may draft and recommend; only an explicit user approval changes a gate.

## Numbered entry prompts

Read [00-prompts/README.md](00-prompts/README.md). Start with `000-start-here.md`; for an existing project, it will read `docs/project-design/workflow-state.yaml` and identify the legal next action.

## Core rules

- Markdown in the local Git repository is the canonical documentation format.
- YAML files are the machine-readable control plane; the model maintains them, while the user approves decisions.
- `MAIN` is always the root scope.
- A project may be `undecided`, `single-scope`, or `multi-scope`.
- Requirements retain source-defined identifiers. Local identifiers are generated only when the source has none.
- EDR is the umbrella decision-record format; architecture is an EDR category, so duplicate ADR files are unnecessary.
- A Solution Design describes the whole system. A TDD describes one bounded technical scope.
- No completion, prompt, or model inference approves the next stage or implementation phase.

## Repository sections

| Directory | Purpose |
|---|---|
| `00-prompts` | Ordered workflow entry points |
| `01-governance` | Authority, gates, lifecycle, naming, and state rules |
| `02-discovery` | Main and scoped discovery templates |
| `03-requirements` | Source intake, analysis, classification, and traceability |
| `04-decisions` | Engineering Decision Records (EDRs) |
| `05-contracts` | API, data, event, and evidence contracts |
| `06-design` | Solution Design and Technical Design Documentation |
| `07-roadmap` | Outcome and dependency sequencing |
| `08-phases` | Bounded execution phases |
| `09-tasks` | Traceable units of work |
| `10-verification` | Acceptance plans and evidence |
| `11-remediation` | Corrective work packages |
| `12-reports` | Review and completion reports |
| `13-model-adapters` | Small environment-specific adapters |
| `14-examples` | Single-scope, multi-scope, and remediation examples |

## Canonical project layout

```text
project-root/
├── solution-design-playbook/
├── docs/
│   └── project-design/
│       ├── project.yaml
│       ├── workflow-state.yaml
│       ├── scope-registry.yaml
│       ├── artifact-index.yaml
│       ├── requirements-source-registry.yaml
│       └── requirements-index.yaml
└── existing project files (unchanged)
```

## Status

Version 0.1.1. The playbook includes explicit Windsurf Plan-to-files and Requirements Baseline review gates.
