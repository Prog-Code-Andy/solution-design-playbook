# Prompt 045 — Review Requirements Baseline

Prerequisites: approved Main Discovery, registered authoritative sources, and a Proposed requirements analysis.

1. Read all registered requirements sources that are accessible, the requirements analysis, approved Main Discovery, source registry, requirements index, and open questions.
2. Verify source-defined IDs and exact source references are preserved.
3. Check completeness, duplicates, conflicts, ambiguity, missing acceptance criteria, derived requirements, proposed scope mappings, and inaccessible-source limitations.
4. Distinguish the source baseline from design choices. Do not turn assumptions or proposed solutions into requirements without explicit owner approval.
5. If incomplete, keep status Under Review and produce a bounded revision/blocker list.
6. If ready, summarize the baseline version, source coverage, exclusions, unresolved non-blocking items, and traceability status, then request a new exact message: `Approve Requirements Baseline v1.0`.
7. Only after that message, record Approved status, approver, timestamp, and version in Markdown and YAML. Keep project implementation unauthorized.
8. Set `next_prompt: 050-decompose-scopes` and stop.

Expected stop: approved Requirements Baseline or explicit revision work; no scope decomposition or implementation has begun.

