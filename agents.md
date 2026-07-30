# Marcus Fleet Codex Adapter

This file adapts the repo's `.agents` system into instructions Codex can follow
reliably in this environment.

## Source of Truth

- Read [agents.md](/Users/lequynhanh/marcus-fleet/agents.md), `.agents/memory/constitution.md`, and the relevant `.agents/workflows/*.md` file before material work.
- For non-trivial changes, treat `.agents/specs/<feature-id>/spec.md`, `plan.md`, `tasks.md`, and `verification.md` as higher-signal than ad hoc chat instructions unless the user explicitly overrides them.
- If project docs are stale, missing, or clearly boilerplate relative to code reality, flag that as a risk before making behavior-changing edits.

## Preferred Codex Skills

- Use the local Codex Marcus skills as the first translation layer for this repo.
- `$marcus-spec-planner`
- `$marcus-docs-writer`
- `$marcus-design-taste`
- `$marcus-qa-gate`
- `$marcus-refactor-audit`
- `$marcus-research-synth`
- Reach into `.agents` source material for grounding, not for literal execution of unavailable commands.
- When a task spans multiple disciplines, pick the smallest useful skill set instead of loading every related skill.

## Startup Checklist

- Start with the minimum viable context, not a full corpus dump.
- Read root `agents.md` for project state and session history.
- Read `.agents/memory/constitution.md` for durable governance rules.
- Read the closest matching workflow in `.agents/workflows/` for the current task shape.
- If the task is scoped to an existing feature or epic, read the relevant `.agents/specs/<feature-id>/` files before editing code.
- If the task follows a Marcus slash command, respect that workflow's script chain exactly. Example: `/marcus.tasks` owns `build_execution_brief.py`; `/develop` consumes the resulting `execution-brief.md` and must not skip its readiness gates.
- If the task changes behavior in an already-running product area, inspect `/docs` and `/docs/development/` enough to detect whether the documentation trail is credible or stale.
- For non-trivial work, prefer the full Marcus loop: `/marcus.specify -> /marcus.clarify -> /marcus.plan -> /marcus.tasks -> /marcus.review -> /marcus.rehearse -> /marcus.verify`.

## Execution Rules

- Verify changed behavior before finalizing. Use project tests where they exist; use Playwright MCP for browser flows when the app can be started locally.
- Keep execution bounded. If the same class of failure repeats three times without new evidence, stop guessing and report the blocker.
- Never claim tests passed without concrete command or MCP evidence.
- Prefer project-local validators and test commands over generic substitutes when they exist and are runnable.
- If verification requires a dev server, state which server was started, which flow was exercised, and what was or was not observed.
- Treat review loops and POC rehearsal as first-class gates, not documentation garnish. A feature package without challenge findings and a release recommendation is not ready.
- When `.agents` routing changes, use `.agents/ROUTING_REGRESSION_CHECKLIST.md` to test the five core task shapes before trusting the release.
- Treat `.agents/scripts/` as workflow-bound entrypoints, not ambient powers. A script should be run only when a workflow names it, a gate depends on its output, and a later artifact consumes that output.

## Brownfield Gate

- Treat missing docs, stale docs, template-only docs, and undocumented code reality as one class of brownfield risk.
- For small low-risk fixes, proceed carefully and report the documentation gap.
- For broader behavior changes, stop and surface the gap before improvising a fake spec process.
- Do not present Marcus Fleet governance as satisfied unless the supporting docs or evidence actually exist.

## Import Boundary

- Import guidance, not bulk artifacts. Ignore `.agents/node_modules`, `.agents/trustgraph-viewer/.next`, Git internals, generated files, and vendored dependencies as instruction sources.
- Treat `.agents/.clinerules` as intent-rich but not literal: keep the testing, docs, and safety goals, while adapting tool names and commands to the current Codex environment.
- Treat `.agents/mcp/mcp.json` as a reference catalog, not a guaranteed runnable config. Validate MCP packages before adopting them.
- Do not trust placeholder commands, placeholder tokens, or paths to nonexistent files just because they appear in doctrine documents.
- When `.agents` and live repo reality disagree, prefer live repo reality and note the mismatch.

## Durable Memory

- After significant Marcus Fleet work, prefer updating the project's durable artifacts that already exist: `agents.md`, relevant spec/workflow docs, and verification evidence.
- TrustGraph writes are desirable when the local adapter path is available, but they are not a reason to fabricate success or block unrelated safe work.
- Session history updates in `agents.md` should be concise, factual, and tied to meaningful changes or discoveries rather than noisy command logs.
- Residual risk should be recorded explicitly when a task closes without full verification or without full documentation alignment.

## Session History

- 2026-05-18: Began Marcus Fleet V34 Superpowers Discipline Layer under
  `.agents/specs/020-superpowers-discipline-layer-v34/`. The upgrade adds a
  first-class `validate_superpowers_discipline.py` gate, wires it into harness
  preflight/postflight/docs/readiness paths, updates README-published slash
  command workflows with clarification/TDD/root-cause/review/verification
  discipline, and records fresh validator evidence in the feature workspace.
- 2026-07-29: Upgraded `.agents` ecosystem to V35 Design-Focused Enterprise Operating System
  (Design V2 Blueprint + Governance). Added Design System Governance layer (`.agents/design-systems/`),
  11 specialized AI skills (`design-discovery`, `design-direction-advisor`, `flow-coverage-planner`,
  `design-board-renderer`, `prototype-renderer`, `design-review`, `handoff-generator`, `design-system-selector`,
  `design-system-compliance`, `design-drift-review`, `design-system-change-governor`), 6 design slash
  command workflows (`/design`, `/design.coverage`, `/design.board`, `/design.prototype`, `/design.review`, `/design.handoff`),
  16 templates (including `board.html`, `prototype.html`, `components.html`, `review-pack.html`), and
  11 deterministic Python validation gates in `.agents/scripts/`.
- 2026-07-30: Upgraded `.agents` ecosystem to V36 Design OS & Modular Pipeline Architecture (Release V36.0). Added Modular Screen Generation Pipeline (`screens/screen_XX.html`), Master Self-Healing Assembler (`.agents/scripts/build_design_board.py`), 11th Deterministic Validation Gate (`validate_modular_design.py`), Binance Enterprise Design System (`binance/DESIGN.md`), 20-Screen Interactive Mobile Board (`024-binance-mobile-20-screens`), Light Mode First Mandate Enforcement, and system-wide Clean Unicode Formatting Standard (100% removal of raw LaTeX artifacts).
