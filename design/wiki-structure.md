# Wiki Structure

This document defines the structure of the agent-wiki — the persistent, LLM-maintained knowledge base on AI agents.

## Directory Layout

```
agent-wiki/
├── index.md               # Catalog of all pages, organized by category
├── log.md                 # Append-only chronological log of ingests and updates
├── overview.md            # High-level synthesis of the current state of AI agents
├── concepts/              # Foundational ideas, patterns, and techniques
│   └── <concept>.md
└── tools/                 # Specific frameworks, libraries, and platforms
    └── <tool>.md
```

## Page Types

### `overview.md`

A high-level synthesis of the field — where things stand, what the key open questions are, and how major themes relate to each other. Updated as the wiki evolves. The starting point for a new reader.

### `index.md`

A catalog of all pages in the wiki, grouped by category. Each entry is a link plus a one-line description. The LLM reads this first when answering queries or deciding where to file new information.

Format:
```markdown
## Concepts

- [Tool Use](concepts/tool-use.md) — How agents invoke external tools and APIs
- [Memory](concepts/memory.md) — Mechanisms for agents to retain information across turns

## Tools

- [LangGraph](tools/langgraph.md) — Graph-based orchestration framework from LangChain
```

### `log.md`

An append-only record of every ingest.

Each log entry includes two summaries:

**Technical**: files touched, links added or changed, new pages created.

**Reader-friendly**: written for someone already familiar with the wiki. Explains what actually changed in the field and why it matters — not just what files were edited. This is the material for the newsletter email.

Each entry begins with a consistent prefix for easy grepping:

```markdown
## [2026-05-04]

- Pages updated: concepts/tool-use.md, tools/openai-agents-sdk.md (new)
- Summary: OpenAI released a new Agents SDK…
```

### `concepts/<concept>.md`

One page per concept, pattern, or technique. Examples: `tool-use.md`, `memory.md`, `multi-agent.md`, `planning.md`, `evaluation.md`. Each page covers:

- What the concept is and why it matters
- Key variants and tradeoffs
- Links to relevant tools

### `tools/<tool>.md`

One page per framework, library, or platform. Examples: `langchain.md`, `langgraph.md`, `openai-agents-sdk.md`. Each page covers:

- What it is and what problem it solves
- Key features and design decisions
- How it relates to alternatives
- Links to relevant concept pages

## Conventions

- All pages use standard markdown with wiki-style links (`[Tool Use](concepts/tool-use.md)`).
- Every non-index, non-log, non-overview page ends with a `## See Also` section listing related pages.
- The `overview.md` is rewritten (not appended) when significant new information arrives; the log records what changed.
- Page titles match filenames: `tool-use.md` → `# Tool Use`.
- `log.md` is append-only — never edit past entries.

## What Belongs in Concepts vs. Tools

- **Concepts**: Ideas, patterns, techniques, and mechanisms — things that exist independent of any specific implementation. Examples: `tool-use.md`, `memory.md`, `multi-agent.md`.
- **Tools**: Specific frameworks, libraries, SDKs, platforms, or protocols. Examples: `langgraph.md`, `mcp.md`, `openai-agents-sdk.md`.

When in doubt: if you could describe it without naming a product, it's a concept.

## Quality Bar

- Be concise. Each page should be readable in a few minutes.
- Prefer accurate and current over exhaustive.
- Link generously between pages — that's what makes this a wiki.
- Do not repeat information already on a linked page; reference it instead.
