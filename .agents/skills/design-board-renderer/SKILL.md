---
name: design-board-renderer
description: Render interactive Figma Canvas design boards (board.html) with Drag & Drop artboards, Mouse Wheel Zooming, dynamic SVG connectors, live component interactivity, and mandatory Design Tokens & System Specs artboard.
---

# Design Board Renderer

Use this skill when rendering visual design boards and compiling modular screens into `board.html`.

## Required Reads

1. Root `agents.md`.
2. [board-contract.md](references/board-contract.md).

## Operating Rules

- Render interactive Figma Canvas boards (`board.html`) on a 5000px x 5000px dotted grid.
- Enforce 100% project design token binding with zero arbitrary colors or tokens.
- Mandate inclusion of the Design Tokens & System Specs Artboard.
- Use modular screen generation (`screens/screen_XX.html`) and compile with `build_design_board.py`.

## Output Expectations

- Emit `board.html` compiling all screen modules with live interactivity and dynamic SVG connectors.

## Superpowers V34 Discipline

- Clarify intent, scope, and verification criteria before executing tasks.
- Do not invent assumptions; ask the operator when blocking ambiguity exists.
- Ensure RED-GREEN-REFACTOR execution paths for behavior changes.
- Provide concrete evidence before making completion claims.
