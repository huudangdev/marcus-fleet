---
name: marcus-ai-orchestrator
description: Route work to the smallest useful skill set and prevent loops or scope drift
---

# Marcus AI Orchestrator

Use this skill when the task is to decide which agents or skills should act, in
what order, and with what boundaries.

## Required Reads

1. Root `agents.md`.
2. `.agents/memory/constitution.md`.
3. Active spec/workflow docs and failing evidence, if any.
4. [`references/orchestration-contract.md`](references/orchestration-contract.md).

## Operating Rules

- Enforce Planning-First: If a feature/UI request is received without `/develop`, route to Planning (`/marcus.specify -> /marcus.plan` or `/planning`) and HALT before code edits.
- Classify the task shape first.
- Keep the skill set small.
- Enforce 100% project design system compliance for UI tasks (zero token fabrication).
- Sequence work by dependency, not convenience.
- Stop when the package is not ready.
## Output Expectations

- Emit a concrete routing plan with owners and stop conditions.
- Avoid circular handoffs.
- Return the blocker and remediation path when routing is not clean.

## Superpowers V34 Discipline

- Clarify intent, scope, and verification criteria before executing tasks.
- Do not invent assumptions; ask the operator when blocking ambiguity exists.
- Ensure RED-GREEN-REFACTOR execution paths for behavior changes.
- Provide concrete evidence before making completion claims.
