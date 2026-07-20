---
course_id: ai-agents-fundamentals
document_type: production-guide
status: production-draft
source_curriculum: curriculum-showcase.html
last_updated: "2026-07-20"
---

# AI Agents Fundamentals — Course Guide

This is the internal design and production reference for **AI Agents Fundamentals**. It defines why the course exists, how it should be taught, and how the curriculum should be evaluated and maintained. It is not intended to be read aloud or converted directly into slides; the companion [`curriculum-showcase.html`](./curriculum-showcase.html) is the canonical curriculum for recording and slide production.

## Course context

### Reality check

- **Why a course?** Learners need a guided sequence that combines concepts, setup, practice, feedback, and a complete supervised workflow. A glossary or tutorial would explain isolated features but would not create the intended behavior change.
- **Performance gap:** Learners have tried chat-based AI, but their work is fragmented, poorly briefed, difficult to verify, and disconnected between sessions.
- **Desired change:** Learners move from casual prompting to defining, supervising, verifying, and improving small AI-assisted workflows.
- **Audience:** Non-technical and lightly technical entrepreneurs, creators, coaches, independent professionals, and small teams.
- **Need to validate:** Pilot interviews should confirm which setup steps, concepts, and first workflows cause the most friction before the course is marked final.

### Place in the course sequence

This is the foundation course. It teaches a provider-neutral mental model, an off-the-shelf macOS setup, and one complete working loop. Persistent memory, advanced setup, business context, brand and content systems, coaching routines, and team knowledge belong in **AI Agents for Your Business**.

### Observable course outcomes

By the end, learners should be able to:

1. Explain the practical differences among a model, AI application, assistant, workflow, automation, and agent.
2. Set up an off-the-shelf AI assistant on macOS and give it focused task context using ordinary files.
3. Give, review, verify, and improve an AI assignment using explicit sources, constraints, deliverables, and success criteria.
4. Complete a low-risk supervised workflow with appropriate permissions and human approval points.

Lesson objectives in `curriculum-showcase.html` break these outcomes into smaller, observable skills.

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
8. **Prefer familiar foundations.** Use ordinary files and off-the-shelf product features before introducing integrations or memory infrastructure.
9. **Use retrieval practice.** Short “Can you explain or decide this?” checks help learners recall ideas instead of only recognizing them.
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

Distribute checks throughout the course rather than relying on a single final quiz. Give immediate, specific feedback through worked answers, comparison criteria, or a short rubric. Revisit the core loop—context → assignment → action → review—several times so recall is spaced and cumulative.

## Consistent course mental model

Use this analogy throughout the course:

| Element      | Plain-language analogy              | What it contributes                                                                 |
| ------------ | ----------------------------------- | ----------------------------------------------------------------------------------- |
| Model        | Brain or reasoning engine           | Generates, analyzes, predicts, and transforms information.                          |
| Application  | Workplace around the brain          | Adds an interface, files, search, permissions, history, and product behavior.       |
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
| AI application    | The product interface and services built around one or more models.                                                         |
| Assistant         | An AI application configured to help a person through conversation and available capabilities.                              |
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

# Assessment plan

## Formative checks

Use low-friction checks throughout the course. They should not add significant video runtime.

| Point           | Check                                                  | Evidence of learning                                                     |
| --------------- | ------------------------------------------------------ | ------------------------------------------------------------------------ |
| After Lesson 2  | Open the assistant and use one selected project file.  | The learner’s environment works.                                         |
| After Lesson 3  | Explain model versus assistant in one sentence.        | The foundational distinction is understood.                              |
| After Lesson 4  | Select an autonomy level and justify it.               | The learner can match autonomy to risk.                                  |
| After Lesson 6  | Classify five information examples.                    | Context, instructions, knowledge, memory, and archive are distinguished. |
| After Lesson 8  | Write one stop-and-ask rule.                           | Permissions and human checkpoints are explicit.                          |
| After Lesson 9  | Complete a CLEAR assignment.                           | The task is executable and reviewable.                                   |
| After Lesson 11 | Revise an output using diagnostic feedback.            | The learner can supervise quality.                                       |

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

- Teach concepts and architecture in provider-neutral language.
- Demonstrate one primary assistant interface throughout the core course.
- Provide a separate Claude/Codex translation sheet for setup and terminology differences.
- Demonstrate an off-the-shelf macOS assistant using ordinary, human-readable files.
- Mention persistent memory and MCP only at recognition level; configure them in Course 2.
- Give every learner a no-integration path so product differences do not block learning.

## Minimum tool stack

| Layer | Course requirement | Acceptable implementation |
| ----- | ------------------ | ------------------------- |
| Assistant | Off-the-shelf macOS assistant with file access | One supported Claude or OpenAI interface |
| Practice folder | Human-readable learner-owned files | Ordinary Finder folder with Markdown or text files |
| Editing | Direct inspection and correction | Built-in editor or any familiar text editor |
| Course assets | Brief, worksheet, and checklists | Downloadable Markdown or PDF files |

## Setup acceptance test

The setup is ready only when the learner can:

1. Open the assistant and identify its current project or workspace.
2. Open the dedicated practice folder or project.
3. Select or attach a harmless starter brief.
4. Ask the assistant to summarize the brief and cite the supplied facts.
5. Create a clearly labeled draft without overwriting the source.
6. Inspect and edit the draft directly.
7. Remove the disposable draft or revoke access if necessary.

## Ordinary-file fallback

If project or workspace features are unavailable, the learner should still be able to complete the course by:

1. Opening the course context folder.
2. Attaching or selecting the relevant files for the task.
3. Giving a CLEAR assignment in an ordinary conversation.
4. Saving the reviewed output as a separate file.

The fallback reinforces the foundation: useful work depends on clear context, a defined assignment, and human review—not on a particular product feature.

# Required course assets

Prepare these assets before recording:

1. **AI lingo field guide.** Short definitions, comparisons, and misconception corrections.
2. **CLEAR assignment worksheet.** A one-page fillable assignment planner.
3. **Context checklist.** Outcome, audience, sources, constraints, example, deliverable, standard, and questions.
4. **Capability and permission map.** Workflow step, information, skill, tool, permission, and approval.
5. **Practice folder.** A starter brief, source note, and safe destination for drafts.
6. **Source-label template.** Approved, reference, draft, outdated, and archive labels.
7. **Lightweight evaluation checklist.** Facts, instruction-following, quality, preference, risk, and approval.
8. **Assistant translation sheet.** Equivalent setup concepts and product-specific terminology.
9. **Troubleshooting guide.** Account, file-access, permission, and ordinary-file fallback checks.
10. **Capstone brief.** One-page fictional business brief with enough information for a small reviewed artifact.

# Guidance for the slide-generation agent

This section describes how a later agent should translate this document into lesson slides.

## Slide principles

- Preserve the lesson objective, runtime, learner output, and closing rule.
- Use one visual model per lesson whenever a relationship or sequence benefits from it.
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

- The model and the AI product are the same thing.
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
- Can they explain the model–application–assistant distinction in their own words?
- Can they complete the setup acceptance test on a clean account?
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
| Explain models, applications, assistants, workflows, automations, and agents | 3–4 | One-sentence explanation and autonomy choice |
| Set up an assistant and provide focused context with ordinary files | 2, 5–6 | Setup test, starter brief, and context checklist |
| Give, review, verify, and improve a well-sourced assignment | 7, 9–11 | Capability map, CLEAR worksheet, source pack, and diagnostic revision |
| Complete a low-risk workflow with appropriate approval points | 4, 8, 12 | Autonomy choice, stop-and-ask rule, and reviewed capstone artifact |

# Design source

This guide incorporates the course creator’s Notion page, [How to design a course](https://app.notion.com/p/ecovirtual/How-to-design-a-course-25ab9164a01f8087a473e53dc68de3a6), reviewed on 2026-07-20. Its key requirements are reflected here: validate the need and desired performance change, define a small set of course outcomes plus lesson-level objectives, progress from simple to complex, manage cognitive load, activate prior knowledge, combine examples with practice and reflection, use frequent retrieval and timely feedback, support accessibility and inclusion, pilot with a small group, measure the outcomes, and iterate regularly.
