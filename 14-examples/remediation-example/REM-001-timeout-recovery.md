# REM-001: Timeout Recovery and Diagnostic Evidence

- Status: Proposed
- Scope: INTEGRATION-A
- Governing EDRs: EDR-003
- Requires new EDR: No
- Repairs: Completed integration reliability gap
- Phase advancement: None
- Exact approval phrase: `Approve Remediation REM-001`

## Confirmed problem

A controlled test proves that a timeout leaves the operation non-terminal and emits no safe diagnostic event.

## Authorized scope

Add bounded timeout recovery, one terminal state, privacy-safe evidence, and targeted regression tests.

## Explicit exclusions

No new integration features, architecture replacement, roadmap advancement, or unrelated refactoring.

## Acceptance criteria

- Timeout always reaches one terminal state.
- A sanitized correlated diagnostic event is retained.
- Targeted tests cover success, timeout, cancellation, and duplicate completion.

