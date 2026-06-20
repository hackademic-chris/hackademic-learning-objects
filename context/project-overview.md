# Project Overview

## Project Name

Hackademic Learning Objects

## Owner

Hackademic Solutions

## Purpose

This project creates reusable, componentized learning objects for AI security, Microsoft AI adoption, cybersecurity governance, and technical literacy training.

The goal is to build a production workflow where a Cursor-based AI agent can take a topic and create structured learning assets that are ready for review, reuse, and future packaging.

## Current Business Context

Hackademic Solutions is an AI security advisory firm in startup mode.

The firm is building training content to support:

- audience building
- LinkedIn visibility
- Skool-based training
- low-cost paid courses
- advisory services
- future corporate training
- future LMS delivery
- eventual productization

## Current Delivery Platform

The first delivery platform is Skool.

Skool is used for speed, audience-building, and early course validation.

However, content should not be authored only for Skool.

The source content should be reusable across many formats.

## Long-Term Vision

The long-term vision is to create modular learning objects that can be pushed into different interfaces, including:

- Skool
- LMS platforms
- SCORM packages
- web courses
- email courses
- slide decks
- PDFs
- chat-based tutors
- workshops
- advisory templates
- future custom learning portals

## Core Design Principle

Create the learning-object folder first.

Render the learning object into platform-specific formats second.

Bad pattern:

Topic -> Skool lesson

Better pattern:

Topic -> Componentized learning-object folder -> Skool lesson
                                             -> LinkedIn post
                                             -> slide outline
                                             -> SCORM metadata
                                             -> xAPI template
                                             -> worksheet
                                             -> advisory asset

## Production Agent Goal

The production agent should live in Cursor and work directly inside this repository.

The agent should be able to:

1. Accept a topic and basic parameters.
2. Classify the content.
3. Create a componentized learning-object folder.
4. Create `index.md` and `object.json`.
5. Create all default instructional components.
6. Create platform renders.
7. Create SCORM-ready metadata.
8. Create xAPI-ready templates.
9. Create a human review checklist.
10. Save all files directly into the repository.
11. Support review and revision.
12. Prepare content for GitHub version control.

## Default Learning-Object Folder

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

## Custom GPT Status

The Custom GPT sandbox idea is not part of the production workflow.

The production system is:

Cursor Agent + Repository Instructions + Context Files + Templates + Schemas + GitHub
