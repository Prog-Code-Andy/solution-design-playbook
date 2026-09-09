# Scope Governance

`MAIN` is the root scope. A project begins in `undecided` mode unless its structure is already explicit.

## Single scope

Use when one coherent design boundary, owner set, lifecycle, and delivery path are sufficient. `MAIN` is both solution and implementation scope.

## Multi scope

Use when bounded capabilities or integrations require separate discovery and TDDs. Subscopes inherit MAIN constraints and cannot override global accepted EDRs.

Do not create one scope or TDD per requirement automatically. Group requirements by cohesive responsibility, interface, owner, security boundary, and lifecycle.

A multi-scope project requires approved Main Discovery, requirements sources, scope decomposition, cross-cutting constraints, and an initial Main Architecture Baseline before deep scoped design. Scope activation is explicit and recorded in `workflow-state.yaml`.

