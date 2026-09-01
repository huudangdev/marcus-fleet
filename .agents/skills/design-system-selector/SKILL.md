---
name: design-system-selector
description: Bind feature briefs to appropriate active domain design systems (company, erp-enterprise, ops-monitoring, executive-insight).
---

# Design System Selector

Use this skill to bind feature briefs to the correct project design system.

## Required Reads

1. Root `agents.md`.
2. [selector-contract.md](references/selector-contract.md).

## Operating Rules

- Analyze domain and feature type to bind the feature to the correct `DESIGN.md`.
- Enforce 100% token binding to active project tokens (zero arbitrary colors).
- Halt code modifications; emit design context as planning artifacts.
- Map complex forms to `erp-enterprise`, telemetry to `ops-monitoring`, crypto to `binance`.

## Output Expectations

- Emit `design-context.md` binding the active design tokens and rules.

## Superpowers V34 Discipline

- Clarify intent, scope, and verification criteria before executing tasks.
- Do not invent assumptions; ask the operator when blocking ambiguity exists.
- Ensure RED-GREEN-REFACTOR execution paths for behavior changes.
- Provide concrete evidence before making completion claims.
