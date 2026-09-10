# Windsurf Adapter

Use Windsurf Plan Mode for Discovery, Requirements, EDR, Contract, Design, Roadmap, Phase, and Task discussions.

```text
Read solution-design-playbook/README.md.
Run 00-prompts/000-start-here.md.
Use docs/project-design/ as the default output root.
Stay in Plan Mode and do not implement application changes unless workflow-state.yaml records a separately approved execution phase.
```

Before changing stage or scope, read `workflow-state.yaml` and `scope-registry.yaml`. Use prompt 060 for an explicit scope switch such as `MAIN → ENTRA-ID`.

## Plan-to-files cycle

Windsurf's `Implement` action is a tool transition from Plan Mode to Code Mode; it is not a Playbook approval. Use this bounded cycle:

1. Run one current numbered prompt in Plan Mode and discuss it to a review-ready plan.
2. Review the exact file boundary and approval gate.
3. Use prompt 025 when materializing the initial 010/020 plan; otherwise authorize only the current planning artifact under `docs/project-design/**`.
4. Let Code Mode write and validate only those planning artifacts.
5. Confirm `implementation_allowed: false`, record the next prompt, stop, and return to Plan Mode.

Do not place all numbered prompts into one Windsurf plan. Prompts 060–120 form a repeatable per-scope loop; prompt 180 is post-delivery, and prompt 190 is conditional remediation.
