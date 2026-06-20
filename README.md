# Hackademic Learning Objects

This repository stores reusable learning objects for Hackademic Solutions.

The repository supports training content for:

- AI security
- Microsoft AI adoption
- cybersecurity governance
- technical literacy foundations
- advisory services
- Skool courses
- LinkedIn content
- SCORM-ready learning modules
- xAPI-ready evidence templates
- future LMS and product delivery

## Core Idea

The goal is to create modular, reusable learning objects that can be rendered into multiple delivery formats.

A topic should become a structured learning-object folder first.

That learning-object folder can then support:

- Skool lessons
- LinkedIn posts
- slide outlines
- worksheets
- advisory assets
- SCORM metadata
- xAPI statement templates
- future LMS packages
- future product interfaces

## Source of Truth

The canonical source is the complete learning-object folder:

learning-objects/[category]/[slug]/

Each learning-object folder includes:

- index.md
- object.json
- components/
- renders/
- metadata/

The `index.md` file is the human-readable object map.

The `object.json` file is the machine-readable full object record.

The `components/` folder contains the reusable instructional substance.

The `renders/` folder contains platform-specific derivatives.

The `metadata/` folder contains SCORM, xAPI, and review-support artifacts.

Do not treat Skool, LinkedIn, slide, SCORM, xAPI, or review files as the source of truth.

## Instructional Model

This repository uses the Read-Watch-Do model:

- READ: conceptual grounding, frameworks, references, and mental models
- WATCH: demonstrations, walkthroughs, scenarios, examples, and decision points
- DO: exercises, worksheets, labs, decisions, artifacts, or applied practice

## Standards Strategy

Default standards posture:

- SCORM 1.2-ready metadata for broad LMS compatibility
- xAPI-ready statement templates for future evidence tracking
- no claim of full SCORM packaging unless actual package files are generated
- no claim of live xAPI tracking unless connected to a Learning Record Store

## Primary Workflow

1. Give Cursor Agent a topic and parameters.
2. Cursor creates a full componentized learning-object folder directly in this repository.
3. Cursor creates `index.md`, `object.json`, all default components, platform renders, and metadata files.
4. Human reviews the content.
5. Cursor fixes issues.
6. Commit to GitHub.

## Default Learning-Object Folder

For each topic, create:

learning-objects/[category]/[slug]/
  index.md
  object.json
  components/
    anticipation-prompt.md
    read-core-concepts.md
    watch-scenario.md
    do-activity.md
    quiz.md
    reflection-prompt.md
    reuse-notes.md
    suggested-next-objects.md
  renders/
    skool.md
    linkedin.md
    slides.md
  metadata/
    scorm.json
    xapi-template.json
    review-checklist.md

## Default Categories

Use one of these categories unless the user explicitly requests another:

- foundations
- microsoft-ai-adoption
- ai-governance
- ai-security
- advisory-assets

## Status Values

Use these status values:

- draft
- needs_revision
- approved
- published
