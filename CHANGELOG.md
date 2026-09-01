# Marcus Fleet Changelog

All notable changes to the Marcus Fleet Enterprise OS ecosystem will be documented in this file.

## [36.1.0] - 2026-09-02

### Added
- **Absolute Directive 1: Planning-First Mandate**: Hard refusal to call code generation/editing tools (`write`, `edit`, `replace`) without an explicit `/develop` invocation and approved spec/plan package. Open-ended prompts default to `/marcus.specify` / `/planning` and halt for user review.
- **Absolute Directive 2: 100% Local Design System Compliance (Zero-Fabrication Rule)**: Mandated scanning and strict binding to user project local tokens (`tailwind.config.*`, CSS Variables in `globals.css`/`tokens.css`, `tokens.json`, or `.agents/design-systems/<domain>/DESIGN.md`) with zero arbitrary hex color or token fabrication.
- **Complete 76/76 Skill Contract Standardization**: Added `references/*.md` contracts and structured sections (`## Required Reads`, `## Operating Rules`, `## Output Expectations`, `## Superpowers V34 Discipline`) across all 76 skills, passing `validate_skill_contracts.py` with 100% compliance.

### Changed
- **Synchronized `.clinerules` & Hardened `agents.md`**: Synchronized root and `.agents/.clinerules` at V36.1. Removed the weakening clause in `agents.md` ("intent-rich but not literal") to make architectural governance binding across all client runtimes.
- **Zero-Fabrication TrustGraph Fallback**: Sanitized `trustgraph_query.py` offline fallback to stop emitting simulated fake module dependencies or bug histories when Neo4j is offline.

---

## [36.0.0] - 2026-07-30

### Added
- **Modular Screen Generation Pipeline**: Split large UI design board generation into isolated screen HTML modules under `screens/screen_XX.html` to eliminate LLM token limit truncations.
- **Master Autonomous Board Assembler (`.agents/scripts/build_design_board.py`)**: Self-healing assembler script that compiles screen modules into interactive `board.html` with zoom, drag & drop, and 20 dynamic SVG Bezier connector edges. Auto-bootstraps missing screen modules from `screen-catalog.md`.
- **11th Validation Gate (`.agents/scripts/validate_modular_design.py`)**: Automated verification gate auditing modular pipeline compliance across all feature design workspaces.
- **Binance Enterprise Design System (`.agents/design-systems/binance/DESIGN.md`)**: Full design system contract with Binance Gold (`#F0B90B`), dark slate, trade success/danger tokens, and component fixtures.
- **20-Screen Interactive Mobile Trading Board (`024-binance-mobile-20-screens`)**: Rendered 20 mobile screens (`MOB-001` through `MOB-020`) and system specs card connected via 20 dynamic Bezier flow edges.

### Changed
- **Light Mode First Mandate**: Updated `.agents/design-systems/company/DESIGN.md` and `design-board-renderer` skill enforcing clean Light Mode (`#f8fafc` canvas, `#ffffff` cards) as mandatory default.
- **Clean Unicode Text Standard**: Purged all raw LaTeX syntax (`\rightarrow`) across all system workflows, skills, architecture docs, and design briefs, replacing them with clean Unicode text arrows (`→`).
- **Validation Suite Upgrade**: Expanded deterministic gate suite from 10 to 11 passing verification gates.

---

## [35.0.0] - 2026-07-29

### Added
- **Design-Focused Enterprise Operating System**: Integrated Design System Governance layer under `.agents/design-systems/`.
- **11 Design Skills**: Added `design-discovery`, `design-direction-advisor`, `flow-coverage-planner`, `design-board-renderer`, `prototype-renderer`, `design-review`, `handoff-generator`, `design-system-selector`, `design-system-compliance`, `design-drift-review`, `design-system-change-governor`.
- **6 Design Slash Command Workflows**: `/design`, `/design.coverage`, `/design.board`, `/design.prototype`, `/design.review`, `/design.handoff`.
- **10 Deterministic Python Validation Gates**: Gated pipeline preventing drift and unapproved design changes.
