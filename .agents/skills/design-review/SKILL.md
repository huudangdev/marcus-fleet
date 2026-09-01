---
name: design-review
description: Conduct multi-role design critique, scorecards, compliance checks, and review-pack.html generation.
---

# Design Review

Use this skill when conducting multi-role design critiques and compiling review packs.

## Required Reads

1. Root `agents.md`.
2. [review-contract.md](references/review-contract.md).

## Operating Rules

- Conduct rigorous multi-role critique across Design, Frontend, PM, and QA personas.
- Enforce design system compliance and flag visual drift or token violations.
- Gate progression: require $\ge 85\%$ score across all dimensions before approving handoff.
- Keep output in review markdown and HTML review packs.

## Output Expectations

- Emit `review.md` with multi-role scorecards and findings.
- Emit `review-pack.html` summarizing the review pack visually.

## Superpowers V34 Discipline

- Clarify intent, scope, and verification criteria before executing tasks.
- Do not invent assumptions; ask the operator when blocking ambiguity exists.
- Ensure RED-GREEN-REFACTOR execution paths for behavior changes.
- Provide concrete evidence before making completion claims.
