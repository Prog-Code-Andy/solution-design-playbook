# Generic LLM Adapter

Give the model:

```text
Read solution-design-playbook/README.md and 00-prompts/000-start-here.md.
Treat docs/project-design/workflow-state.yaml as machine-readable state.
Work in discussion/planning mode until an approved phase explicitly authorizes execution.
Do not infer approvals. Show assumptions and open questions. Stop at every gate.
```

If the model cannot read local files, provide the root README, relevant governance files, current YAML state, and only the current numbered prompt.

