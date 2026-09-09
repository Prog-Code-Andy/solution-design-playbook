# Prompt 060 — Activate Scope

Input: exact approved `scope_id`.

1. Confirm the scope exists, its parent exists, prerequisites are approved, and current work can be safely paused or completed.
2. Summarize inherited MAIN constraints, relevant requirements, dependencies, and known blockers.
3. Ask for clarification only if the scope ID is ambiguous or unregistered.
4. Update `active_scope`, `active_stage`, `active_artifact`, and `next_prompt` without changing another scope's approved artifacts.
5. Keep implementation authorization false.

Expected stop: requested scope is active and prompt 070 is the next action.

