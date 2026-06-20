# Standards Strategy

## Purpose

This repository should prepare learning objects for future standards-compatible delivery without overbuilding too early.

The content should support Skool first, but remain portable to LMS and enterprise learning environments.

## Standards Stack

The long-term standards stack includes:

- SCORM for delivery and LMS package compatibility
- xAPI for learning evidence
- LTI 1.3 for future external platform connections
- Open Badges for future credentials
- IMS Caliper as a possible higher-education evidence alternative

## SCORM Strategy

SCORM is the delivery and packaging layer.

Use SCORM to prepare content for LMS import and completion tracking.

Default target:

SCORM 1.2

Use SCORM 1.2 first because it is broadly compatible with many LMS platforms and sufficient for basic completion, pass/fail, score, and time tracking.

Do not implement advanced SCORM sequencing unless specifically requested.

For each learning object, create:

metadata/scorm.json

The SCORM metadata file should include:

- identifier
- title
- version
- description
- launch_asset
- completion_rule
- success_criteria
- estimated_time_minutes
- score_model
- interactions
- metadata
- review_notes

Important rule:

Do not claim that a complete SCORM package exists unless actual package files are generated and tested.

SCORM-ready metadata is not the same thing as a finished SCORM package.

## xAPI Strategy

xAPI is the evidence layer.

Use xAPI to describe what the learner demonstrated, submitted, completed, reflected on, or applied.

For each learning object, create:

metadata/xapi-template.json

The xAPI template should include:

- template_id
- actor_placeholder
- verb
- object
- context
- result
- evidence_artifact
- statement_example
- review_notes

Use meaningful evidence verbs such as:

- completed
- demonstrated
- submitted
- reflected
- applied
- explained
- analyzed
- defended

Avoid xAPI statements that only track passive consumption.

Weak xAPI evidence:

"Learner viewed lesson."

Better xAPI evidence:

"Learner demonstrated ability to classify an AI use case by governance risk level."

Important rule:

Do not claim live xAPI tracking exists unless connected to a Learning Record Store.

## LTI 1.3

LTI 1.3 may be useful later for connecting external platforms.

Possible future external platforms:

- Microsoft Learn
- TryHackMe
- Hack The Box
- PortSwigger Academy
- AWS Skill Builder
- other training or lab systems

LTI is a connection layer, not the primary evidence layer.

Do not build LTI support in the first version.

## Open Badges

Open Badges may be useful later for portable learner credentials.

A badge should be tied to evidence.

Do not issue badges before the curriculum, assessment model, and evidence strategy are stable.

## IMS Caliper

IMS Caliper may be relevant if the project moves into higher education partnerships.

For now, treat IMS Caliper as a future consideration.

## Current Build Rule

For the MVP:

- create SCORM 1.2-ready metadata
- create xAPI-ready statement templates
- do not create full SCORM packages unless explicitly requested
- do not connect to an LRS unless explicitly requested
- do not implement LTI, badges, or Caliper yet
- include quiz components as instructional content, not only as SCORM metadata

The first job is reliable componentized learning-object production.
