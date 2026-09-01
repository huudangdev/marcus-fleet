---
name: design-direction-advisor
description: Propose 2-3 structured visual and tone directions when function is clear but art direction needs framing.
---

# Design Direction Advisor

Use this skill when function is clear but visual direction needs stakeholder alignment.

## Required Reads

1. Root `agents.md`.
2. [advisor-contract.md](references/advisor-contract.md).

## Operating Rules

- Formulate 2-3 structured directions (Tone, Suitability, Advantages, Risks, Recommendation).
- Enforce Planning-First: Never output production code or unapproved styles.
- Bind strictly to the active design system token hierarchy (zero arbitrary tokens).
- Require human alignment before moving to coverage or layout rendering.

## Output Expectations

- Emit `direction-options.md` containing structured comparison tables.

## Superpowers V34 Discipline

- Clarify intent, scope, and verification criteria before executing tasks.
- Do not invent assumptions; ask the operator when blocking ambiguity exists.
- Ensure RED-GREEN-REFACTOR execution paths for behavior changes.
- Provide concrete evidence before making completion claims.
