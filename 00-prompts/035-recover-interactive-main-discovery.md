# Prompt 035 — Recover Interactive Main Discovery

Use this recovery prompt only when prompt 030 produced `DISC-MAIN-001` without completing the required interactive discussion with the user.

## Purpose

Convert an AI-generated Main Discovery draft into a user-reviewed discovery proposal. This prompt does not approve Discovery, Requirements, scope decomposition, decisions, design, or implementation.

## Authorization

- Work in planning/discussion mode.
- Allowed eventual writes: Main Discovery and directly related control/reporting artifacts under `docs/project-design/**` only.
- Project source code, tests, runtime configuration, infrastructure, deployment, EDRs, contracts, designs, roadmaps, phases, and tasks: prohibited.
- Keep `authorization.mode: discussion_only` and `implementation_allowed: false`.
- Do not interpret any approval phrase printed in this prompt as user approval.

## Preconditions

1. Read the playbook root README and `01-governance/`.
2. Read prompts 030, 035, and 040.
3. Read `project.yaml`, `workflow-state.yaml`, `scope-registry.yaml`, `artifact-index.yaml`, requirements registries/indexes, requirements analysis, assumptions/open questions, and the existing `DISC-MAIN-001`.
4. Confirm that MAIN is the active scope and that no later planning artifact has been approved from the unreviewed Discovery.
5. If later artifacts already depend on it, report the affected artifacts and stop for recovery direction.

## Immediate state

Treat the existing `DISC-MAIN-001` as an AI-generated draft. Set or keep its working status `Under Review`; do not mark it Approved.

## Interactive review protocol

Conduct exactly one round at a time. For each round:

1. Show the current relevant content from `DISC-MAIN-001`.
2. Cite the supporting requirement/source references.
3. Separate confirmed facts from inferences and assumptions.
4. Identify contradictions, missing information, and material risks.
5. Ask a short group of specific questions.
6. Stop and wait for the user's response.
7. Do not advance to the next round in the same response.

### Round 1 — Problem and outcomes

- Problem statement
- Desired outcomes
- Users/beneficiaries
- Success evidence

### Round 2 — Scope and boundaries

- Included scope
- Excluded scope
- System boundary
- Read-only versus change/execution responsibilities

### Round 3 — Systems and integrations

- Current state
- Participating systems
- External dependencies
- Sources, execution targets, and owners

### Round 4 — Data, security, and operations

- Data inputs, outputs, storage, classification, and retention
- Identity, permissions, secrets, and trust boundaries
- Privacy/compliance constraints
- Availability, support, and operational constraints

### Round 5 — Stakeholders and authority

- Business and technical owners
- Security/platform/integration reviewers
- Approval responsibilities
- Ownership gaps

### Round 6 — Uncertainty and decisions needed

- Confirmed facts
- Assumptions
- Constraints
- Risks
- Blocking and non-blocking open questions
- Durable decisions that may later require EDRs

### Round 7 — Project mode and capability map

- `single-scope` versus `multi-scope` recommendation
- Candidate capabilities and scopes
- Cross-cutting concerns
- Proposed dependencies

The recommendation remains provisional. Scope decomposition is approved only through prompt 050.

## Materialization after all seven rounds

Only after the user has answered all rounds:

1. Summarize confirmed corrections and unresolved questions.
2. Update only `DISC-MAIN-001`, its facts/assumptions/open-questions artifact, `artifact-index.yaml`, and `workflow-state.yaml` under `docs/project-design/**`.
3. Mark Main Discovery `Proposed` only when its exit criteria are satisfied; otherwise keep it `Under Review` with a bounded revision list.
4. Validate source traceability, unique IDs, paths, YAML syntax, and Markdown/YAML status consistency.
5. Set `active_scope: MAIN`, `active_stage: main_discovery_review`, `next_prompt: 040-review-main-discovery`, and keep `implementation_allowed: false`.

## Stop condition

Report the exact changed planning files and validation results, then stop. Do not run prompt 040 automatically and do not request or record Discovery approval from this recovery prompt.

