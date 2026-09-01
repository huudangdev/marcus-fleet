---
name: flow-coverage-planner
description: Deconstruct PRDs into comprehensive flow inventories, screen catalogs, and mandatory state coverage matrices.
---

# Flow Coverage Planner

Use this skill to map end-to-end user flows and 8-state coverage matrices.

## Required Reads

1. Root `agents.md`.
2. [flow-contract.md](references/flow-contract.md).

## Operating Rules

- Map all screen nodes, transitions, and edge cases before visual rendering.
- Enforce the mandatory 8-state coverage matrix across all screen catalogs.
- Halt code execution; emit planning and coverage artifacts only.
- Ground state designs strictly in the project's local design system.

## Output Expectations

- Emit `flow-inventory.md`, `screen-catalog.md`, and `state-coverage.md`.

## Superpowers V34 Discipline

- Clarify intent, scope, and verification criteria before executing tasks.
- Do not invent assumptions; ask the operator when blocking ambiguity exists.
- Ensure RED-GREEN-REFACTOR execution paths for behavior changes.
- Provide concrete evidence before making completion claims.
