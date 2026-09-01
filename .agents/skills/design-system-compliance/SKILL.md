---
name: design-system-compliance
description: Audit rendered HTML artifacts for token, component, and layout pattern compliance against active DESIGN.md.
---

# Design System Compliance

Use this skill to audit rendered HTML artifacts against active `DESIGN.md` rules.

## Required Reads

1. Root `agents.md`.
2. [compliance-contract.md](references/compliance-contract.md).

## Operating Rules

- Audit all generated HTML artifacts against the active project design tokens and layout rules.
- Flag any arbitrary hex colors, unauthorized font styles, or non-token spacing.
- Enforce strict token fidelity (zero token fabrication).
- Run `python3 .agents/scripts/validate_token_compliance.py` and `validate_component_compliance.py`.

## Output Expectations

- Emit `compliance-report.md` detailing token, component, and pattern audit results.

## Superpowers V34 Discipline

- Clarify intent, scope, and verification criteria before executing tasks.
- Do not invent assumptions; ask the operator when blocking ambiguity exists.
- Ensure RED-GREEN-REFACTOR execution paths for behavior changes.
- Provide concrete evidence before making completion claims.
