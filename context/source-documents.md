# Source Documents

This file summarizes the project source documents and explains how the Cursor agent should use them.

## The Read-Watch-Do Framework

Use this document as the instructional foundation.

Key ideas:

- READ builds conceptual understanding and strategic thinking.
- WATCH helps learners observe expert practice, demonstrations, decision points, and reasoning.
- DO turns knowledge into capability through applied practice, exercises, labs, scenarios, and artifacts.
- Intelligent agents can help orchestrate learning across all three modes.
- Content creation agents should synthesize knowledge, identify useful demonstrations, design practice scenarios, and connect learning modes into coherent pathways.

How to apply it:

- Every repo-ready learning object must include READ, WATCH, and DO components.
- WATCH may be a scenario, walkthrough, or decision example if no video is available.
- DO must require applied practice or artifact creation.
- Do not create passive content-only modules unless explicitly requested.
- Use anticipation and reflection prompts to make learning active.

## CyberTA

Use this document as the curriculum-agent and standards architecture foundation.

Key ideas:

- Curriculum plans should be structured as modular nodes, not only linear syllabi.
- Each node can include reading, video/demo, lab/practice, SCORM object, xAPI verb, and competency.
- Prerequisites should determine sequence.
- SCORM should be used for packaging and delivery.
- xAPI should be used for evidence of demonstrated learning.
- LTI 1.3 can connect external learning platforms later.
- Open Badges can support portable credentials later.
- IMS Caliper may be relevant for higher education.
- Assessment should emphasize scenario defense, annotated lab writeups, concept portfolios, and peer-teaching checks.
- Credentials should be backed by queryable evidence, not just a certificate.

How to apply it:

- Create modular, componentized learning objects.
- Include pathway and prerequisite metadata when useful.
- Include SCORM-ready metadata for LMS delivery.
- Include xAPI-ready evidence templates.
- Prefer evidence-producing activities.
- Include quiz components as instructional content.
- Do not overbuild credentialing, LTI, or live LRS integration in the first version.

## Project Conversation Context

The design direction from project planning is:

- The Custom GPT sandbox is not part of the production workflow.
- Cursor Agent is the production agent.
- GitHub is the source of truth and audit trail.
- Skool is the initial delivery platform.
- SCORM metadata should be created from day one.
- xAPI-ready templates should be created from day one.
- Full SCORM packaging and live xAPI tracking can come later.
- Initial calibration content includes Git, JSON, YAML, Markdown, and APIs.
- Strategic training pathway is Secure Microsoft AI Adoption for Mid-Sized Organizations.
- Microsoft Cloud Adoption Framework and Azure Well-Architected Framework are key sources for the first serious training product.
- Repo-ready learning objects use a componentized folder structure with paired `index.md` and `object.json`.
- Slide renders are created by default.
- Source references are required for deeper Microsoft, framework, governance, cybersecurity, AI security, legal, compliance, or standards-related subjects.

## Use of External Sources

When current framework, Microsoft, standards, or security information is needed, prefer official sources.

Preferred source types:

- Microsoft Learn
- NIST
- OWASP
- ISO pages or official summaries
- ADL or official SCORM/xAPI references
- MITRE
- official vendor documentation

Flag claims that need source verification.

Do not invent framework details.

Do not make legal, compliance, or certification claims without review.
