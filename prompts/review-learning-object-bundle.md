# Review Learning Object Bundle

Use this prompt to review an existing Hackademic componentized learning-object folder.

## Task

Review the specified learning-object folder.

Fix minor formatting and consistency issues directly.

For substantive issues, update metadata/review-checklist.md and flag them for human review.

## Folder to Review

learning-objects/[category]/[slug]/

## Required Files to Review

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

## Review Areas

Check:

1. Folder completeness
2. index.md YAML front matter validity
3. object.json validity
4. index.md and object.json synchronization
5. Required component completeness
6. Audience fit
7. Business purpose fit
8. Learning objective quality
9. Read-Watch-Do quality
10. Anticipation prompt quality
11. Reflection prompt quality
12. Quiz quality
13. DO activity quality
14. Skool render usefulness
15. LinkedIn render strength
16. Slide render usefulness
17. SCORM 1.2 metadata quality
18. xAPI evidence quality
19. Brand voice
20. Unsupported claims
21. Source verification needs
22. Publish readiness

## Learning Objective Review

The learning objective should be observable.

Weak:

Understand JSON.

Better:

Explain how JSON supports structured AI outputs and identify one security risk caused by malformed or untrusted JSON.

## DO Activity Review

The DO activity should require practical application.

Weak:

Think about how this applies to your work.

Better:

Review a sample AI output formatted as JSON and identify two places where structure improves validation, automation, or security review.

## Quiz Review

The quiz should check understanding and should not be trivia for trivia's sake.

For foundation topics, 3 to 5 questions are usually enough.

For deeper topics, use scenario-based questions and rationales.

## SCORM Review

Check that metadata/scorm.json includes:

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

Confirm that the file does not claim a full SCORM package exists.

## xAPI Review

Check that metadata/xapi-template.json includes:

- template_id
- actor_placeholder
- verb
- object
- context
- result
- evidence_artifact
- statement_example
- review_notes

The xAPI statement should capture meaningful learning evidence.

Weak:

Learner viewed lesson.

Better:

Learner demonstrated ability to classify an AI use case by governance risk level.

## Source Review

For deeper Microsoft, framework, governance, cybersecurity, AI security, legal, compliance, or standards-related subjects, source references are required.

If sources are missing, flag source verification needed.

Do not invent framework details.

## Synchronization Review

Confirm:

- index.md and object.json both exist.
- Titles match.
- Slugs match.
- Object IDs match.
- Pathway values match.
- Categories match.
- Audience values match.
- Business purpose values match.
- Status values match.
- Component references match actual files.
- Render references match actual files.
- Metadata references match actual files.
- Source reference lists are consistent.

## Final Response

After review, summarize:

- folder reviewed
- files reviewed
- minor fixes made
- major issues flagged
- source verification status
- publish readiness decision
- recommended next action

Do not paste full file contents unless asked.
