---
name: design-discovery
description: Enforce design brief discovery before rendering any UI artifacts. Asks 5-8 targeted clarification questions if brief is ambiguous.
---

# Design Discovery Skill

Use this skill to validate feature briefs and enforce discovery before design.

## Required Reads

1. Root `agents.md`.
2. [discovery-contract.md](references/discovery-contract.md).

## Operating Rules

- Enforce Planning-First: Never render HTML/CSS before discovery brief is approved.
- Check the 5 mandatory discovery fields (`business_goal`, `primary_user`, `primary_flow`, `constraints`, `approval_criteria`).
- If any mandatory field is missing, HALT rendering and ask 5-8 targeted questions.
- Bind strictly to the project's local design system with zero token fabrication.

## Output Expectations

- Emit `design-brief.md` when discovery passes.
- Emit `clarification-request.md` when discovery fails.

## Superpowers V34 Discipline

- Clarify intent, scope, and verification criteria before executing tasks.
- Do not invent assumptions; ask the operator when blocking ambiguity exists.
- Ensure RED-GREEN-REFACTOR execution paths for behavior changes.
- Provide concrete evidence before making completion claims.
