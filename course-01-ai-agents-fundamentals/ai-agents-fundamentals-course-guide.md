---
course_id: ai-agents-fundamentals
document_type: production-guide
status: production-draft
source_curriculum: course-01-curriculum.html
last_updated: "2026-07-21"
---

# AI Agents Fundamentals: Course Guide

This is the internal design and production reference for **AI Agents Fundamentals**. It defines why the course exists, how it should be taught, and how the curriculum should be evaluated and maintained. It is not intended to be read aloud or converted directly into slides; the companion [`course-01-curriculum.html`](./course-01-curriculum.html) is the canonical curriculum for recording and slide production, and the **source of truth** for Google Slides generation. Use each lesson's collapsible **Slides (draft)** section (title + bullets, per-slide 16-bit pixel-art visual brief, optional side-panel terms, instructor screen-share note). Brand is applied later outside this HTML.

## Course context

### Reality check

- **Why a course?** Learners need a guided sequence that combines concepts, setup, practice, feedback, and a complete supervised workflow. A glossary or tutorial would explain isolated features but would not create the intended behavior change.
- **Performance gap:** Learners have tried chat-based AI, but their work is fragmented, poorly briefed, difficult to verify, and disconnected between sessions.
- **Desired change:** Learners move from casual prompting to defining, supervising, verifying, and improving small AI-assisted workflows.
- **Audience:** Non-technical and lightly technical entrepreneurs, creators, coaches, independent professionals, and small teams.
- **Need to validate:** Pilot interviews should confirm which setup steps, concepts, and first workflows cause the most friction before the course is marked final.

### Place in the course sequence

This is the foundation course, scoped around a **complete local, single-user setup**: Claude Desktop as the primary assistant for beginners, grounding in context/memory/RAG, tools vs skills vs plugins, a careful skill install, ALIVE for local memory (via Claude Code plugins in later lessons), data-sharing awareness, MCP at recognition level, and one supervised working loop. The course closes by naming its own boundary: everything here works for one person on one machine. Shared team context, multi-user access control, business context, brand systems, and coaching routines belong in **AI Agents for Your Business**, rebuilt around that local-vs-team boundary rather than simply continuing where this course leaves off.

### Observable course outcomes

By the end, learners should be able to:

1. Explain the practical differences among a model, AI application (harness), assistant, workflow, automation, and agent, and how a modern chat turn actually runs.
2. Set up Claude Desktop on macOS, extend the assistant with a new skill, and give it focused task context using ordinary files.
3. Explain what gets shared with whom, including the practical difference between a locally-running model and a cloud API, well enough to make deliberate, cautious choices about sensitive information.
4. Explain why an assistant has no persistent memory by default, what retrieval-augmented generation (RAG) does, and complete a basic ALIVE local memory setup.
5. Give, review, verify, and improve an AI assignment using explicit sources, constraints, deliverables, and success criteria.
6. Complete a low-risk supervised workflow with appropriate permissions and human approval points, and explain why a local, single-user setup is a different problem from a shared team setup.

Lesson objectives in `course-01-curriculum.html` break these outcomes into smaller, observable skills. Each lesson is also scoped as a 2–5 minute standalone promo clip where practical (Lesson 2 is theory before install; Lesson 3 is a short hands-on setup). Outcome 4's hands-on counterpart is Lesson 11 (ALIVE setup), after tools/skills/plugins vocabulary and a careful skill install, in the ~60-minute core.

## Instructional design approach

The course uses backward design: the practical behavior expected at the end determines the lessons, examples, activities, and capstone. Concepts are included only when they help the learner make a better decision or perform the final workflow.

### Design principles

1. **One clear outcome per lesson.** Every lesson has a single main behavior or decision the learner should be able to perform.
2. **Progress from mental model to action.** Learners first understand the system, then its information, then its capabilities (tools/skills/plugins), then how to extend and supervise it, and finally how to complete a workflow. Lesson 2 is theory only (what models and harnesses do); Lesson 3 is the install, so setup has meaning after the mental model. ALIVE and MCP come only after plugin vocabulary is clear.
3. **Keep cognitive load low.** New terminology is grouped by function and anchored to one consistent analogy.
4. **Use realistic business examples.** Abstract concepts are demonstrated through briefs, research, planning, drafting, and review.
5. **Correct misconceptions explicitly.** Each lesson names a common false belief and replaces it with a usable rule.
6. **Require a small learner output.** Every module ends with a decision, artifact, or check that contributes to the final workflow.
7. **Teach supervision, not blind trust.** The learner remains accountable for scope, permissions, evidence, and final approval.
8. **Prefer familiar foundations.** Use ordinary files and off-the-shelf product features before introducing integrations or memory infrastructure.
9. **Use retrieval practice.** Short "Can you explain or decide this?" checks help learners recall ideas instead of only recognizing them.
10. **Align the final assessment with the promise.** The capstone requires setup, delegation, tool awareness, review, and revision.

### Standard lesson pattern

Each recorded lesson should follow this five-part pattern:

1. **Orient:** State the practical question the lesson answers.
2. **Explain:** Introduce one mental model or method in plain language.
3. **Correct:** Address one or two likely misconceptions.
4. **Demonstrate or decide:** Show a small example, or ask the learner to make a decision.
5. **Close:** Give one memorable rule and connect it to the next lesson.

This pattern is a teaching scaffold, not a word-for-word script.

### Learning rhythm

Every module should include three forms of learner effort:

1. **Example:** Show the behavior or decision in a realistic business context.
2. **Practice:** Ask the learner to produce a small artifact, classification, or decision.
3. **Reflection and retrieval:** Ask the learner to explain a distinction, justify a choice, or retrieve prior knowledge without simply rereading it.

Distribute checks throughout the course rather than relying on a single final quiz. Give immediate, specific feedback through worked answers, comparison criteria, or a short rubric. Revisit the core loop (context → assignment → action → review) several times so recall is spaced and cumulative.

## Consistent course mental model

Use this analogy throughout the course:

| Element      | Plain-language analogy              | What it contributes                                                                 |
| ------------ | ----------------------------------- | ----------------------------------------------------------------------------------- |
| Model        | Brain or reasoning engine           | Generates, analyzes, predicts, and transforms information. It does not execute tools by itself. |
| Harness / app| Workplace and hands around the brain| Assembles context, runs the chat/tool loop, executes tools, and enforces permissions. |
| Instructions | Job description and operating rules | Defines role, priorities, process, constraints, and standards.                      |
| Context      | Current workbench                   | Holds the information available for this task or conversation.                      |
| Memory       | Notebook or knowledge system        | Preserves selected information for later use.                                       |
| Tools        | Hands                               | Let the system search, calculate, read, write, send, or change something.           |
| Skills       | Playbooks                           | Describe how to perform a recurring type of work well.                              |
| MCP          | Standard connection layer           | Gives compatible assistants a common way to discover and use external capabilities. |
| Guardrails   | Permissions and boundaries          | Restrict what can happen and where approval is required.                            |
| Human        | Accountable owner                   | Defines the goal, provides judgment, verifies results, and approves consequences.   |

The anatomy of a useful agent is therefore:

> Goal + instructions + context + memory + tools + boundaries + review.

## Terminology policy

Use terms consistently across videos, worksheets, and slides.

**Glossary scope in the curriculum HTML:** per-lesson glossaries list only technical or AI/agent-specific terms (for example harness, token, context window, MCP). Everyday words used in teaching (practice task, deliverable, source pack) stay in the lesson body but are not glossary entries.

| Term              | Course definition                                                                                                           |
| ----------------- | --------------------------------------------------------------------------------------------------------------------------- |
| AI model          | The underlying system that processes input and generates output.                                                            |
| LLM               | A language-focused model trained to work with text and related representations.                                             |
| Multimodal model  | A model that can work with more than one type of input or output, such as text, images, audio, or video.                    |
| Harness / AI application | The software around the model: UI, context assembly, tool execution, history, integrations, and permissions. Same idea as "app," "runtime," or "scaffold." |
| Assistant         | The working experience when a model is combined with a harness, instructions, context, and available capabilities.           |
| Tool call         | A structured request from the model to use a capability; the harness runs it (if allowed) and returns the result.            |
| Workflow          | A defined sequence of steps used to produce an outcome.                                                                     |
| Automation        | A workflow triggered and executed according to predefined rules, usually with limited judgment.                             |
| Agent             | A goal-directed system that can choose and perform multiple steps, often using tools, within defined boundaries.            |
| Prompt            | The immediate input or request given to the model.                                                                          |
| Instructions      | Persistent or task-level guidance that shapes behavior beyond one isolated request.                                         |
| Token             | A small unit used by models to process text and other encoded information; it is not always a whole word.                   |
| Context           | The information made available to the model for the current task.                                                           |
| Context window    | The finite amount of information the model can consider in one model call.                                                  |
| Chat history      | A record of messages; it may be used as context, but it is not automatically reliable memory.                               |
| Memory            | A mechanism for preserving selected information and making it available later.                                              |
| Knowledge source  | A document, database, page, or other source the system can consult.                                                         |
| Retrieval         | The process of finding relevant information for the current task.                                                           |
| RAG               | Retrieval-augmented generation: retrieving relevant source material and adding it to the model's context before generation. |
| Embedding         | A numeric representation used to compare meaning or similarity.                                                             |
| Vector search     | A way of finding semantically similar material using embeddings.                                                            |
| Knowledge graph   | Structured entities and relationships that make connections explicit.                                                       |
| Tool              | A capability the assistant can invoke to observe or change something.                                                       |
| Skill             | Reusable instructions, standards, examples, or procedures for a type of work.                                               |
| Connector         | An integration that links the assistant to another service or data source.                                                  |
| API               | A defined interface through which software systems communicate.                                                             |
| MCP               | Model Context Protocol, a standard way for compatible AI clients to discover and use external resources and tools.          |
| Guardrail         | A technical or procedural control that limits behavior.                                                                     |
| Sandbox           | A restricted environment that limits the effect of actions.                                                                 |
| Human in the loop | A person reviews, approves, corrects, or intervenes at defined points.                                                      |
| Evaluation        | A repeatable way to test whether an output or workflow meets its standard.                                                  |

# Assessment plan

## Formative checks

Use low-friction checks throughout the course. They should not add significant video runtime.

| Point           | Check                                                  | Evidence of learning                                                     |
| --------------- | ------------------------------------------------------ | ------------------------------------------------------------------------ |
| After Lesson 2  | Explain model versus harness/app in one sentence, and sketch one chat turn. | The foundational distinction and chat/tool loop are understood. |
| After Lesson 3  | Open Claude Desktop and confirm a simple prompt works with a chosen workspace folder. | The harness is installed and usable. |
| After Lesson 4  | Complete the Chat and Code tries from Lesson 4. Say what changed on your Mac in each part and who controlled the steps. | The learner can tell one-answer chat from multi-step, file-changing work in Claude Desktop. |
| After Lesson 6  | Explain in one sentence why the assistant won't remember them next session without help. | Statelessness is understood. |
| After Lesson 7  | Explain RAG in one sentence and name one limit. | RAG is distinguished from memory. |
| After Lesson 8  | Explain tools vs skills vs plugins/connections in one sentence each. | Capability vocabulary is clear before installs. |
| After Lesson 9  | Evaluate one skill listing (real or the course showcase example) before installing it, including author/source when discovered via directories like [skills.sh](https://skills.sh). | The learner treats new skills as a deliberate, reviewed choice, not a default install. |
| After Lesson 10 | Write one stop-and-ask rule.                           | Permissions and human checkpoints are explicit.                          |
| After Lesson 11 | Complete ALIVE install (including quick Python check) and confirm a saved item returns in a fresh session. | Local memory plugin works in practice. |
| After Lesson 12 | State one personal rule for what not to share, and explain the local-model-vs-cloud-API distinction in one sentence. | Data-sharing awareness is practical, not just theoretical. |
| After Lesson 13 | Explain what MCP is in one sentence. | MCP is recognized as a connection standard, not memory. |
| After Lesson 14 | Complete a CLEAR assignment.                           | The task is executable and reviewable.                                   |
| After Lesson 15 | Revise an output using diagnostic feedback.            | The learner can supervise quality.                                       |
| After Lesson 17 | State in one sentence what this setup covers and what it deliberately does not. | The local-vs-team boundary is understood, not just heard.                |

## Final practical check

Using a supplied one-page business brief, the learner asks the assistant to plan and create a short artifact, verifies it against the brief, and revises it once before final approval.

### Capstone success rubric

| Criterion            | Successful evidence                                                |
| -------------------- | ------------------------------------------------------------------ |
| Outcome clarity      | The requested artifact and intended audience are explicit.         |
| Context quality      | Only relevant sources are provided and their authority is labeled. |
| Boundaries           | Constraints, non-goals, and approval points are stated.            |
| Capability awareness | The learner can explain which skills and tools are required.       |
| Verification         | Claims and requirements are checked against the brief.             |
| Feedback             | At least one revision is requested with diagnostic reasoning.      |

# Tool setup and implementation guidance

## Recommended teaching posture

- Teach concepts and architecture in provider-neutral language where possible.
- Demonstrate **Claude Desktop** as the primary assistant for Lesson 3 and early hands-on work; **Claude Code** appears later for plugins (skills, ALIVE).
- **Lesson 2 sequence (required, theory only, no install):** what a model does (next-token / text generation) → named model families (concrete, dated "as of recording") → harness / app / assistant vs model; Claude Desktop = the harness we'll install → one chat turn (model requests → harness runs tools) → bridge: next we install the harness.
- **Lesson 3 sequence (required), numbered learner path:** (0) minimum stack in plain language (Claude Desktop + one workspace folder + one harmless starter brief) with a brief opening caution woven in (access ≠ authority; keep first session non-sensitive) and CLI named as vocabulary only (not a step) → (1) download & install Claude Desktop from [claude.com/product/claude-code](https://claude.com/product/claude-code) (Download for Mac; sign in on first launch; paid plan or Console required) → (2) create workspace in Finder (new folder per project, or one Personal OS directory; explain the difference orally) → (3) confirm it works with a simple prompt → close toward agents; tools/skills/plugins and ALIVE come later. Install before folder. Do not open with install commands or Terminal. Official links: [claude.com/product/claude-code](https://claude.com/product/claude-code) · [claude.com/pricing](https://claude.com/pricing).
- **Capability ladder (required order):** tools vs skills vs plugins/connections (Lesson 8) → carefully install/review a skill with [skills.sh](https://skills.sh) author checks (Lesson 9) → approvals / least privilege (Lesson 10) → **ALIVE** as first meaningful plugin for local memory (Lesson 11) → data-sharing judgment (Lesson 12) → MCP at recognition level (Lesson 13). Do not teach ALIVE or MCP before the vocabulary lesson.
- Use **ALIVE** by name for the hands-on local memory lesson (Lesson 11): a Claude Code plugin that stores persistent local memory on disk. Lesson 3's folder guidance (project folders vs Personal OS) should foreshadow that without teaching the full ALIVE lesson early.
- When naming tools or brands, say what they *are* (the job they do): harness, local files, memory layer, cloud API, assistant UI, not random name-drops.
- Provide a separate translation sheet only where product differences would block learners on other assistants.
- Demonstrate file-aware work using ordinary, human-readable files in a dedicated workspace.
- Teach why persistent memory doesn't exist by default and what RAG is before extensions; teach MCP at recognition level only after skills/plugins are clear (dedicated ~3 min MCP lesson).
- Give every learner a no-integration path for conceptual lessons so product differences do not block learning.

## Minimum tool stack

| Layer | Course requirement | Acceptable implementation |
| ----- | ------------------ | ------------------------- |
| Assistant | Claude Desktop on macOS with file access | Primary beginner demo environment; Claude Code for plugins (ALIVE, skills) in later lessons |
| Workspace | Human-readable learner-owned files | New folder per project, or one general Personal OS directory for a personal-assistant style setup |
| Editing | Direct inspection and correction | Built-in editor or any familiar text editor |
| Course assets | Brief, worksheet, and checklists | Downloadable Markdown or PDF files |

## Lesson 3 setup path (step-by-step)

Teach and demo in this order. Every installable/openable tool gets a one-line role, an official URL, and the exact action already used in the slides.

| Step | What to do | What this is | Link / action |
| ---- | ---------- | ------------ | -------------- |
| · | Know the minimum stack | Claude Desktop (harness) + one workspace folder + one harmless starter brief. Brief opening caution: keep first session non-sensitive; file access ≠ permission to share secrets. CLI named as vocabulary only (command-line install exists in docs; not our beginner step). | [claude.com/product/claude-code](https://claude.com/product/claude-code) |
| 1 | Download & install Claude Desktop | Mac app from the product page. Sign in on first launch. Sign-in needs a paid Claude plan or Console. | [claude.com/product/claude-code](https://claude.com/product/claude-code) → Download for Mac · [claude.com/pricing](https://claude.com/pricing) |
| 2 | Create your workspace | A new folder per project, **or** one general Personal OS directory. Explain the difference orally; keep slides brief. | Create in Finder (File → New Folder) |
| 3 | Confirm it works | Try a simple prompt, confirm a reply. Optional: summarize a harmless starter brief. | Example prompt: `Reply with one sentence: setup works.` |

**Intentionally not in Lesson 3:** Terminal / CLI install (`curl install.sh`, `claude` command) as a taught step; Node.js/npm; Homebrew; Python / ALIVE / skills (Lessons 8–11). Other install methods exist in docs; the beginner path is Desktop only.

## Setup quick check

After Lesson 3, the learner should be able to:

1. Open Claude Desktop and have a chosen workspace folder ready (project folder or Personal OS directory).
2. Try a simple prompt and confirm a reply comes back.
3. Optionally: attach a harmless starter brief and ask for a short summary. Inspect the result outside chat if they created a draft.
4. Keep sensitive material out of this first session.

## Ordinary-file fallback

If project or workspace features are unavailable, the learner should still be able to complete the course by:

1. Opening the course context folder.
2. Attaching or selecting the relevant files for the task.
3. Giving a CLEAR assignment in an ordinary conversation.
4. Saving the reviewed output as a separate file.

The fallback reinforces the foundation: useful work depends on clear context, a defined assignment, and human review, not on a particular product feature.

# Required course assets

Prepare these assets before recording:

1. **AI lingo field guide.** Short definitions, comparisons, and misconception corrections.
2. **CLEAR assignment worksheet.** A one-page fillable assignment planner.
3. **Context checklist.** Outcome, audience, sources, constraints, example, deliverable, standard, and questions.
4. **Capability and permission map.** Workflow step, information, skill, tool, permission, and approval.
5. **Workspace starter.** A starter brief, source note, and safe destination for drafts in a new project folder or a Personal OS directory.
6. **Source-label template.** Approved, reference, draft, outdated, and archive labels.
7. **Lightweight evaluation checklist.** Facts, instruction-following, quality, preference, risk, and approval.
8. **Assistant translation sheet.** Equivalent setup concepts and product-specific terminology.
9. **Troubleshooting guide.** Account, file-access, permission, and ordinary-file fallback checks.
10. **Capstone brief.** One-page fictional business brief with enough information for a small reviewed artifact.
11. **Data-sharing quick-reference.** A one-page local-vs-cloud comparison plus a short list of what to withhold by default.
12. **Skill showcase example.** Keep the literal placeholder label (`[Skill Name TBD: branding/business-coach skill]`) until the final skill/name is supplied. Use it only to demonstrate discovery, review, and install via the skills command. In Lesson 9, point learners to [skills.sh](https://skills.sh) as one place to discover skills, and reinforce that installs carry risk: verify the author, prefer official skills from reputable teams, and review what a package claims to do before installing.
13. **ALIVE setup companion.** Install steps, `/alive:world`, `/alive:save`, and a fresh-session confirm for Lesson 11.

## Reference documentation

| Document | Purpose |
| -------- | ------- |
| [`docs/local-memory-alternatives.md`](./docs/local-memory-alternatives.md) | Agent-agnostic and harness-portable memory options (plain files, MCP-based memory, and other persistent local or synced memory layers); tradeoffs vs the Course 1 ALIVE + Claude Code path. Point curious learners and instructors here from Lessons 2, 3, and 11. |

# Guidance for the slide-generation agent

This section describes how a later agent should translate the curriculum into lesson slides. Prefer the **Slides (draft)** block in each lesson of `course-01-curriculum.html` (concrete draft cards with titles and bullets; **one 16-bit pixel-art visual brief per content slide**; optional side panel of technical terms + ultra-short defs; screen-share as an instructor note only) over regenerating structure from this guide alone. Do not invent a brand system in the slides. Brand is applied later.

## Slide principles

- Preserve the lesson objective, runtime, learner output, and closing rule.
- Give every content slide its own visual brief that reinforces that slide's teaching point (16-bit pixel art; diagram-like and concrete).
- When the slide introduces technical terms, include a side panel with only those terms and ultra-short definitions (prefer lesson glossary wording).
- Avoid turning every teaching point into a bullet slide.
- Prefer diagrams, comparisons, annotated examples, checklists, and before/after artifacts.
- Keep terminology identical to the definitions in this document.
- Label examples as fictional unless they come from an approved real source.
- Do not add product claims, prices, screenshots, or interface instructions without current verification.
- Do not imply that memory, RAG, MCP, embeddings, or knowledge graphs guarantee correctness.
- Keep branding and content examples deliberately shallow; they are bridges to the next course.
- Make human approval visually explicit wherever an external or consequential action appears.
- Preserve placeholders exactly as written in the curriculum HTML (skill name) until the production team supplies a final name. Do not invent a name to fill a slide.

## Suggested slide count

Use approximately one slide per minute, but let the content determine the final count. A two-minute demonstration may need three quick screens; a six-minute conceptual lesson may use four or five slides plus a live demonstration.

| Lesson type   | Suggested structure                                            |
| ------------- | -------------------------------------------------------------- |
| Concept       | Question → mental model → misconception → example → rule       |
| Comparison    | Definitions → comparison table → decision rule → learner check |
| Demonstration | Starting state → action sequence → verification → result       |
| Method        | Framework → worked example → learner template → closing rule   |

## Slide metadata to retain

For every slide deck, retain:

- Course title and module number.
- Lesson number and title.
- Lesson objective.
- Estimated runtime.
- Required learner action.
- Source or evidence notes for factual claims.
- Demonstration prerequisites.
- Closing rule and next-lesson transition.

# Recording and facilitation notes

## Tone

- Calm, practical, and non-alarmist.
- Respect the learner's business judgment.
- Avoid anthropomorphic claims and exaggerated promises.
- Define jargon immediately, then return to plain language.
- Use "the assistant may" or "the product can" instead of implying universal behavior.

## Recording discipline

- Open each lesson with the question it answers.
- Keep one example consistent across the full course.
- Explain what the learner should notice during every demonstration.
- Pause or add an on-screen prompt when a learner action is required.
- End every lesson with the reusable rule listed in its brief.
- Avoid interface details that are likely to age quickly in conceptual lessons.
- Record setup screens separately where possible so they can be replaced without re-recording the conceptual explanation.
- For Lesson 2 (theory) and Lesson 3 (install), record separately so either can be updated without re-shooting both.

## Accessibility and comprehension

- Spell out an acronym before using it repeatedly.
- Display important definitions on screen as they are introduced.
- Use captions and provide the lingo field guide as text.
- Do not rely on color alone to distinguish permissions, status, or risk.
- Keep diagrams readable at small screen sizes.
- Describe essential visual information aloud.
- Give learners a downloadable transcript or detailed lesson notes where possible.

# Common misconceptions index

Use this list to ensure the course corrects the misunderstandings most likely to cause poor results or unsafe behavior.

- The model and the AI product (harness) are the same thing.
- The model itself executes tools, searches the web, or edits files.
- A bigger or newer model remembers more about the user personally.
- Chat history is reliable long-term memory.
- A large context window produces perfect recall.
- More context always improves results.
- RAG is the same as memory.
- RAG prevents hallucinations.
- Embedding similarity proves truth or authority.
- A knowledge graph is automatically more accurate than source files.
- A skill is the same as a tool.
- MCP is a memory system.
- A connected tool will automatically be selected and used correctly.
- More tools make a better agent.
- The agent permanently learns from every correction.
- Instructions enforce security.
- Sandboxing guarantees correctness or harmlessness.
- More autonomy is always more useful.
- Prompting is mainly clever wording.
- A confident or well-written answer is a verified answer.
- The agent's summary is an objective record of what happened.
- A locally-running model and a cloud API call carry the same data-exposure risk.
- Anything shared with an AI product stays only inside that one conversation.
- Installing a skill is the same as installing harmless documentation. It deserves no more scrutiny than reading a paragraph.
- A local, single-user memory or delegation setup will keep working unchanged once a second person needs it too.

# Pre-production decisions

Resolve these items before the setup lesson and screenshots are recorded:

1. Select the primary demonstrated assistant interface.
2. Confirm that the ordinary-file fallback completes the same learning objectives.
3. Create the fictional capstone business brief.
4. Define the exact list of sensitive data learners must exclude from exercises.
5. Test setup, file access, draft creation, correction, and permission removal on a clean learner account.
6. Decide which interface-specific setup details belong in replaceable companion videos.
7. Verify all product names, screenshots, availability, and plan requirements immediately before recording.

# Evaluation and iteration

Pilot the course with a small group from the intended audience before final recording. Observe behavior as well as collecting opinions.

## Pilot evidence

- Can learners choose a safe, appropriately narrow practice task without help?
- Can they explain the model–harness/app–assistant distinction and sketch one chat/tool turn in their own words?
- Can they open Claude Desktop and confirm a simple prompt works on a clean account?
- Can they produce a usable CLEAR assignment without copying the instructor example?
- Can they identify a meaningful approval point and verify a claim against a source?
- Where do they pause, replay, abandon, or ask for help?

## Revision loop

1. Pilot with 3–5 representative learners.
2. Record completion, errors, questions, and time-on-task for each lesson output.
3. Compare results with the four course outcomes and capstone rubric.
4. Remove unnecessary explanation before adding more content.
5. Improve examples, practice, feedback, or sequencing where learners fail.
6. Re-test changed lessons and review time-sensitive product instructions before release.
7. Schedule periodic checks for screenshots, product names, access requirements, and terminology.

# Curriculum alignment map

| Course outcome | Primary lessons | Demonstrated by |
| -------------- | --------------- | --------------- |
| Explain models, harnesses/apps, assistants, workflows, automations, and agents (including one chat turn) | 2–4 | Lesson 2 teaches model vs harness and one chat turn; Lesson 4 teaches agent vs workflow |
| Set up an assistant, install a new skill, and provide focused context with ordinary files | 3, 5, 8–9, 11 | Lesson 3 Claude Desktop install + verify, context checklist, tools/skills/plugins map, one deliberately installed skill, ALIVE memory |
| Explain data sharing (local vs. cloud) well enough to make cautious choices | 12 | One stated personal rule for what not to share |
| Explain why memory isn't persistent by default, and what RAG does | 6–7, 11 | Classification examples, plain-language RAG, then ALIVE as the practical local-memory plugin |
| Give, review, verify, and improve a well-sourced assignment | 14–15 | CLEAR worksheet, source pack, and diagnostic revision |
| Complete a low-risk workflow with approval points, and explain the local-vs-team boundary | 4, 10, 16–17 | Chat vs Code exercise (one answer vs multi-step local action), stop-and-ask rule, reviewed capstone artifact, and one-sentence scope statement |

# Design source

This guide incorporates the course creator's Notion page, [How to design a course](https://app.notion.com/p/ecovirtual/How-to-design-a-course-25ab9164a01f8087a473e53dc68de3a6), reviewed on 2026-07-20. Its key requirements are reflected here: validate the need and desired performance change, define a small set of course outcomes plus lesson-level objectives, progress from simple to complex, manage cognitive load, activate prior knowledge, combine examples with practice and reflection, use frequent retrieval and timely feedback, support accessibility and inclusion, pilot with a small group, measure the outcomes, and iterate regularly.
