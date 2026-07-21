# Local and portable memory alternatives

**Audience:** Course instructors and curious learners  
**Course 1 default:** [ALIVE](https://alivecontext.com/) + [Claude Code](https://code.claude.com/docs/en/quickstart)  
**Last reviewed:** July 2026

This document compares ways to give an AI assistant **persistent context across sessions**—without treating any single product as the only answer. Course 1 teaches ALIVE inside Claude Code because that stack is local, inspectable, and matches the hands-on path. Everything below is optional reading if you use a different harness or want a more portable pattern.

---

## How to read this guide

Three layers are easy to conflate:

| Layer | What it is | Examples |
| ----- | ---------- | -------- |
| **Model** | The reasoning engine that predicts text (and sometimes other modalities) | Claude, GPT, Gemini, local Llama |
| **Harness** | The app/runtime around the model: UI, context assembly, tools, permissions, session handling | Claude Code, Cursor, OpenCode, Codex CLI |
| **Memory layer** | How information survives after a session ends | ALIVE files, `AGENTS.md`, MCP memory server, Mem0 API |

The harness decides *what the model sees this turn*. The memory layer decides *what gets saved and reloaded later*. Same model, different harness → different defaults for files, tools, and memory. Switching harnesses usually means switching memory patterns too.

---

## Quick comparison

| Option | Primary fit | Harness compatibility | Setup | Local by default? | Team-share potential | Maintenance |
| ------ | ----------- | --------------------- | ----- | ----------------- | -------------------- | ----------- |
| **ALIVE + Claude Code** *(Course 1 path)* | Structured project context in plain files; checkpoint at session end | Claude Code (plugin) | Intermediate | Yes | Good via git/Dropbox on `.alive/` | Low–medium; plugin + folder conventions |
| **Plain markdown / project files** | Portable, human-readable notes you control | Any file-aware harness | Beginner | Yes | Excellent (git) | Low; you enforce structure |
| **`AGENTS.md` / `CLAUDE.md` conventions** | Standing instructions + light project context | Codex, OpenCode, Cursor, Claude Code, others | Beginner | Yes | Excellent (git) | Low; size limits on some harnesses |
| **Cursor rules / skills** | Editor-specific behavior and repeatable workflows | Cursor primarily | Beginner–intermediate | Yes | Good (repo rules); skills vary | Low–medium |
| **MCP memory server** | Agent-agnostic graph memory via MCP | Any MCP-capable client (Claude Desktop, Cursor, VS Code, etc.) | Intermediate | Yes (default `memory.jsonl`) | Medium; file or DB sync | Medium |
| **Mem0** | Drop-in memory API for apps and agents | Framework integrations; not a harness | Intermediate | Optional (hosted or self-host) | Strong multi-tenant patterns | Medium; API + extraction tuning |
| **Zep / Graphiti** | Time-aware facts and relationships | Backend service; agents call SDK/API | Intermediate–advanced | Self-host possible | Strong for CRM-like state | Medium–high |
| **Letta** | Stateful agent runtime with self-edited memory | Letta runtime / Letta Code | Intermediate–advanced | Self-host possible | Per-agent isolation | Medium–high |
| **OpenMemory** | Self-hosted cognitive memory engine + MCP | SDK, MCP clients, custom apps | Intermediate | Yes | Service mode possible | Medium |

None of these guarantee correctness. All require human review of what was saved and what gets retrieved.

---

## Course 1 path: ALIVE + Claude Code

### What it is

[ALIVE](https://alivecontext.com/) is an open-source **personal context manager** for Claude Code. It stores project state—decisions, tasks, knowledge—in readable Markdown and JSON on disk. Lifecycle hooks load context at session start; `/alive:save` checkpoints work at session end.

### Harness compatibility

- **Built for:** Claude Code (plugin marketplace).
- **Not claimed today:** Native adapters for other harnesses in the current stable release (cross-agent portability is on the project's roadmap; files remain ordinary Markdown either way).

### Setup complexity

**Intermediate** — requires Claude Code, Python 3.10+, plugin install, and guided `/alive:world` setup.

### Tradeoffs

| Pros | Cons |
| ---- | ---- |
| Plain files you can open in any editor | Tied to Claude Code for the automated load/save workflow |
| Local-first; no account for core use | Another convention to learn (walnuts, bundles, checkpoints) |
| Strong fit for multi-session project work | Not a team permissions system |

### When to choose it vs alternatives

**Choose ALIVE** when you are following Course 1 on Claude Code and want structured, session-surviving project memory without building your own layout.

**Consider alternatives** when you use Cursor or OpenCode as your daily harness, need MCP-standard memory across clients, or are building a product that needs a memory API (Mem0/Zep) rather than a personal folder system.

**Official links:** [alivecontext.com](https://alivecontext.com/) · [GitHub — alivecontext/alive](https://github.com/alivecontext/alive)

---

## Plain markdown and project-file conventions

### What it is

You maintain a **practice folder** (or repo) of human-readable files: briefs, decision logs, `notes/`, dated journals, checklists. Each session, you attach or point the harness at the relevant files—or the harness auto-includes project docs.

This is the most portable memory pattern. It is also what ALIVE formalizes.

### Harness compatibility

**Any** harness with file access: Claude Code, Cursor, Windsurf, OpenCode, Codex, Continue, etc.

### Setup complexity

**Beginner** — create folders and filenames you can sustain.

### Tradeoffs

| Pros | Cons |
| ---- | ---- |
| No vendor lock-in; works offline | No automatic checkpoint unless you build a habit or tool |
| Trivial to audit, diff, and share via git | Retrieval is manual or RAG-dependent |
| Teaches the underlying skill Course 1 depends on | Easy to let files drift without structure |

### When to choose it vs ALIVE

**Choose plain files** when you want maximum portability, minimal tooling, or you are on a harness ALIVE does not support.

**Add ALIVE** when you want Claude Code to load and route context automatically instead of re-attaching files every session.

---

## `AGENTS.md`, `CLAUDE.md`, and harness instruction files

### What it is

Emerging **conventions for persistent instructions** checked into a repo (or a global home directory):

- **[`AGENTS.md`](https://agents.md/)** — project guidance for coding agents (build commands, style, tests). Supported by Codex, OpenCode, Cursor, and others.
- **`CLAUDE.md`** — Claude Code's project memory file (often auto-loaded; subject to size limits).
- **Harness-specific rules** — e.g. Cursor `.cursor/rules`, Claude `CLAUDE.md` / `MEMORY.md`.

These are **standing instructions and light context**, not a full decision log. They overlap with "memory" but are closer to a briefing packet than episodic recall.

### Harness compatibility

Varies by filename: `AGENTS.md` is intentionally cross-tool; `CLAUDE.md` is Claude-ecosystem; Cursor rules are Cursor-native.

### Setup complexity

**Beginner** — add a file at repo root; refine over time.

### Tradeoffs

| Pros | Cons |
| ---- | ---- |
| Version-controlled; team-visible | Size caps on some harnesses (e.g. Codex ~32 KiB combined) |
| Zero extra services | Weak for rich episodic history unless you also keep logs |
| Composes well with other options | Not a substitute for deliberate save/checkpoint habits |

### When to choose it vs ALIVE

**Choose instruction files** for stable conventions and "how we work here."

**Add ALIVE (or structured logs)** when you need session-to-session project state, decisions, and bundles—not just static rules.

**Official links:** [agents.md](https://agents.md/) · [OpenAI Codex — AGENTS.md](https://developers.openai.com/codex/guides/agents-md) · [Claude Code memory docs](https://code.claude.com/docs/en/memory)

---

## Cursor rules and skills

### What it is

**[Cursor](https://cursor.com/)** (and similar IDEs) support **rules** (project or user-level instructions) and **skills** (packaged workflows). Rules shape behavior each session; skills bundle repeatable procedures.

Functionally, this is **lightweight, editor-local memory of how you want work done**—not a general knowledge graph.

### Harness compatibility

**Cursor-first.** Other products have analogous features (Claude Code skills/plugins, Codex skills, OpenCode config) but formats differ.

### Setup complexity

**Beginner–intermediate**

### Tradeoffs

| Pros | Cons |
| ---- | ---- |
| Low friction inside Cursor | Not portable verbatim to other harnesses |
| Good for coding style and guardrails | Easy to confuse rules with factual project memory |
| Skills can encode repeatable workflows | Team sharing depends on how rules are stored |

### When to choose it vs ALIVE

**Choose Cursor rules/skills** if Cursor is your primary harness and you need behavior and workflow memory.

**Choose ALIVE** (or plain files + MCP) if you need durable **project facts and history** across tools, or you are on Claude Code for Course 1.

---

## MCP memory servers (agent-agnostic)

### What it is

The [Model Context Protocol (MCP)](https://modelcontextprotocol.io/) lets harnesses attach **standardized tools**. The official [**Knowledge Graph Memory Server**](https://github.com/modelcontextprotocol/servers/tree/main/src/memory) (`@modelcontextprotocol/server-memory`) stores entities, relations, and observations in a local graph (default: `memory.jsonl`).

Community and vendor variants exist (e.g. [Neo4j MCP memory](https://neo4j.com/developer/genai-ecosystem/model-context-protocol-mcp/) for larger graphs).

### Harness compatibility

**Any MCP client:** Claude Desktop, Claude Code, Cursor, VS Code extensions, OpenCode, and others—if MCP is enabled and the server is configured.

### Setup complexity

**Intermediate** — install server, configure MCP in the harness, understand graph tools (`create_entities`, `search_nodes`, etc.).

### Tradeoffs

| Pros | Cons |
| ---- | ---- |
| Portable across MCP-capable harnesses | More abstract than a folder of Markdown |
| Standard tool surface for agents | Quality depends on what the agent writes to the graph |
| Local default; path configurable | Another moving part to back up |

### When to choose it vs ALIVE

**Choose MCP memory** when you want **harness flexibility** and are comfortable with a graph/tool model.

**Choose ALIVE** when you want **human-readable project files** and a Claude Code–integrated checkpoint flow out of the box.

**Official links:** [MCP servers — memory](https://github.com/modelcontextprotocol/servers/tree/main/src/memory) · [npm — @modelcontextprotocol/server-memory](https://www.npmjs.com/package/@modelcontextprotocol/server-memory)

---

## Mem0

### What it is

[**Mem0**](https://mem0.ai/) is a **memory layer** for LLM applications: it extracts facts from conversations and exposes add/search APIs. Available hosted or self-hosted; integrates with several agent frameworks.

### Harness compatibility

**Application/framework layer**, not a terminal harness. Use via SDK when **you build** the agent or app. Not a drop-in replacement for ALIVE inside Claude Code without custom integration.

### Setup complexity

**Intermediate** — API keys, user/session IDs, integration code.

### Tradeoffs

| Pros | Cons |
| ---- | ---- |
| Fast to add personalization to an app | Hosted tier sends data to Mem0's cloud unless self-hosted |
| Good multi-user isolation patterns | Less transparent than plain files for non-developers |
| Broad framework support | Extraction can drift; needs monitoring |

### When to choose it vs ALIVE

**Choose Mem0** when you are **shipping a product** that needs per-user memory at scale.

**Choose ALIVE** for **personal, local, file-first** work on Claude Code (Course 1).

**Official links:** [mem0.ai](https://mem0.ai/) · [GitHub — mem0ai/mem0](https://github.com/mem0ai/mem0)

---

## Zep / Graphiti

### What it is

[**Zep**](https://www.getzep.com/) is a **memory platform** built around temporal knowledge graphs. [**Graphiti**](https://github.com/getzep/graphiti) (open source) models entities and facts with validity over time—useful when "what was true in March?" matters.

### Harness compatibility

Backend **service + SDK**. Agents or apps call Zep; not a Claude Code plugin equivalent.

### Setup complexity

**Intermediate–advanced** — graph storage, extraction pipeline, more ops if self-hosted.

### Tradeoffs

| Pros | Cons |
| ---- | ---- |
| Strong for changing facts and relationships | Heavier than Markdown folders or Mem0 for simple prefs |
| Enterprise-oriented features on managed offering | Overkill for solo practice-folder workflows |
| Open-source graph core available | Requires engineering investment |

### When to choose it vs ALIVE

**Choose Zep/Graphiti** for **time-aware, entity-heavy** production systems (support, CRM, compliance trails).

**Choose ALIVE** for **individual project continuity** with files you can read without a graph query language.

**Official links:** [getzep.com](https://www.getzep.com/) · [Graphiti on GitHub](https://github.com/getzep/graphiti)

---

## Letta (formerly MemGPT)

### What it is

[**Letta**](https://www.letta.com/) is an **agent runtime** where memory is tiered (core context vs archival) and the agent can edit memory via tools—the MemGPT research line. Includes hosted cloud and open-source server; **Letta Code** targets coding-agent use cases.

### Harness compatibility

**Letta as the runtime**—you adopt Letta's agent model rather than bolting memory onto Claude Code alone.

### Setup complexity

**Intermediate–advanced**

### Tradeoffs

| Pros | Cons |
| ---- | ---- |
| Memory is first-class in the architecture | Not a thin plugin; different operational model |
| Good for long-lived autonomous agents | More moving parts than ALIVE + files |
| Self-host option (Apache 2.0 core) | Learning curve for memory blocks and tool semantics |

### When to choose it vs ALIVE

**Choose Letta** when you are building **stateful, long-running agents** where memory management is core to the product.

**Choose ALIVE** for Course 1's **simple local checkpoint** pattern on Claude Code.

**Official links:** [letta.com](https://www.letta.com/) · [GitHub — letta-ai/letta](https://github.com/letta-ai/letta)

---

## OpenMemory

### What it is

[**OpenMemory**](https://github.com/CaviraOSS/OpenMemory) is a **self-hosted cognitive memory engine** (Python and Node SDKs) with multi-sector memory, optional temporal graph features, and an **MCP server** for clients like Claude Desktop and Cursor.

### Harness compatibility

SDK integrations, MCP clients, or embedded in custom apps. Not Claude Code–native like ALIVE.

### Setup complexity

**Intermediate** — local SQLite by default; more config for Postgres/service mode.

### Tradeoffs

| Pros | Cons |
| ---- | ---- |
| Local-first; inspectable storage | Younger ecosystem than Mem0/Zep |
| MCP path for portable clients | More concepts than "a folder of notes" |
| Explainable recall traces (per project docs) | Another system to operate |

### When to choose it vs ALIVE

**Choose OpenMemory** if you want a **self-hosted memory service** with MCP and multi-sector recall, and you are willing to run infrastructure.

**Choose ALIVE** for **Claude Code–integrated, Markdown-native** project context with minimal setup.

**Official links:** [GitHub — CaviraOSS/OpenMemory](https://github.com/CaviraOSS/OpenMemory)

---

## Harness alternatives (context for memory choices)

Course 1 demonstrates **Claude Code**, but the **model vs harness** lesson applies broadly. Real coding-agent harnesses learners may already use:

| Harness | Notes |
| ------- | ----- |
| **[Claude Code](https://code.claude.com/docs/en/quickstart)** | Course 1 default; ALIVE plugin; `CLAUDE.md` |
| **[Cursor](https://cursor.com/)** | IDE-integrated; rules and skills; MCP |
| **[Windsurf](https://windsurf.com/)** | IDE agent; Cascade flows; MCP |
| **[OpenCode](https://opencode.ai/)** | Open-source, model-agnostic terminal/IDE harness; `AGENTS.md`, MCP |
| **[OpenAI Codex](https://developers.openai.com/codex)** | CLI/TUI agent; `AGENTS.md`, skills, MCP |
| **[Continue](https://www.continue.dev/)** | Open-source IDE extension; configurable models and context |

Switching harness changes default context assembly, tool access, and which memory patterns are one command away. The **underlying lesson**—save important state in inspectable form and reload it deliberately—does not.

---

## Decision guide

```
Need memory for Course 1 on Claude Code?
  └─ Yes → ALIVE (lesson path) + plain files habit

Primary harness is not Claude Code?
  └─ Start with AGENTS.md / project markdown + harness rules
  └─ Add MCP memory server if your client supports MCP well

Building a product for many end-users?
  └─ Evaluate Mem0 or Zep APIs (or self-host)
  └─ Not ALIVE alone

Building long-running autonomous agents?
  └─ Evaluate Letta or custom runtime + memory tools

Must stay 100% local and file-readable?
  └─ Plain markdown logs, ALIVE, MCP memory.jsonl, or OpenMemory (self-hosted)
```

---

## What we deliberately did not list

- **Vector databases alone** (Pinecone, Weaviate, etc.) — storage/retrieval layers, not end-to-end memory products; pair with an app pattern or RAG.
- **Chat product "memory" toggles** — convenient but opaque, vendor-specific, and weak for project audit trails.
- **Team shared memory** — out of scope for Course 1; see Course 2 boundary.

---

## Maintenance notes for instructors

- Re-verify install commands and URLs before each recording season.
- ALIVE's cross-harness roadmap may change; update this doc if stable adapters ship.
- When demoing alternatives, keep the same **acceptance test** as Lesson 8: save one fact, new session, ask a question only answerable from saved context.
