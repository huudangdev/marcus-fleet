---
name: design-drift-review
description: Detect qualitative visual brand drift and unapproved visual anti-patterns in rendered HTML artifacts.
---

# Design Drift Review

Use this skill to detect qualitative visual brand drift and unapproved anti-patterns.

## Required Reads

1. Root `agents.md`.
2. [drift-contract.md](references/drift-contract.md).

## Operating Rules

- Scan artifacts for visual anti-patterns and brand drift against `anti-patterns.md`.
- Flag unauthorized styling decisions that break visual continuity.
- Enforce the Light Mode First mandate and token discipline.
- Validate drift using `python3 .agents/scripts/validate_design_drift.py`.

## Output Expectations

- Emit brand drift findings and concrete remediation steps in review notes.

## Superpowers V34 Discipline

- Clarify intent, scope, and verification criteria before executing tasks.
- Do not invent assumptions; ask the operator when blocking ambiguity exists.
- Ensure RED-GREEN-REFACTOR execution paths for behavior changes.
- Provide concrete evidence before making completion claims.
