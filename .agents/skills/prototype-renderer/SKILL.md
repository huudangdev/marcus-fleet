---
name: prototype-renderer
description: Render interactive prototype.html and components.html with state toggles for flow validation.
---

# Prototype Renderer

Use this skill when generating interactive prototypes and component galleries.

## Required Reads

1. Root `agents.md`.
2. [prototype-contract.md](references/prototype-contract.md).

## Operating Rules

- Render interactive `prototype.html` and `components.html` with state toggles.
- Enforce 100% project design token binding (zero arbitrary hex colors or spacing).
- Halt backend code changes; output self-contained HTML/CSS/JS validation artifacts only.
- Validate component compliance using `python3 .agents/scripts/validate_component_compliance.py`.

## Output Expectations

- Emit `prototype.html` with state simulators for all 8 mandatory states.
- Emit `components.html` cataloging all active UI component families.

## Superpowers V34 Discipline

- Clarify intent, scope, and verification criteria before executing tasks.
- Do not invent assumptions; ask the operator when blocking ambiguity exists.
- Ensure RED-GREEN-REFACTOR execution paths for behavior changes.
- Provide concrete evidence before making completion claims.
