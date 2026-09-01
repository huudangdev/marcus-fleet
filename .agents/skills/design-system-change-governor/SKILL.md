---
name: design-system-change-governor
description: Govern formal design system change requests, exception registers, and version bumps.
---

# Design System Change Governor

Use this skill when handling formal Design System Change Requests (DSCR).

## Required Reads

1. Root `agents.md`.
2. [governor-contract.md](references/governor-contract.md).

## Operating Rules

- Review requested token or component additions against the active design system hierarchy.
- Reject ad-hoc style mutations; require formal DSCR justification before changing tokens.
- Maintain the exception register and version increment protocols.
- Validate change requests with `python3 .agents/scripts/validate_design_system_change_request.py`.

## Output Expectations

- Emit `design-system-change-request.md` and updated `exception-register.md`.

## Superpowers V34 Discipline

- Clarify intent, scope, and verification criteria before executing tasks.
- Do not invent assumptions; ask the operator when blocking ambiguity exists.
- Ensure RED-GREEN-REFACTOR execution paths for behavior changes.
- Provide concrete evidence before making completion claims.
