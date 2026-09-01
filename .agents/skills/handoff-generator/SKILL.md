---
name: handoff-generator
description: Package approved design artifacts into execution packages for frontend engineering and UAT.
---

# Handoff Generator

Use this skill when compiling final developer handoff packages and UAT checklists.

## Required Reads

1. Root `agents.md`.
2. [handoff-contract.md](references/handoff-contract.md).

## Operating Rules

- Assemble the complete design handoff package from approved artifacts.
- Map 100% of design tokens to production engineering CSS variables/classes.
- Structure UAT test cases covering all 8 mandatory states.
- Validate handoff readiness using `python3 .agents/scripts/validate_handoff_readiness.py`.

## Output Expectations

- Emit `handoff.md` and `uat-checklist.md`.

## Superpowers V34 Discipline

- Clarify intent, scope, and verification criteria before executing tasks.
- Do not invent assumptions; ask the operator when blocking ambiguity exists.
- Ensure RED-GREEN-REFACTOR execution paths for behavior changes.
- Provide concrete evidence before making completion claims.
