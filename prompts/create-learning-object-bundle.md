# Create Learning Object Bundle

Use this prompt to create a new Hackademic componentized learning-object folder directly inside the repository.

## Task

Create a complete repo-ready learning-object folder directly inside this repository.

Do not merely print the content in chat.

Create the actual files.

## Required Inputs

Topic:
Audience:
Business purpose:
Technical depth:
Category:
Pathway:
Delivery:
Brand voice:
Source requirements:

## Required Folder

Create:

learning-objects/[category]/[slug]/

Replace [slug] with a lowercase kebab-case slug based on the title.

Use the selected category unless the selected category is clearly wrong. If the category is changed, explain why in metadata/review-checklist.md.

## Required Files

Inside the learning-object folder, create:

index.md
object.json

components/anticipation-prompt.md
components/read-core-concepts.md
components/watch-scenario.md
components/do-activity.md
components/quiz.md
components/reflection-prompt.md
components/reuse-notes.md
components/suggested-next-objects.md

renders/skool.md
renders/linkedin.md
renders/slides.md

metadata/scorm.json
metadata/xapi-template.json
metadata/review-checklist.md

## index.md Requirements

Create:

index.md

Use Markdown with YAML front matter.

The YAML front matter must include:

object_id:
title:
slug:
pathway:
category:
audience:
business_purpose:
technical_depth:
estimated_duration_minutes:
content_type:
delivery_platforms:
scorm_target:
xapi_ready:
status:
human_review_required:
components:
renders:
metadata:
source_references:
version:
last_updated:

The Markdown body must include:

# Title

## Overview

## Learning Objective

## Component Map

## Render Map

## Metadata Map

## Source and Reference Notes

## Review Status

## object.json Requirements

Create:

object.json

Use valid JSON.

The JSON file must include the same core metadata as `index.md`.

Include:

object_id
title
slug
pathway
category
audience
business_purpose
technical_depth
estimated_duration_minutes
content_type
delivery_platforms
scorm_target
xapi_ready
status
human_review_required
learning_objective
components
renders
metadata
source_references
version
last_updated

The YAML front matter in `index.md` and the metadata in `object.json` must stay synchronized.

## Component Requirements

Create all default component files.

### components/anticipation-prompt.md

Include a prompt that asks the learner to predict, explain, decide, or estimate before instruction begins.

### components/read-core-concepts.md

Include the core conceptual explanation.

Use clear, practical, academically grounded language.

For deeper Microsoft, framework, governance, cybersecurity, AI security, legal, compliance, or standards-related subjects, include source references or flag source verification needed.

### components/watch-scenario.md

Include a demonstration, scenario, walkthrough, case, decision pattern, or observation activity.

WATCH does not have to be a video.

### components/do-activity.md

Include applied practice.

The learner should produce something, decide something, explain something, analyze something, complete something, or create an artifact.

### components/quiz.md

Include a lightweight quiz or check-for-understanding.

For foundation topics, include 3 to 5 questions.

For deeper subjects, prefer scenario-based questions with rationales.

### components/reflection-prompt.md

Include a post-module reflection prompt.

The reflection should ask what changed in the learner's thinking or what they would do differently.

### components/reuse-notes.md

Explain how this object can be reused as free content, paid course content, and advisory support.

### components/suggested-next-objects.md

Suggest related learning objects.

## Render Requirements

### renders/skool.md

Create a Skool-ready lesson assembled from the components.

Include:

- lesson title
- short intro
- estimated time
- before-you-begin prompt
- main lesson content
- watch/demo or scenario section
- do activity
- quiz/check-for-understanding
- reflection/discussion prompt
- completion action

### renders/linkedin.md

Create a LinkedIn-ready post.

Include:

- strong opening hook
- practical explanation
- concrete example
- useful takeaway
- soft call to action

Avoid generic hashtags unless they genuinely help.

### renders/slides.md

Create a slide outline or slide-ready teaching structure.

Include:

- title slide
- learning objective
- setup or problem slide
- READ concept slides
- WATCH scenario slide
- DO activity slide
- quiz/check slide
- reflection slide
- closing/next-step slide

## SCORM Metadata Requirements

Create:

metadata/scorm.json

Use valid JSON.

Include:

identifier
title
version
description
launch_asset
completion_rule
success_criteria
estimated_time_minutes
score_model
interactions
metadata
review_notes

Default SCORM target:

SCORM 1.2

Do not claim that a full SCORM package exists.

## xAPI Template Requirements

Create:

metadata/xapi-template.json

Use valid JSON.

Include:

template_id
actor_placeholder
verb
object
context
result
evidence_artifact
statement_example
review_notes

Use evidence-oriented verbs.

Prefer:

completed
demonstrated
submitted
reflected
applied
explained
analyzed
defended

## Review Checklist Requirements

Create:

metadata/review-checklist.md

Include:

- technical accuracy review
- audience fit review
- learning objective review
- Read-Watch-Do review
- anticipation/reflection review
- quiz review
- assessment review
- SCORM readiness review
- xAPI readiness review
- brand voice review
- source verification review
- index/object synchronization review
- publish readiness decision
- open issues

Use status values:

- draft
- needs_revision
- approved
- published

## Quality Rules

Use Hackademic Solutions voice:

- practical
- academically grounded
- clear
- skeptical
- useful
- operationally fluent

Avoid:

- AI hype
- generic corporate training filler
- unsupported claims
- shallow activities
- vague learning objectives
- unnecessary technical jargon

## Source Reference Rule

For deeper Microsoft, framework, governance, cybersecurity, AI security, legal, compliance, or standards-related subjects, source references are required.

If sources are not available in the current context, flag source verification needed in metadata/review-checklist.md.

## Final Response

After creating the files, summarize:

- folder created
- files created
- slug used
- category used
- estimated duration
- source verification status
- major review issues
- suggested next related objects

Do not paste the full file contents unless asked.
