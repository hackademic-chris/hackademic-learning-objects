# Instructional Framework

## Core Model

This repository uses the Read-Watch-Do framework.

The purpose of the framework is to build learning objects that support conceptual understanding, expert observation, and applied practice.

Most learners overuse one learning mode.

Some read but do not practice.

Some watch demonstrations but do not understand the underlying principles.

Some do hands-on activities without building a conceptual model.

Read-Watch-Do forces balance.

## READ

READ is for deep engagement with complex material.

Use READ to provide:

- conceptual grounding
- frameworks
- definitions
- mental models
- technical explanations
- policy references
- architecture principles
- research-backed interpretation
- source-based summaries

READ should help the learner understand why the concept matters.

READ is not just a wall of text.

It should be concise, structured, and connected to the rest of the learning object.

Default component:

components/read-core-concepts.md

## WATCH

WATCH is for purposeful observation.

WATCH may include:

- demonstration
- walkthrough
- case scenario
- decision example
- expert reasoning pattern
- annotated example
- before-and-after comparison
- short video suggestion
- guided observation prompt

WATCH is not passive video consumption.

The learner should know what to watch for.

The section should highlight:

- decisions
- tradeoffs
- warning signs
- patterns
- reasoning
- expert judgment

For executive or management content, WATCH may be a scenario rather than a video.

Default component:

components/watch-scenario.md

## DO

DO is for applied practice.

DO should require the learner to produce something, decide something, explain something, analyze something, or complete something.

Examples:

- worksheet
- checklist
- scenario response
- policy review
- risk classification
- use-case analysis
- governance decision
- threat model
- lab activity
- annotated writeup
- concept explanation
- executive decision memo
- mini portfolio artifact

DO does not always mean technical hands-on keyboard work.

For leaders, DO may mean making a decision under constraints.

For managers, DO may mean identifying gaps in a workflow.

For practitioners, DO may mean completing a lab or technical analysis.

Default component:

components/do-activity.md

## Anticipation Prompt

Each learning object must include an anticipation prompt before instruction begins.

The anticipation prompt should ask the learner to predict, estimate, explain, or decide based on their current understanding.

Examples:

- What do you think this concept allows an organization to do?
- What do you think the biggest risk is in this scenario?
- How would you currently approach this problem?
- What do you expect to learn from this module?
- What do you already believe about this topic?

The prompt should activate prior knowledge and create a comparison point for reflection.

Do not make it decorative.

Default component:

components/anticipation-prompt.md

## Quiz Component

Each repo-ready learning object must include a quiz component.

Default component:

components/quiz.md

The quiz should check understanding and support evidence of learning.

For foundation topics, a short quiz may be enough.

For deeper Microsoft, governance, AI security, cybersecurity, or framework topics, use scenario-based quiz questions where possible.

Quiz questions should include answer rationales when useful.

## Reflection Prompt

Each learning object must include a reflection prompt after instruction.

The reflection should ask the learner to compare what they thought before with what they understand now.

Examples:

- What changed in your thinking?
- What would you do differently in a real organization?
- What assumption did this module challenge?
- What question would you now ask before approving this AI use case?
- What risk would you look for first?

Default component:

components/reflection-prompt.md

## Assessment Philosophy

Assessment should focus on evidence of understanding and judgment.

Useful evidence includes:

- scenario defense
- annotated worksheet
- checklist completion
- concept portfolio
- peer-teaching explanation
- governance artifact
- risk review
- decision memo
- lab writeup
- applied analysis

Traditional quizzes can be used, but they should not be the only evidence when deeper judgment matters.

## Component Rule

Every repo-ready learning object should connect:

READ -> WATCH -> DO

The learner should understand the concept, observe how it appears in practice, and then apply it.
