---
name: understand-chat
description: Answer codebase questions using the knowledge graph with minimal reads
argument-hint: [query]
---

# /understand-chat

Answer questions about this codebase using `.understand-anything/knowledge-graph.json`.

## Required Reads

- [knowledge-graph-contract.md](references/knowledge-graph-contract.md)

## Operating Rules

- Grep the graph before reading it in full.
- Use node summaries, tags, and edges before touching source files.
- Keep the answer grounded in actual file paths, node IDs, and layer names.
- If the graph does not exist, tell the user to run `/understand` first.

## Output Expectations

- Reference specific nodes, files, and relationships.
- Explain which layer or layers are relevant and why.
- Stay concise, evidence-led, and scoped to the query.

## Superpowers V34 Discipline

- Clarify intent, scope, and verification criteria before executing tasks.
- Do not invent assumptions; ask the operator when blocking ambiguity exists.
- Ensure RED-GREEN-REFACTOR execution paths for behavior changes.
- Provide concrete evidence before making completion claims.
