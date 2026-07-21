# AI Agents Courses

This repository contains the source curricula for two courses:

1. **AI Agents Fundamentals**  
   *Set up an AI assistant, assign real work, and supervise the result—entirely on your own machine*  
   [Course curriculum](course-01-ai-agents-fundamentals/course-01-curriculum.html) · [Course guide](course-01-ai-agents-fundamentals/ai-agents-fundamentals-course-guide.md) · [Memory alternatives](docs/local-memory-alternatives.md)  
   Canonical teaching surface: the HTML curriculum (6 modules · 17 lessons · 61 min core). Claude Code + ALIVE for local memory. Each lesson is also scoped as a 2–5 min standalone promo clip. The course is scoped as a complete **local, single-user** setup and closes by naming that boundary explicitly. The long-form outline below is an earlier expanded draft that predates this scope and does not match the current module/lesson structure—treat the HTML as the only source of truth and disregard the outline below where it conflicts.

2. **AI Agents for Your Business**  
   *Build a persistent, shared AI workspace for strategy, brand, content, and execution*  
   [Course curriculum](course-02-ai-agents-for-your-business/course-02-curriculum.html)  
   Reserved for team-scale and shared/multi-user concerns (shared context, access control, persistent team memory) that Course 1 deliberately does not cover. To be redone around that boundary in a future pass.

---

---
course_id: ai-agents-foundations
title: "AI Assistants & Agents: The Practical Foundations"
subtitle: "Understand, set up, and work effectively with a modern AI collaborator"
version: "1.0"
status: "Production draft"
audience: "Non-technical entrepreneurs, creators, coaches, independent professionals, and small-business teams"
delivery_format: "Self-paced video course"
total_runtime_minutes: 60
module_count: 7
lesson_count: 15
lesson_duration_minutes: "2–6"
knowledge_level: "Beginner; no technical background required"
primary_outcome: "Learners can safely set up an AI assistant, give it a well-formed assignment, supervise its work, and maintain useful context across sessions."
document_purpose:
  - "Instructor recording guide"
  - "Curriculum definition"
  - "Source document for slide generation"
last_updated: "2026-07-20"
---

# AI Assistants & Agents: The Practical Foundations

## Course promise

In 60 minutes, learners will replace vague ideas about “AI magic” with a practical mental model of AI assistants and agents. They will set up a working environment, understand the language used around modern AI, learn a reliable method for assigning work, supervise a small workflow, and create the foundation for portable long-term context.

The course is intentionally general. Brand building, content systems, and entrepreneurship coaching appear as examples, but their strategy and implementation belong in the follow-on courses.

## Course description

This is a concise, non-technical introduction to working with modern AI assistants and agents. It is designed for entrepreneurs and business users who have experimented with chat-based AI but do not yet have a dependable way to use it for real work.

Learners will understand the difference between a model, an AI application (harness), an assistant, a workflow, an automation, and an agent—and how a modern chat turn runs (context → model → optional tools via the harness → response). They will learn the practical meaning of context, context windows, memory, retrieval-augmented generation (RAG), embeddings, knowledge graphs, tools, skills, connectors, APIs, and the Model Context Protocol (MCP). They will also learn where these concepts overlap, where they do not, and why the distinctions matter.

By the end, learners will have a simple working system: one AI assistant, one owned context workspace, one repeatable way to delegate, one set of safety rules, and one completed supervised workflow. The memory implementation may change over time, but the underlying knowledge remains portable and inspectable.

## Learner transformation

### Before the course

The learner may:

- Treat every AI product as if it were “the model,” ignoring the harness/app around it.
- Use chat as a sequence of disconnected questions, without seeing the tool/context loop.
- Assume the assistant remembers everything or learns permanently from corrections.
- Add more context, tools, or autonomy without understanding the tradeoffs.
- Judge an answer by how confident or polished it sounds.
- Repeatedly re-explain their business, goals, audience, or preferences.
- Feel unsure about what an agent should be allowed to read, change, or publish.

### After the course

The learner can:

- Describe what the model does and what the surrounding harness/app adds (including the chat/tool loop).
- Choose between a simple chat, a reusable skill, a workflow, an automation, and an agent.
- Give a clear assignment with the right context, constraints, sources, and success criteria.
- Recognize the limits of context windows, retrieval, and memory.
- Inspect capabilities and define approval points before an agent acts.
- Save confirmed knowledge in a structured, portable context system.
- Review the assistant’s work as the accountable owner of the outcome.

## Intended audience

This course is for:

- Entrepreneurs and small-business owners.
- Independent professionals, consultants, and coaches.
- Creators and personal-brand builders.
- Operators and small teams beginning to use AI in daily work.
- Non-technical or lightly technical users who have tried ChatGPT, Claude, or a similar assistant.
- People who want useful continuity across sessions without giving up ownership of their knowledge.

This course is not aimed at software engineers building agent infrastructure, although the mental models remain relevant to them.

## Prerequisites

Learners need:

- A laptop and permission to install or connect the selected tools.
- An account for one supported AI assistant.
- A folder or workspace in which course context can be stored.
- One real but non-sensitive business task to use during the exercises.

Learners do **not** need coding, API, database, or command-line experience.

## Learning objectives

By the end of the course, learners will be able to:

1. Distinguish a model, AI application (harness), assistant, workflow, automation, and agent—and explain how one modern chat turn runs.
2. Explain context, context windows, memory, RAG, embeddings, and knowledge graphs in plain language.
3. Differentiate instructions, skills, tools, connectors, APIs, and MCP.
4. Identify an agent’s autonomy level, permissions, risks, and necessary human checkpoints.
5. Assign work using a clear outcome, relevant context, constraints, examples, deliverable, and review criteria.
6. Work effectively with source files and tell the agent what to trust, question, or ask about.
7. Give diagnostic feedback and verify factual and procedural work.
8. Set up and test a portable context or memory workspace.
9. Decide what should be saved, retrieved, corrected, superseded, archived, or kept private.
10. Complete a small end-to-end supervised workflow and identify the next workflow worth developing.

## Completion criteria

A learner has completed the course successfully when they can perform the following without copying a full instructor prompt:

- Explain the model–harness/app–assistant–agent distinction and the chat/tool loop.
- Classify information as task context, instructions, durable memory, source knowledge, or archive.
- Give an AI assistant a complete assignment using the CLEAR method.
- Identify the tools and permissions required for that assignment.
- Name at least one point at which the agent must stop and ask for approval.
- Verify the output against an explicit standard or source.
- Save one confirmed learning with a source, scope, and status.
- Retrieve that learning in a fresh session.

## Scope and boundaries

### Included

- The modern AI landscape in practical language.
- A durable mental model for assistants and agents.
- Essential current terminology.
- Initial tool and workspace setup.
- Prompting as assignment design, not clever wording.
- Context and memory foundations.
- Tools, skills, MCP, permissions, and safety.
- A file-first approach to portable knowledge.
- A short supervised business workflow.

### Reserved for later courses

- Brand positioning and brand strategy.
- Audience research and offer development.
- Content pillars, channel strategy, and editorial planning.
- Voice modeling and content production systems.
- Advanced entrepreneurship coaching methods.
- Personal second-brain design and coaching memory in depth.
- Shared team-memory infrastructure.
- Agent engineering, APIs, EVE, multi-agent systems, or database development.
- Fully autonomous publishing or other consequential unattended actions.

## Instructional design approach

The course uses backward design: the practical behavior expected at the end determines the lessons, examples, activities, and capstone. Concepts are included only when they help the learner make a better decision or perform the final workflow.

### Design principles

1. **One clear outcome per lesson.** Every lesson has a single main behavior or decision the learner should be able to perform.
2. **Progress from mental model to action.** Learners first understand the system, then its information and capabilities, then how to work with it, and finally how to complete a workflow.
3. **Keep cognitive load low.** New terminology is grouped by function and anchored to one consistent analogy.
4. **Use realistic business examples.** Abstract concepts are demonstrated through briefs, research, planning, drafting, and review.
5. **Correct misconceptions explicitly.** Each lesson names a common false belief and replaces it with a usable rule.
6. **Require a small learner output.** Every module ends with a decision, artifact, or check that contributes to the final workflow.
7. **Teach supervision, not blind trust.** The learner remains accountable for scope, permissions, evidence, and final approval.
8. **Prefer portable foundations.** Course knowledge and memory templates use plain files and explicit structure wherever possible.
9. **Use retrieval practice.** Short “Can you explain or decide this?” checks help learners recall ideas instead of only recognizing them.
10. **Align the final assessment with the promise.** The capstone requires setup, delegation, tool awareness, review, revision, and selective memory capture.

### Standard lesson pattern

Each recorded lesson should follow this five-part pattern:

1. **Orient:** State the practical question the lesson answers.
2. **Explain:** Introduce one mental model or method in plain language.
3. **Correct:** Address one or two likely misconceptions.
4. **Demonstrate or decide:** Show a small example, or ask the learner to make a decision.
5. **Close:** Give one memorable rule and connect it to the next lesson.

This pattern is a teaching scaffold, not a word-for-word script.

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

| Term              | Course definition                                                                                                           |
| ----------------- | --------------------------------------------------------------------------------------------------------------------------- |
| AI model          | The underlying system that processes input and generates output.                                                            |
| LLM               | A language-focused model trained to work with text and related representations.                                             |
| Multimodal model  | A model that can work with more than one type of input or output, such as text, images, audio, or video.                    |
| Harness / AI application | The software around the model: UI, context assembly, tool execution, history, integrations, and permissions. Same idea as “app,” “runtime,” or “scaffold.” |
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
| RAG               | Retrieval-augmented generation: retrieving relevant source material and adding it to the model’s context before generation. |
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

> Instructor note: learners may encounter the typo “MPC” online. The course term is **MCP: Model Context Protocol**.

# Curriculum at a glance

| Module | Module title                      | Lessons |    Runtime | Module output                                                       |
| -----: | --------------------------------- | ------: | ---------: | ------------------------------------------------------------------- |
|      1 | Orientation and setup             |       2 |      8 min | A safe practice task and a verified working environment.            |
|      2 | The AI mental model               |       2 |     10 min | A correct model–assistant–agent explanation and an autonomy choice. |
|      3 | Context and memory language       |       2 |     12 min | A context checklist and information-classification exercise.        |
|      4 | Tools, skills, MCP, and safety    |       2 |      8 min | A capability map and approval rule.                                 |
|      5 | Working effectively with an agent |       3 |     12 min | A complete assignment, source pack, and reviewed output.            |
|      6 | Durable context and ontology      |       2 |      6 min | A starter context workspace and one confirmed memory.               |
|      7 | First supervised workflow         |       2 |      4 min | One reviewed artifact and a next-workflow brief.                    |
|        | **Total**                         |  **15** | **60 min** | **A complete, supervised AI working loop.**                         |

# Full curriculum and instructor recording guide

## Module 1 — Orientation and setup

**Module runtime:** 8 minutes  
**Module purpose:** Give learners a clear destination, a safe practice boundary, and a verified environment before introducing more theory.  
**Module outcome:** The learner has selected a suitable practice task and confirmed that the assistant can work with the course context workspace.

### Lesson 1 — What you will build, and how to learn safely

**Runtime:** 3 minutes  
**Lesson objective:** Select a small, non-sensitive practice task and understand the final course workflow.  
**Learner output:** A one-sentence practice task and a clear privacy boundary.

#### Why this lesson exists

Many introductions begin with definitions and make learners wait to discover what the knowledge is for. This lesson starts with the destination: by the end, the learner will give an assistant a business brief, receive a draft, review it, revise it, and save one approved learning for later.

#### Teaching points

- Describe the final result before explaining the technology.
- Position the assistant as a collaborator that must be briefed and supervised.
- Explain that course exercises should use real enough material to be meaningful, but not confidential customer data, passwords, private financial records, regulated information, or anything the learner is not authorized to share.
- Introduce the rule: start with reversible, low-consequence work.
- Ask learners to choose one small task such as summarizing a non-sensitive brief, planning a short article, drafting a customer FAQ, or organizing public research.
- Explain that they will keep the same task through the course so every concept connects to one practical outcome.

#### Suggested teaching flow

1. Open with the course promise and show the completed workflow in one sentence.
2. Explain the learner’s role as accountable owner.
3. Give two safe practice-task examples and two examples that are inappropriate for a beginner exercise.
4. Ask the learner to pause and write their task as: “By the end, I want the assistant to help me \_\_\_.”
5. Close with the rule: **use real work, but begin with low stakes and reversible actions.**

#### Misconceptions to correct

- “If the AI service accepts the upload, the information must be safe to share.”
- “A polished answer means the result is ready to use.”
- “An agent is accountable for the business outcome.”

#### Example

Use a simple content example: “Turn a public one-page business description into three possible article angles.” Do not teach content strategy yet; use the example only to show the working loop.

#### Slide opportunities

- Course journey: understand → set up → assign → supervise → remember.
- Safe starting zone: low consequence, reversible, non-sensitive.
- Final workflow diagram with human approval before the final output and before memory capture.

#### Transition

“Now that we know what we are building, let’s make sure the assistant and its context workspace actually work.”

### Lesson 2 — Set up and verify your AI workspace

**Runtime:** 5 minutes  
**Lesson objective:** Confirm a minimal tool stack and complete a read/write/retrieve setup test.  
**Learner output:** A working assistant connected to an owned context workspace, or a verified plain-Markdown fallback.

#### Production decision before recording

Record one primary assistant interface consistently. Keep the explanation provider-neutral and provide a separate translation sheet for the other supported interface. Do not record every step twice inside the core lesson.

The required architecture is:

1. One supported AI assistant.
2. One dedicated course or project workspace.
3. One file-first context folder that the learner can inspect and edit.
4. An optional retrieval or memory layer connected through a supported integration such as MCP.
5. A plain-Markdown fallback if the integration is unavailable.

The course must not depend on a particular paid memory product. A product such as Basic Memory may be demonstrated, but it should be presented as one implementation of the architecture, not as the definition of memory.

#### Teaching points

- Show the exact minimum stack; postpone optional tools.
- Create or open a dedicated project rather than mixing course work into a general chat.
- Show where the context files live and emphasize that the learner can read, edit, copy, and back them up.
- If using MCP or another connector, show where connected capabilities are listed.
- Run a harmless acceptance test:
  1. Ask the assistant to list the intended workspace or folder.
  2. Ask it to read a small starter note.
  3. Create a clearly labeled test note.
  4. Inspect the saved result directly.
  5. Start a fresh conversation and retrieve it explicitly.
  6. Delete the test note or mark it as a disposable setup test.
- Explain that a successful connection is not proof that the assistant will always choose or use it correctly.

#### Suggested teaching flow

1. Show the stack as layers: assistant, context files, optional retrieval connection.
2. Point out where files are stored and how the learner retains access.
3. Perform the acceptance test without adding business information.
4. Demonstrate the plain-file fallback in one sentence or screen.
5. Close with the rule: **if you cannot inspect, correct, export, and back up the context, do not treat it as your canonical memory.**

#### Misconceptions to correct

- “Connected” means “the agent will automatically use it.”
- A memory product owns the only copy of the learner’s knowledge.
- More integrations create a better beginner setup.
- Chat history alone is a durable context system.

#### Demonstration checklist

- Show the assistant’s current workspace.
- Show the starter context folder.
- Read one file.
- Write one disposable note.
- Inspect it outside the conversation.
- Retrieve it in a new conversation.
- Show how to disconnect or remove access.

#### Slide opportunities

- Minimal stack diagram.
- Six-step setup acceptance test.
- “Canonical files vs. optional index” architecture.

#### Transition

“The setup works. Next we need a reliable way to understand what is actually doing the work inside it.”

## Module 2 — The AI mental model

**Module runtime:** 10 minutes  
**Module purpose:** Replace vague or anthropomorphic ideas with a practical model that remains useful as products change—especially model vs harness/app.  
**Module outcome:** The learner can distinguish the model from the product/harness, explain one chat turn (including tools), and choose an appropriate level of autonomy.

### Lesson 3 — Model, harness (app), and assistant

**Runtime:** 5 minutes  
**Lesson objective:** Explain why a model, the product/harness around it, and the assistant experience are related but not interchangeable—and how one modern chat turn actually runs.  
**Learner output:** A one-sentence model vs harness distinction, plus a sketched chat turn.

> Canonical detail lives in `course-01-ai-agents-fundamentals/course-01-curriculum.html` (12-lesson curriculum). Prefer that file’s **Slides (draft)** section when generating Google Slides (per-slide visual briefs + side-panel terms; brand later).

#### Teaching points

- A model is the reasoning and generation engine; it does not open files, click buttons, or enforce permissions by itself.
- The application—also called the harness or runtime—is ordinary software around the model: UI, context assembly, tool execution, history, integrations, and permissions.
- An assistant is the working experience when model + harness + instructions + context + capabilities combine.
- How a chat turn works now: you send a message → harness assembles context → model replies with text and/or tool requests → harness runs allowed tools and feeds results back → model may continue → you see a response.
- Same model, different harness → different behavior. Switching apps changes more than the model name.
- “Multimodal” means more than one form of information; it does not mean every product supports every modality everywhere.

#### Suggested teaching flow

1. Show model vs harness (brain + workplace/hands).
2. Walk one chat turn sequence, including an optional tool call.
3. Compare same model in two products.
4. Ask: “What does the harness do that the model cannot do alone?”
5. Close with the rule: **judge the model plus its harness—not the model name alone.**

#### Misconceptions to correct

- “ChatGPT,” “Claude,” or another product is simply one model.
- The model itself executes tools, searches the web, or edits files.
- A newer or larger model automatically has access to more of the learner’s data or better permissions.
- Model intelligence and product permissions are the same capability.
- A conversational tone means the system understands or cares in the human sense.

#### Example

Use a research assistant. The model can summarize text; the harness determines whether it can search the web, open a private workspace, cite sources, or save a result—and it is the harness that actually runs those tools when the model requests them.

#### Slide opportunities

- Model vs harness diagram.
- One modern chat-turn sequence (with optional tool loop).
- Same model, different app comparison.
- Retrieval check: what the harness does that the model cannot.

#### Transition

“One chat turn can already use tools. An agent extends that loop across more steps toward a goal—but autonomy is a spectrum, not magic.”

### Lesson 4 — Workflow, automation, and agent

**Runtime:** 6 minutes  
**Lesson objective:** Choose the simplest appropriate working pattern and a suitable autonomy level.  
**Learner output:** An autonomy level selected for the learner’s practice task.

#### Teaching points

- A single response is not automatically a workflow or an agent.
- A workflow is a sequence of steps, whether a human, software, or AI performs them.
- An automation follows a predefined trigger and path; it is valuable when the steps and exceptions are well understood.
- An agent receives a goal, decides or adapts some steps, uses available tools, observes results, and continues within boundaries.
- “Agentic” is a degree. Systems differ in how much they plan, choose, act, and recover.
- More autonomy is not inherently more advanced or more useful. It increases the need for trustworthy inputs, permissions, monitoring, and recovery.

#### The autonomy ladder

1. **Suggest:** The assistant gives options; the human does the work.
2. **Draft:** The assistant creates a proposed artifact; the human edits and uses it.
3. **Prepare:** The assistant completes multiple steps and prepares an action; the human approves execution.
4. **Act with approval:** The assistant can use tools but stops at defined checkpoints.
5. **Act independently:** The assistant acts and monitors within a narrow, tested boundary.

For this course, most examples should remain between levels 2 and 4.

#### Suggested teaching flow

1. Contrast a one-off answer, a workflow, an automation, and an agent.
2. Explain the agent loop: understand goal → plan → use tools → observe → adjust → stop or ask.
3. Present the autonomy ladder.
4. Apply it to one example: preparing a newsletter is appropriate; publishing it without review usually is not a beginner workflow.
5. Ask learners to select the lowest autonomy level that can still save meaningful time.
6. Close with the rule: **earn autonomy through narrow scope, evidence, and successful review—not enthusiasm.**

#### Misconceptions to correct

- Any chatbot with a friendly name is an agent.
- An agent must operate without human involvement.
- More steps or more tools make a system more agentic in a useful way.
- Automation and agent are synonyms.
- The agent always knows when it should stop.

#### Example

Use a content workflow:

- Suggest: propose five article ideas.
- Draft: write one article outline.
- Prepare: research, outline, and draft a post for approval.
- Act with approval: save an approved draft to the content system.
- Independent: schedule or publish under narrow rules after extensive testing.

#### Slide opportunities

- Workflow vs. automation vs. agent comparison.
- Agent loop.
- Five-level autonomy ladder with a “course zone” highlight.

#### Transition

“Agents make choices using whatever information is available at that moment. To supervise them well, we need to understand what enters that temporary workbench—and what does not.”

## Module 3 — Context and memory language

**Module runtime:** 12 minutes  
**Module purpose:** Give learners the vocabulary and judgment needed to provide, retrieve, and preserve information reliably.  
**Module outcome:** The learner can assemble useful task context and classify information by where it should live.

### Lesson 5 — Prompts, instructions, tokens, and context windows

**Runtime:** 6 minutes  
**Lesson objective:** Assemble focused context for a task without assuming that more information always produces a better result.  
**Learner output:** A context checklist for the practice task.

#### Teaching points

- A prompt is the immediate input; an assignment can include a goal, sources, constraints, format, process, and success criteria.
- Instructions may exist at multiple levels: product rules, course or organization rules, project rules, a reusable skill, and the current request.
- The model does not see everything the learner sees. It can only use information the application actually includes in the current model call.
- Tokens are processing units, not a useful measure of importance or truth.
- A context window is finite working space. It may contain instructions, messages, retrieved notes, tool results, and source material.
- A large window reduces some limitations, but does not guarantee attention, recall, correct prioritization, or conflict resolution.
- Relevance, authority, structure, and clarity matter more than filling the window.

#### The context checklist

Before assigning a substantial task, identify:

1. The outcome.
2. The audience or user of the result.
3. The authoritative sources.
4. The constraints and non-goals.
5. A strong example, when useful.
6. The required deliverable and format.
7. The quality standard.
8. What the assistant must ask rather than assume.

#### Suggested teaching flow

1. Put a small “workbench” on screen and add information to it.
2. Explain prompts and layered instructions.
3. Show how messages, files, retrieved notes, and tool results compete for finite attention.
4. Compare a disorganized context dump with a short structured brief.
5. Build the context checklist for the practice task.
6. Close with the rule: **give the smallest complete set of relevant, authoritative information.**

#### Misconceptions to correct

- More context always produces a better answer.
- A large context window is perfect memory.
- If information appeared earlier in a long chat, the model will necessarily use it correctly.
- The model can see every connected file or service at all times.
- Prompting is mainly about finding a magical sentence.

#### Example

Compare these two inputs:

- “Write a post about our company. Here are 40 unlabelled files.”
- “Draft a 300-word founder post for first-time agency owners. Use the approved positioning note as the source of truth, match the two attached voice examples, avoid product claims not found in the source, and list any missing facts before drafting.”

#### Slide opportunities

- Context workbench diagram.
- Instruction hierarchy.
- “More” versus “more relevant and authoritative.”
- Eight-item context checklist.

#### Transition

“Context is the temporary workbench. Memory is how selected information becomes available again—but chat history, RAG, and memory are not interchangeable.”

### Lesson 6 — Memory, RAG, embeddings, and knowledge graphs

**Runtime:** 6 minutes  
**Lesson objective:** Classify information correctly and explain how a system may retrieve it later.  
**Learner output:** A short classification of information as context, instruction, durable memory, source knowledge, or archive.

#### Core distinctions

- **Chat history** is a record of prior messages. A product may summarize, truncate, search, or ignore parts of it.
- **Context** is what is actually made available for the current task.
- **Instructions** define how the assistant should behave or perform recurring work.
- **Source knowledge** is the material the assistant may consult, such as approved brand notes, research, policies, or product documentation.
- **Memory** preserves selected facts, decisions, preferences, relationships, or state for future use.
- **Retrieval** finds potentially useful material and places it into the current context.
- **RAG** combines retrieval with generation. It improves grounding when the right source is retrieved, but does not prove the source is correct or the answer follows it faithfully.
- **Embeddings** help compare semantic similarity. They are useful for finding related passages, not for deciding truth or authority.
- **Knowledge graphs** make entities and relationships explicit, such as “Offer A serves Audience B” or “Decision C supersedes Decision D.”

#### The memory pipeline

Explain memory as a lifecycle rather than a magical feature:

1. Capture a candidate fact, decision, preference, or event.
2. Decide whether it is worth preserving.
3. Label its source, scope, status, and sensitivity.
4. Store it in a canonical system.
5. Index or connect it for retrieval.
6. Retrieve relevant material for a future task.
7. Correct, supersede, archive, or delete it when reality changes.

#### Suggested teaching flow

1. Contrast chat history with durable memory.
2. Walk through the memory pipeline.
3. Explain RAG with a librarian analogy: retrieval brings books to the desk; the model still has to read and use them correctly.
4. Explain embeddings as meaning-based coordinates and graphs as explicit relationship maps.
5. Classify five examples from a fictional founder workspace.
6. Close with the rule: **retrieval improves access, not truth; durable memory needs provenance and correction.**

#### Misconceptions to correct

- A bigger model remembers the learner personally.
- Chat history is a reliable permanent memory.
- RAG and memory are the same thing.
- RAG prevents hallucinations.
- Vector similarity means factual relevance or authority.
- A knowledge graph is automatically more accurate than files.
- The agent permanently learns every correction made in conversation.

#### Classification example

| Information                            | Appropriate home           | Reason                                        |
| -------------------------------------- | -------------------------- | --------------------------------------------- |
| “Draft a launch email today.”          | Current task context       | Temporary assignment.                         |
| “Always ask before publishing.”        | Instruction or guardrail   | Reusable behavior rule.                       |
| Approved positioning statement         | Canonical source knowledge | Authoritative business material.              |
| “We chose monthly billing on 12 July.” | Durable decision memory    | A confirmed decision with date and rationale. |
| Old brainstorming dump                 | Archive                    | Potentially useful history, not active truth. |

#### Slide opportunities

- Context, history, knowledge, and memory comparison.
- Seven-stage memory lifecycle.
- RAG librarian diagram.
- Embeddings versus knowledge graph.

#### Transition

“Information helps the agent decide. Tools let it do. Skills tell it how. MCP helps connect the pieces.”

## Module 4 — Tools, skills, MCP, and safety

**Module runtime:** 8 minutes  
**Module purpose:** Explain how agents gain capabilities and how the learner keeps consequential actions under control.  
**Module outcome:** The learner can map the capabilities required for a workflow and define a clear stop-and-ask rule.

### Lesson 7 — Tools, skills, connectors, APIs, and MCP

**Runtime:** 5 minutes  
**Lesson objective:** Distinguish reusable guidance from executable capability and from the connection mechanism.  
**Learner output:** A capability map for the practice workflow.

#### The simple distinction

- **Tools do.** A tool searches, reads, calculates, writes, sends, updates, or performs another action.
- **Skills guide.** A skill provides reusable instructions, procedures, examples, standards, and decision rules for a type of work.
- **Connectors link.** A connector links the assistant to an external source or service.
- **APIs define communication.** An API is a software interface through which systems exchange requests and results.
- **MCP standardizes discovery and use.** MCP gives compatible AI clients a common pattern for exposing resources, prompts, and tools.

These categories can overlap in a product interface, but the distinction helps the learner reason about behavior and risk.

#### Teaching points

- A skill without a necessary tool can explain what to do but cannot perform the external action.
- A tool without a good skill may be used inconsistently or in the wrong order.
- A connector or MCP server can expose several capabilities, each with different permissions.
- Installation or connection does not guarantee selection, correct use, or reliable output.
- More tools increase the action surface, ambiguity, and potential impact.
- A good capability map starts with the workflow and adds only what each step requires.

#### Suggested teaching flow

1. Present “tools do, skills guide, MCP connects.”
2. Add connectors and APIs to complete the vocabulary.
3. Use one content example: a voice skill guides the writing; a file tool reads examples; a research tool finds sources; a publishing tool changes external state.
4. Build a capability map with columns for step, information, skill, tool, and approval.
5. Show why the publishing tool is not required for a drafting course.
6. Close with the rule: **start from the workflow and grant the minimum capability needed for each step.**

#### Misconceptions to correct

- A skill and a tool are the same thing.
- MCP is the agent’s memory.
- MCP replaces APIs or guarantees interoperability in every detail.
- Once a tool is connected, the agent will choose it correctly.
- More tools always create a more capable system.

#### Capability-map example

| Workflow step | Needed information  | Skill or procedure          | Tool                   | Approval                    |
| ------------- | ------------------- | --------------------------- | ---------------------- | --------------------------- |
| Read brief    | Approved brief      | Source-handling rules       | File read              | No                          |
| Find evidence | Research question   | Research and citation skill | Web search             | Review sources              |
| Draft         | Brief and examples  | Voice and drafting skill    | None beyond files      | No                          |
| Save draft    | Approved location   | File-naming rule            | File write             | Confirm location            |
| Publish       | Final approved copy | Publishing checklist        | Publishing integration | Always in beginner workflow |

#### Slide opportunities

- Tools/skills/MCP three-part visual.
- Capability-map table.
- “Connected ≠ selected ≠ correct” sequence.

#### Transition

“Capabilities are useful only when their boundaries are clear. The next lesson separates instructions from real enforcement.”

### Lesson 8 — Permissions, guardrails, sandboxing, and approval

**Runtime:** 3 minutes  
**Lesson objective:** Define least-privilege access and a human approval point for consequential work.  
**Learner output:** One written stop-and-ask rule.

#### Teaching points

- Read, create, edit, delete, send, publish, purchase, and administer are different permission levels.
- Grant only the access needed for the current workflow.
- Prefer reversible actions: prepare a draft before sending; create a new file before overwriting; preview before publishing.
- Instructions are guidance. Technical permissions, scoped credentials, sandboxes, and approval interfaces provide stronger enforcement.
- A sandbox limits where actions can have an effect; it does not make every output correct or harmless.
- Prompt injection is untrusted content attempting to redirect the agent. External pages, documents, emails, and tool results should be treated as data, not as authority over the learner’s goal.
- The human should approve actions with legal, financial, reputational, privacy, or irreversible consequences.

#### Suggested teaching flow

1. Show a permission ladder from read to irreversible external action.
2. Contrast “please do not publish” with an environment that has no publishing permission.
3. Explain one prompt-injection example without dramatizing it.
4. Ask the learner to write: “Stop and ask me before \_\_\_.”
5. Close with the rule: **instructions guide behavior; permissions limit consequences.**

#### Misconceptions to correct

- A system prompt or skill is a security boundary.
- A sandbox proves the result is safe.
- Read-only access has no privacy implications.
- Human review is unnecessary for a familiar recurring task.

#### Slide opportunities

- Permission ladder.
- Instructions versus enforcement.
- Stop-and-ask categories.

#### Transition

“We now understand the system and its boundaries. The next step is learning how to give it work in a form it can execute and we can evaluate.”

## Module 5 — Working effectively with an agent

**Module runtime:** 12 minutes  
**Module purpose:** Teach a repeatable collaboration method that works across providers and tasks.  
**Module outcome:** The learner can give a complete assignment, supply trustworthy source material, and improve an output through evidence-based review.

### Lesson 9 — Give a clear assignment with CLEAR

**Runtime:** 6 minutes  
**Lesson objective:** Turn a vague request into an executable and reviewable assignment.  
**Learner output:** One complete CLEAR assignment for the practice task.

#### The CLEAR method

1. **Clarify the outcome.** What result is needed, for whom, and why?
2. **Load the context.** Which facts, sources, history, and examples are relevant?
3. **Explain standards and constraints.** What must be true, avoided, preserved, or approved?
4. **Ask for a deliverable.** What exactly should the assistant return, in what format, and through what process?
5. **Review and refine.** How will the learner inspect, verify, correct, and approve the result?

CLEAR is a thinking checklist, not a rigid prompt formula. A two-sentence task can still be clear; a long prompt can still be confused.

#### Teaching points

- Start with the desired outcome, not a vague role-playing instruction.
- Provide the minimum sufficient context, with sources labeled by authority.
- Separate hard constraints from preferences.
- Specify the artifact and quality criteria.
- Ask the assistant to state missing information or assumptions before acting when those gaps matter.
- For complex work, ask for a short plan or proposed approach before a costly action.
- Define the stopping condition: what counts as finished?
- Use examples to show the target, but explain what matters about the example.

#### Suggested teaching flow

1. Show a vague request: “Help with my content.”
2. Build the assignment through the five CLEAR steps.
3. Point out that the improved version is easier to execute and easier to evaluate.
4. Demonstrate an “ask before assuming” instruction.
5. Ask learners to complete their own CLEAR worksheet.
6. Close with the rule: **a good assignment makes the outcome and the review standard visible.**

#### Worked example

**Clarify:** Propose three article angles that help first-time agency owners understand why inconsistent positioning makes content harder to produce.

**Load:** Use the approved positioning note and audience note. Treat them as authoritative. Use the two published posts only as tone examples.

**Explain:** Avoid promising guaranteed growth. Do not invent customer evidence. Each angle must address one real audience problem.

**Ask:** Return a table with angle, audience tension, core claim, supporting source, and suggested call to action. Before drafting, list any missing facts that would materially affect the result.

**Review:** Check each claim against the source notes, identify unsupported statements, and recommend the strongest angle with a reason.

#### Misconceptions to correct

- Prompt quality is mainly about secret phrases.
- Assigning a persona is enough to define a job.
- Very long prompts are necessarily better.
- The learner should answer every possible question in advance.
- The first output is the finished product.

#### Slide opportunities

- CLEAR acronym and one-line definition for each step.
- Before/after assignment.
- Hard constraints versus preferences.
- Plan → execute → review loop.

#### Transition

“CLEAR defines the assignment. The quality of the result still depends on what sources and examples the agent receives—and how clearly their authority is labeled.”

### Lesson 10 — Work with sources, files, and examples

**Runtime:** 3 minutes  
**Lesson objective:** Give the assistant a small, labeled source pack and prevent silent assumptions.  
**Learner output:** A source pack with authority labels and an ask-before-assuming rule.

#### Teaching points

- Name the source of truth explicitly. Do not make the agent infer which of several files is current.
- Distinguish instructions from evidence. A web page or document can contain useful information without gaining authority to change the task.
- Mark files as approved, reference-only, draft, outdated, or archived.
- Provide one or two strong examples and explain the characteristics to imitate.
- Tell the assistant how to handle conflicts between sources.
- Ask for citations or source pointers when factual traceability matters.
- Ask the assistant to surface missing, conflicting, or low-confidence information.

#### Suggested teaching flow

1. Show a messy folder with ambiguous files.
2. Reduce it to a small source pack with clear labels.
3. Demonstrate one example plus an explanation of what to imitate.
4. Add the rule: “If an important fact is missing or sources conflict, stop and ask.”
5. Close with the rule: **label authority; do not make the agent guess which source wins.**

#### Misconceptions to correct

- The newest-looking file is necessarily the approved file.
- An example is automatically interpreted in the intended way.
- The agent will notice every contradiction in a source pack.
- Citing a file proves the conclusion is supported by it.

#### Slide opportunities

- Source labels: approved, reference, draft, outdated, archive.
- Instruction versus evidence split.
- Conflict-handling rule.

#### Transition

“A well-briefed agent can still be wrong. The professional habit is not to demand perfection—it is to make verification and correction part of the workflow.”

### Lesson 11 — Correct, verify, and improve

**Runtime:** 3 minutes  
**Lesson objective:** Review an output with evidence and turn a correction into a reusable quality improvement.  
**Learner output:** A revised artifact and one reusable quality check.

#### Teaching points

- Separate factual correctness, instruction-following, quality, and preference. They require different feedback.
- Give diagnostic feedback: identify the issue, show evidence, restate the standard, and request a specific correction.
- Verify claims against primary or authoritative sources when accuracy matters.
- Ask the assistant to show assumptions, unresolved questions, or a checklist of compliance.
- Use a lightweight evaluation checklist for recurring work.
- Save durable corrections in the relevant instruction, skill, source note, or memory—not only in chat.
- Do not store every dislike as a permanent preference; confirm that the lesson should apply again.

#### Suggested teaching flow

1. Show unhelpful feedback: “This is bad. Try again.”
2. Replace it with a diagnostic correction tied to a source or standard.
3. Verify one claim and one instruction requirement.
4. Decide whether the correction is task-specific or reusable.
5. Close with the rule: **correct the system where the error originated, then test the correction.**

#### Misconceptions to correct

- A confident answer is a verified answer.
- Asking the model “Are you sure?” is a sufficient fact check.
- Every correction should become long-term memory.
- A longer self-critique automatically improves the result.

#### Feedback formula

> Issue → evidence → applicable standard → requested correction → verification.

Example: “The draft says the service includes weekly reporting, but the approved offer note says monthly. Replace the claim, scan the rest of the draft for unsupported service details, and list the source line used for each corrected claim.”

#### Slide opportunities

- Four review dimensions: facts, instructions, quality, preference.
- Diagnostic feedback formula.
- Task correction versus durable system improvement.

#### Transition

“Some corrections disappear when the chat ends. The next module shows how to preserve only the knowledge that deserves to survive.”

## Module 6 — Durable context and ontology

**Module runtime:** 6 minutes  
**Module purpose:** Turn useful, confirmed information into an owned and maintainable context system.  
**Module outcome:** The learner understands the file-first architecture and can save one well-formed memory.

### Lesson 12 — Build a portable context architecture

**Runtime:** 4 minutes  
**Lesson objective:** Understand a file-first context system whose canonical knowledge remains independent of the retrieval product.  
**Learner output:** A starter context workspace with a small, understandable structure.

#### Architecture to teach

Use four layers:

1. **Canonical files:** Human-readable notes containing approved knowledge, decisions, instructions, and evidence.
2. **Active context:** The small set of notes relevant to current work.
3. **Retrieval index:** A searchable representation such as full-text or vector search that helps find relevant files.
4. **Derived relationships:** Optional links, summaries, or graph edges created from canonical knowledge.

The canonical files are the source of truth. Indexes and graphs can be rebuilt. Derived summaries and inferred relationships should remain labeled and correctable.

#### Starter ontology

Keep the first version small. Use only categories that support real work:

- **Profile:** working preferences, responsibilities, and relevant background.
- **Business:** mission, model, stage, constraints, and operating context.
- **Brand:** positioning, promise, values, personality, and approved language.
- **Audience:** segments, problems, jobs, objections, and evidence.
- **Offer:** product or service, price, scope, proof, and exclusions.
- **Content system:** pillars, channels, formats, voice, examples, and editorial rules.
- **Goal:** outcome, metric, target date, status, and owner.
- **Project:** scope, milestones, current state, risks, and decisions.
- **Task:** action, owner, status, deadline, and dependency.
- **Decision:** choice, rationale, alternatives, date, and superseded decision.
- **Experiment:** hypothesis, action, result, evidence, and learning.
- **Evidence:** interview, metric, source, artifact, or observation.
- **Session:** agenda, insights, commitments, and follow-up.

The introduction course should show the structure without requiring learners to fill every category. The brand, content, coaching, and team ontologies are expanded in later courses.

#### Metadata for durable knowledge

When knowledge matters, capture:

- **Scope:** private, project, team, or organization.
- **Source:** who stated it or which artifact supports it.
- **Status:** proposed, confirmed, disputed, superseded, or archived.
- **Time:** capture date, effective date, and optional review date.
- **Confidence:** explicit statement, observed evidence, or inference.
- **Owner:** who can confirm or change it.
- **Sensitivity:** ordinary, confidential, personal, or restricted.

#### Suggested teaching flow

1. Show canonical files at the center and optional indexes around them.
2. Explain why files are a durable ownership boundary.
3. Introduce the starter ontology as a map, not a form to complete immediately.
4. Open one sample decision or brand note and point out source, status, and scope.
5. Explain that Basic Memory or another memory service can sit above these files without becoming the only copy.
6. Close with the rule: **keep truth inspectable; treat indexes, summaries, and graphs as rebuildable views.**

#### Misconceptions to correct

- A complex folder tree is the same as a useful ontology.
- Every conversation should be saved.
- A generated summary is automatically canonical truth.
- A graph should replace the source documents.
- Choosing a memory product solves governance and correction.

#### Slide opportunities

- Four-layer portable-memory architecture.
- Starter ontology map.
- Durable-memory metadata card.
- Canonical versus derived information.

#### Transition

“The architecture is only useful if knowledge has a lifecycle. Let’s save one confirmed item and show how it changes later without silently rewriting history.”

### Lesson 13 — Save, retrieve, correct, and supersede

**Runtime:** 2 minutes  
**Lesson objective:** Apply a simple memory lifecycle to one confirmed item.  
**Learner output:** One saved memory with source, scope, and status.

#### Teaching points

- Search before writing to avoid duplicates and contradictions.
- Capture a memory candidate, then confirm whether it should persist.
- Separate a user statement, an observed fact, and an agent inference.
- Add source, scope, status, and date.
- Retrieve explicitly in a fresh session and inspect what was actually returned.
- Correct a factual error at the canonical source.
- When a decision changes, mark the old one superseded and link to the replacement rather than erasing the history.
- Archive or delete information that should no longer influence current work.

#### Suggested teaching flow

1. Save one approved preference or decision from the practice task.
2. Show its metadata.
3. Retrieve it in a fresh session.
4. Describe correction and supersession with one changed-decision example.
5. Close with the rule: **memory is curated state, not an automatic transcript.**

#### Misconceptions to correct

- Everything useful should be stored forever.
- New information should silently overwrite old decisions.
- Retrieval proves that the latest or correct version was found.
- An inferred preference is equivalent to an explicit user preference.

#### Slide opportunities

- Search → confirm → write → retrieve → correct/supersede → archive.
- Confirmed fact versus inference.
- Supersession example.

#### Transition

“We now have every part of the loop. The last module compresses them into one supervised business workflow.”

## Module 7 — First supervised workflow

**Module runtime:** 4 minutes  
**Module purpose:** Let learners experience the complete loop and identify the most valuable next application.  
**Module outcome:** The learner completes one reviewed artifact and leaves with a candidate workflow for the follow-on course.

### Lesson 14 — Mini workflow: from brief to reviewed output

**Runtime:** 2 minutes  
**Lesson objective:** Execute the complete supervised loop once.  
**Learner output:** One reviewed artifact and one approved learning saved to memory.

#### Workflow

1. Open the practice task and identify the intended outcome.
2. Load the approved brief and source pack.
3. Give the assistant the CLEAR assignment.
4. Confirm the tools and permissions it may use.
5. Ask for a short plan or missing-information check.
6. Generate the small artifact.
7. Verify it against the brief and one quality checklist.
8. Request one diagnostic revision.
9. Approve or reject the result.
10. Save only one confirmed decision, preference, or learning with appropriate metadata.

#### Teaching points

- Keep the artifact deliberately small so the full loop is visible.
- Use a brand or content example only as a neutral practice case.
- Narrate the human decisions: source authority, permission, approval, and memory selection.
- Do not make the demonstration about a perfect first draft.

#### Suggested demonstration artifact

A table containing three article angles based on a one-page audience and positioning brief. Review each angle for source support, audience relevance, and unsupported claims. Revise one angle and save the approved content-pillar decision—not the entire conversation.

#### Closing rule

**The value is not the first answer; it is the controlled loop from context to action to verified learning.**

#### Misconceptions to correct

- A successful demonstration means the workflow is ready for unattended use.
- The entire conversation should be saved because every intermediate thought may be useful later.
- The best workflow is the one that produces the largest artifact.

#### Slide opportunities

- Ten-step supervised workflow.
- Human decision markers.
- Final artifact plus one memory card.

#### Transition

“You have completed one loop. The next question is where this way of working will create the most repeated value.”

### Lesson 15 — Choose your next agent workflow

**Runtime:** 2 minutes  
**Lesson objective:** Select a repeated task and classify the appropriate AI working pattern.  
**Learner output:** A one-page candidate workflow brief for the next course.

#### Teaching points

- Look for work that is repeated, time-consuming, information-heavy, and reviewable.
- Avoid starting with rare, highly consequential, poorly understood, or irreversible work.
- Choose the simplest pattern:
  - Use regular chat for one-off thinking.
  - Use a skill for a recurring method or quality standard.
  - Use a workflow for a repeatable sequence.
  - Use an agent when the system must adapt steps or use tools toward a goal.
  - Add automation only when triggers, boundaries, and exceptions are understood.
- Define the input, output, sources, tools, approval points, quality criteria, and memory created.
- Introduce the follow-on learning paths without teaching them here.

#### Candidate workflow brief

- Workflow name.
- Repeated business problem.
- Desired outcome.
- Trigger or starting point.
- Required sources and context.
- Reusable skill or method.
- Required tools.
- Human approval points.
- Quality checklist.
- Knowledge worth preserving.
- Risks and failure recovery.

#### Suggested teaching flow

1. Show the decision tree: chat, skill, workflow, agent, or automation.
2. Apply it to two tasks: a one-off brainstorming session and a recurring content-research workflow.
3. Ask learners to select one candidate and complete the brief.
4. Point to the next course that matches their goal.
5. Close with the final rule: **build one narrow, reviewable workflow; improve it through evidence; expand only when trust is earned.**

#### Misconceptions to correct

- Every repeated task needs a fully autonomous agent.
- Automation should be the starting point rather than the result of understanding a workflow.
- The most impressive use case is necessarily the most valuable first use case.

#### Slide opportunities

- Pattern-selection decision tree.
- “Good first workflow” criteria.
- Candidate workflow brief.
- Follow-on course map.

#### Course closing

Return to the promise from Lesson 1: the learner now understands the system, has a working setup, can assign and supervise work, and can preserve confirmed context. Invite them to build one narrow workflow in the relevant follow-on course.

# Assessment plan

## Formative checks

Use low-friction checks throughout the course. They should not add significant video runtime.

| Point           | Check                                                  | Evidence of learning                                                     |
| --------------- | ------------------------------------------------------ | ------------------------------------------------------------------------ |
| After Lesson 2  | Retrieve the disposable setup note in a fresh session. | The learner’s environment works.                                         |
| After Lesson 3  | Explain model versus harness/app in one sentence, and sketch one chat turn. | The foundational distinction and chat/tool loop are understood. |
| After Lesson 4  | Select an autonomy level and justify it.               | The learner can match autonomy to risk.                                  |
| After Lesson 6  | Classify five information examples.                    | Context, instructions, knowledge, memory, and archive are distinguished. |
| After Lesson 8  | Write one stop-and-ask rule.                           | Permissions and human checkpoints are explicit.                          |
| After Lesson 9  | Complete a CLEAR assignment.                           | The task is executable and reviewable.                                   |
| After Lesson 11 | Revise an output using diagnostic feedback.            | The learner can supervise quality.                                       |
| After Lesson 13 | Retrieve one confirmed memory in a fresh session.      | The memory lifecycle works.                                              |

## Final practical check

Using a supplied one-page business brief, the learner asks the assistant to plan and create a short artifact, verifies it against the brief, revises it once, and saves only one confirmed decision or preference to durable memory.

### Capstone success rubric

| Criterion            | Successful evidence                                                |
| -------------------- | ------------------------------------------------------------------ |
| Outcome clarity      | The requested artifact and intended audience are explicit.         |
| Context quality      | Only relevant sources are provided and their authority is labeled. |
| Boundaries           | Constraints, non-goals, and approval points are stated.            |
| Capability awareness | The learner can explain which skills and tools are required.       |
| Verification         | Claims and requirements are checked against the brief.             |
| Feedback             | At least one revision is requested with diagnostic reasoning.      |
| Memory judgment      | Only a confirmed, reusable item is saved.                          |
| Provenance           | The saved item includes source, status, scope, and date.           |
| Retrieval            | The item can be found and used in a fresh session.                 |

# Tool setup and implementation guidance

## Recommended teaching posture

- Teach concepts and architecture in provider-neutral language.
- Demonstrate one primary assistant interface throughout the core course.
- Provide a separate Claude/Codex translation sheet for setup and terminology differences.
- Keep the canonical context in plain, human-readable files.
- Treat any memory product, vector database, or knowledge graph as an optional service around those files.
- Give every learner a no-integration fallback so account or MCP problems do not block learning.
- Do not include EVE in this course.

## Minimum tool stack

| Layer               | Course requirement                                        | Acceptable implementation                                               |
| ------------------- | --------------------------------------------------------- | ----------------------------------------------------------------------- |
| Assistant           | Conversational interface with project or workspace access | One supported Claude or OpenAI assistant interface                      |
| Canonical context   | Human-readable, learner-owned notes                       | Markdown folder                                                         |
| Retrieval or memory | Ability to find and supply relevant notes                 | Basic Memory, another compatible memory layer, or manual file selection |
| Editing             | Direct inspection and correction                          | File editor, Obsidian, or memory product interface                      |
| Course assets       | Templates, skills, and checklists                         | Downloadable Markdown files                                             |
| Backup              | Exportable copy of context                                | Versioned archive, synced folder, or version control                    |

## Setup acceptance test

The setup is ready only when the learner can:

1. Open the assistant and identify its current project or workspace.
2. List or search the intended context project.
3. Read a harmless starter note.
4. Create a clearly labeled test note.
5. Inspect and edit the resulting file or note directly.
6. Retrieve it after beginning a fresh conversation.
7. Remove the test note and disconnect the integration if necessary.

## Plain-Markdown fallback

If a memory integration fails, the learner should still be able to complete the course by:

1. Opening the course context folder.
2. Attaching or selecting the relevant Markdown files for the task.
3. Asking the assistant to propose a memory candidate after the task.
4. Confirming and manually adding the item to the appropriate note.
5. Reusing that note in a fresh conversation.

The fallback reinforces the architecture: memory is the practice of selecting, storing, retrieving, and correcting useful knowledge—not the logo of a particular product.

# Required course assets

Prepare these assets before recording:

1. **AI lingo field guide.** Short definitions, comparisons, and misconception corrections.
2. **CLEAR assignment worksheet.** A one-page fillable assignment planner.
3. **Context checklist.** Outcome, audience, sources, constraints, example, deliverable, standard, and questions.
4. **Capability and permission map.** Workflow step, information, skill, tool, permission, and approval.
5. **Starter context workspace.** Sample Markdown files for profile, business, brand, audience, offer, goals, projects, decisions, evidence, and sessions.
6. **Memory-note template.** Source, scope, status, date, confidence, owner, sensitivity, and relationships.
7. **Memory lifecycle skill.** Search, propose, confirm, write, retrieve, correct, supersede, archive.
8. **Session-start skill.** Retrieve current goals, active project state, recent decisions, and unresolved questions.
9. **Session-close skill.** Summarize work, propose memory candidates, confirm commitments, and identify next actions.
10. **Source and provenance template.** Approved, reference, draft, outdated, and archive labels.
11. **Lightweight evaluation checklist.** Facts, instruction-following, quality, preference, risk, and approval.
12. **Claude/Codex translation sheet.** Equivalent setup concepts and product-specific terminology.
13. **Troubleshooting guide.** Connection checks, permissions, missing retrieval, duplicate memories, and the Markdown fallback.
14. **Capstone brief.** One-page fictional business brief with enough information for a small reviewed artifact.
15. **Next-workflow brief.** Template used in Lesson 15.

# Guidance for the slide-generation agent

This section describes how a later agent should translate this document into lesson slides. Prefer `course-01-curriculum.html` **Slides (draft)** as the source of truth (title + bullets; one 16-bit pixel-art visual brief per content slide; optional side-panel terms; screen-share instructor-only; brand later).

## Slide principles

- Preserve the lesson objective, runtime, learner output, and closing rule.
- Give every content slide its own visual brief that reinforces that slide’s teaching point (16-bit pixel art).
- When the slide introduces technical terms, include a side panel with only those terms and ultra-short definitions.
- Avoid turning every teaching point into a bullet slide.
- Prefer diagrams, comparisons, annotated examples, checklists, and before/after artifacts.
- Keep terminology identical to the definitions in this document.
- Label examples as fictional unless they come from an approved real source.
- Do not add product claims, prices, screenshots, or interface instructions without current verification.
- Do not imply that memory, RAG, MCP, embeddings, or knowledge graphs guarantee correctness.
- Keep branding and content examples deliberately shallow; they are bridges to the next course.
- Make human approval visually explicit wherever an external or consequential action appears.

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
- Respect the learner’s business judgment.
- Avoid anthropomorphic claims and exaggerated promises.
- Define jargon immediately, then return to plain language.
- Use “the assistant may” or “the product can” instead of implying universal behavior.

## Recording discipline

- Open each lesson with the question it answers.
- Keep one example consistent across the full course.
- Explain what the learner should notice during every demonstration.
- Pause or add an on-screen prompt when a learner action is required.
- End every lesson with the reusable rule listed in its brief.
- Avoid interface details that are likely to age quickly in conceptual lessons.
- Record setup screens separately where possible so they can be replaced without re-recording the conceptual explanation.

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
- The agent’s summary is an objective record of what happened.

# Follow-on learning paths

## Course 2 — Brand and Content Systems With AI

Reserved modules and sections:

- Business and brand context setup.
- Audience, positioning, offers, and differentiation.
- Content pillars and channel strategy.
- Brand voice ontology and approved example library.
- Research, ideation, drafting, editing, repurposing, and review skills.
- Content calendar, tasks, experiments, analytics, and learning loops.
- Approval, publishing, and brand-risk controls.

## Course 3 — Your AI Second Brain and Coach

Reserved modules and sections:

- Personal operating manual and coaching preferences.
- Goals, commitments, decisions, reflections, and evidence.
- Memory scopes, consent, sensitivity, expiry, and correction.
- Coaching modes: reflect, challenge, plan, review, and accountability.
- Session-start, session-close, weekly-review, and monthly-review skills.
- Private, project, and shared-team memory.
- Shared knowledge access, roles, and conflict resolution.
- Migration from a personal file system to a hosted team context service.

## Product track — Entrepreneur AI Coach

Not part of this course, but this curriculum creates the conceptual foundation for:

- Tenant and permission architecture.
- A domain ontology and memory-write policy.
- Shared team and project context.
- Skill evaluation and regression testing.
- Human approval and high-stakes escalation.
- Memory-backend and agent-runtime selection.
- Data portability, deletion, audit, and recovery.

# Pre-production decisions

Resolve these items before the setup lesson and screenshots are recorded:

1. Select the primary demonstrated assistant interface.
2. Select the primary memory implementation for the recorded path.
3. Confirm that the Markdown fallback completes the same learning objectives.
4. Freeze and test the starter ontology and course skills.
5. Create the fictional capstone business brief.
6. Define the exact list of sensitive data learners must exclude from exercises.
7. Test setup, retrieval, export, correction, and disconnection on a clean learner account.
8. Decide which interface-specific setup details belong in replaceable companion videos.
9. Verify all product names, screenshots, availability, and plan requirements immediately before recording.

# Curriculum alignment map

| Learning objective                                                         | Primary lessons | Demonstrated by                               |
| -------------------------------------------------------------------------- | --------------- | --------------------------------------------- |
| Distinguish model, application, assistant, workflow, automation, and agent | 3–4             | Explanation plus autonomy choice              |
| Explain context and memory terminology                                     | 5–6             | Context checklist and classification exercise |
| Differentiate skills, tools, connectors, APIs, and MCP                     | 7               | Capability map                                |
| Assess permissions, risk, and approval                                     | 4, 8            | Autonomy choice and stop-and-ask rule         |
| Give a complete assignment                                                 | 9               | CLEAR worksheet                               |
| Work with sources and files                                                | 10              | Labeled source pack                           |
| Correct and verify work                                                    | 11, 14          | Diagnostic revision and capstone review       |
| Set up portable context                                                    | 2, 12           | Acceptance test and starter workspace         |
| Manage the memory lifecycle                                                | 6, 13           | Saved and retrieved confirmed memory          |
| Complete a supervised workflow                                             | 14              | Reviewed artifact and approved memory         |
| Select a valuable next workflow                                            | 15              | Candidate workflow brief                      |

# Design-source note

This draft was prepared for alignment with the Notion page **How to design a course** supplied by the course creator. During production of this file, the Notion connector required reauthentication and the shared page opened to a sign-in screen, so its private contents could not be reviewed directly.

The curriculum currently applies widely accepted course-design practices: backward design, observable learning objectives, constructive alignment, progressive complexity, short modular lessons, misconception correction, worked examples, learner action, retrieval checks, practical assessment, and accessibility. After the Notion connection is restored, reconcile this section and the instructional design approach against any additional house rules in that page before marking the curriculum final.
