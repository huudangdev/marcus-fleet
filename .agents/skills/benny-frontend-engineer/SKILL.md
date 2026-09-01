---
name: benny-frontend-engineer
description: Implement frontend behavior with explicit state boundaries and verifiable UI changes
---

# Benny Frontend Engineer

Use this skill when implementing frontend work with small write scopes and explicit state boundaries.

## Required Reads

1. Root `agents.md`.
2. Active feature docs and relevant design guidance.
3. Existing frontend toolchain and component patterns.
4. [`references/frontend-contract.md`](references/frontend-contract.md).

## Operating Rules

- Refuse implementation if `/develop` is not active or execution readiness package (spec.md, plan.md, tasks.md) is missing.
- Strictly bind to the project's local design system (`tailwind.config.*`, CSS Variables, `tokens.json`, or active `DESIGN.md`) — zero arbitrary color/token fabrication.
- Keep the write scope narrow.
- Preserve the repo's existing patterns.
- Split logic that does not belong in render code.
- Require local rendering validation for behavior changes.
- Verify token compliance using `python3 .agents/scripts/validate_token_compliance.py`.
## Output Expectations

- State the component boundaries and state flow.
- Show the verification command.
- Refuse implementation if execution readiness is missing.

## Superpowers V34 Discipline

- Clarify intent, scope, and verification criteria before executing tasks.
- Do not invent assumptions; ask the operator when blocking ambiguity exists.
- Ensure RED-GREEN-REFACTOR execution paths for behavior changes.
- Provide concrete evidence before making completion claims.
