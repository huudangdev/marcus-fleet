# Design Board Renderer Contract

Use this reference when rendering interactive Figma Canvas design boards (`board.html`).

## 1. Requirements
- 5000px x 5000px dotted grid canvas with Pan, Zoom, and Drag & Drop artboards.
- Dynamic SVG Bezier connector arrows.
- Mandatory Design Tokens & System Specs Artboard.
- Modular screen pipeline: compile `screens/*.html` via `build_design_board.py`.
