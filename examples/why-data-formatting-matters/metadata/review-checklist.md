# Human Review Checklist: Why Data Formatting Matters

**Review date:** 2026-06-20  
**Review pass:** Second pass (strict, weakness-focused)  
**Reviewer:** Agent bundle review

## Object metadata

- **Object ID:** hackademic-lo-foundations-why-data-formatting-matters-v1
- **Title:** Why Data Formatting Matters: A Manager's Guide to Structured Information
- **Slug:** why-data-formatting-matters
- **Pathway:** Format Plus
- **Category:** foundations
- **Status:** needs_revision
- **Human review required:** Yes

---

## Second-pass weakness findings

### 1. Learning objective — borderline, not blocking alone

**Current:** Given a simple structured data example, the learner will explain what the format communicates, identify how formatting affects data quality or automation, and describe one business risk caused by poorly structured data.

**Weakness:** Compound objective with three parallel verbs and no decision criterion. A learner can satisfy it by restating visible fields without prioritizing risk or making a readiness judgment.

**Exact fix required:**
- Rewrite objective to require a manager decision, e.g. readiness judgment (hold / pilot only / expand) plus defense of one prioritized risk tied to a field conflict or missing value in an unfamiliar example.

---

### 2. DO activity — shallow (blocking)

**Status:** Revised 2026-06-20 — new Security Alert Triage Copilot record; readiness decision, prioritization, and rubric added; Skool/SCORM/xAPI aligned.

**Weakness (original):**
- The exercise JSON includes `"missing_fields": ["reviewer"]`, which gives away the primary answer.
- Task C lists four candidate issues, three of which are explicitly visible in the record; no competing plausible issue requires judgment.
- The activity repeats the WATCH pattern (missing field breaks automation routing) without raising difficulty.
- No go/no-go recommendation, risk ranking, or accountability assignment is required.
- Learner can copy the suggested answer key with minimal interpretation.

**Exact fixes required:**
1. ~~Replace DO JSON with a record that does **not** include `missing_fields` or equivalent answer labels.~~ **Done**
2. ~~Introduce at least one field conflict so multiple issues are plausible.~~ **Done**
3. ~~Add a required **readiness decision** with one-sentence rationale.~~ **Done**
4. ~~Remove or shorten the hint list in Task C.~~ **Done**
5. ~~Add a rubric criterion for non-obvious prioritized issue.~~ **Done**

**Files updated:** `components/do-activity.md`, `renders/skool.md`, `metadata/scorm.json`, `metadata/xapi-template.json`

---

### 3. Quiz — too easy and recall-based (blocking)

**Status:** Revised 2026-06-20 — all five questions replaced with unseen scenario-based items; SCORM interactions aligned.

**Weakness (original):**
- Q1–Q4 use implausible distractors; correct answers are obvious without applying lesson concepts to new material.
- Q2 tests format recognition, not automation reasoning.
- Q5 correct answer is copied verbatim from DO activity and lesson examples — recognition, not judgment.
- No question uses an unseen JSON snippet requiring analysis.
- No question requires selecting a manager action under constraint.

**Exact fixes required:**
1. ~~Replace at least **3 of 5** questions with scenario-based items using **new** structured data not shown in READ/WATCH/DO.~~ **Done**
2. ~~Use plausible distractors grounded in common manager mistakes~~ **Done**
3. ~~Add one question requiring **prioritization**~~ **Done (Q3)**
4. ~~Remove or rewrite Q5 so it cannot be answered by matching lesson phrasing.~~ **Done**
5. ~~Align `metadata/scorm.json` interaction descriptions and correct_response values with revised quiz.~~ **Done**

**Remaining:** Re-run strict review after DO, Skool, SCORM, xAPI, and LinkedIn fixes are complete.

---

### 4. xAPI evidence — too generic (blocking)

**Status:** Revised 2026-06-20 — specific assessment object, DO rubric scoring, success tied to rubric + quiz; statement example updated.

**Weakness (original):**
- Object definition claims broad "business-level understanding" rather than a specific demonstrated capability.
- Success is anchored primarily to quiz score; DO artifact criteria are listed but not rubric-scored in `result`.
- `demonstrated` verb is appropriate, but the statement would not distinguish weak vs strong manager performance.
- No minimum evidence threshold for readiness decision or prioritized risk identification.

**Exact fixes required:**
1. ~~Narrow object definition to specific demonstrated capability.~~ **Done**
2. ~~Add rubric extensions for readiness decision and prioritized issue.~~ **Done**
3. ~~Tie `result.success` to DO artifact quality criteria, not quiz alone.~~ **Done**
4. ~~Update `statement_example` for non-trivial submission.~~ **Done**

**Files updated:** `metadata/xapi-template.json`

---

### 5. SCORM metadata — implies packaging/runtime that does not exist (blocking)

**Status:** Revised 2026-06-20 — scorm_package_exists false, null launch asset, artifact-based completion, WATCH as long-fill-in, planning-only score model notes.

**Weakness (original):**
- `launch_asset.suggested_file: "index.html"` implies a launchable SCORM asset when only metadata exists.
- Completion rule lists "Learner completes the READ section" and "WATCH/demo section" as if trackable SCORM segments exist.
- `watch_scenario_review` interaction type is `performance`, but WATCH delivery is narrated/passive in Skool render.
- Review note "Validate launch asset naming during packaging" uses packaging language inconsistent with metadata-only scope.
- `status_mapping` (passed/failed/incomplete) reads like a deployed runtime contract.

**Exact fixes required:**
1. ~~Set `launch_asset.suggested_file` to null with explicit metadata-only note.~~ **Done**
2. ~~Rewrite completion_rule to reference submitted artifacts.~~ **Done**
3. ~~Reclassify WATCH interaction as long-fill-in with learner response required.~~ **Done**
4. ~~Replace packaging language in review_notes.~~ **Done**
5. ~~Add `scorm_package_exists: false`.~~ **Done**

**Files updated:** `metadata/scorm.json`

---

### 6. LinkedIn render — generic middle (blocking for publish)

**Status:** Revised 2026-06-20 — listicle removed; executive dashboard scenario, skeptical line, and field-standardization CTA added.

**Weakness (original):**
- Strong opening hook, then devolves into listicle rhythm: "It tells… It supports… It improves… It reduces… It gives…"
- Repeats four core messages nearly verbatim from READ/Skool without a distinct advisory angle.
- No named organizational consequence, role-specific decision, or Hackademic-skeptical insight beyond the first paragraph.
- Closing soft test is useful but insufficient to differentiate from generic AI literacy posts.

**Exact fixes required:**
1. ~~Cut the listicle block; replace with one concrete executive scenario.~~ **Done (board prep / conflicting pipeline dashboards)**
2. ~~Add one skeptical line challenging "buy better AI" vs fix intake first.~~ **Done**
3. ~~Tie CTA to specific next action.~~ **Done (comment with one field + required format)**
4. ~~Ensure derivative compression, not Skool duplicate.~~ **Done**

**Files updated:** `renders/linkedin.md`

---

### 7. Skool render — too passive (blocking)

**Status:** Revised 2026-06-20 — READ checkpoints, discovery-first WATCH, inline quiz, DO rubric, and community reply step added.

**Weakness (original):**
- "Main lesson content" pastes READ material as a long passive block with no in-lesson checkpoints.
- WATCH section narrates the scenario but omits decision-point prompts from `components/watch-scenario.md`.
- Quiz is externalized: "Complete the quiz in `components/quiz.md`" — breaks flow and reduces completion friction incorrectly.
- No required learner response between READ and DO beyond opening anticipation.
- Completion action asks for a post but provides no rubric, peer reply requirement, or facilitator challenge.

**Exact fixes required:**
1. ~~Insert **stop-and-respond** prompts after READ subsections (minimum 2) and during WATCH.~~ **Done (3 READ + 6 WATCH)**
2. ~~Embed quiz questions inline — do not reference external file path.~~ **Done**
3. ~~WATCH learner task before debrief; learner identifies gap without narration first.~~ **Done (sample_record vs required_fields)**
4. ~~Add completion rubric visible to learner before submission.~~ **Done**
5. ~~Optionally require one peer reply.~~ **Done (recommended community step)**

**Files updated:** `renders/skool.md`

---

### 8. Source references — weak for cited concepts (non-blocking at intro depth)

**Weakness:**
- `source_references` contains only meta-notes, not actual references.
- Data quality dimensions table (accuracy, completeness, consistency, timeliness, validity, uniqueness) is presented without attribution; these are framework-adjacent claims.

**Exact fix required (choose one):**
- Add at least one authoritative reference for data quality dimensions (e.g. DAMA-DMBOK summary page), **or**
- Reframe dimensions as "commonly used labels" without implying standard authority, **or**
- Remove the table and keep qualitative explanation only.

**Files:** `components/read-core-concepts.md`, `index.md`, `object.json`

---

### 9. Brand voice — render drift (non-blocking, fix with Skool/LinkedIn revisions)

**Weakness:**
- READ component voice is strong (practical, skeptical, operationally fluent).
- Skool intro uses generic training phrasing ("You will learn how…").
- LinkedIn middle section reads like corporate enablement filler — inconsistent with Hackademic voice in READ and reflection.

**Exact fix:** Addressed by Skool and LinkedIn revisions above; no separate edit needed if those fixes are applied.

---

## What passed strict review (no action required)

- Folder structure and file completeness
- index.md / object.json synchronization
- Anticipation and reflection prompts (activate prior knowledge; return to opening examples)
- READ component substance and brand voice in canonical components
- SCORM/xAPI files exist and include review_notes disclaiming live tracking (disclaimers present; metadata content still overstates runtime — see fixes above)
- No unsupported compliance, legal, or Microsoft framework claims
- Reuse notes and pathway continuity logic

---

## Source verification gaps

| Item | Strict assessment |
|---|---|
| Data quality dimensions | Weak — cite or soften (see fix #8) |
| JSON / formatting claims | Acceptable at foundation depth |
| Microsoft / NIST / compliance claims | Not applicable — none made |

---

## Publish readiness decision

**Status:** needs_revision

**Decision:** Not approved. Instructional scaffolding is structurally complete, but assessment design, passive Skool delivery, generic LinkedIn derivative, and SCORM/xAPI metadata overstatement require substantive revision before publish or pilot.

### Select one

- [ ] Approved to publish as-is
- [ ] Approved with minor edits
- [x] Needs revision before publishing
- [ ] Hold for pathway/design review

---

## Required revision sequence (recommended order)

1. ~~**DO activity** — remove answer leakage; add conflict and readiness decision.~~ **Done**
2. ~~**Quiz** — replace recall items with unseen scenario questions.~~ **Done**
3. ~~**Skool render** — add checkpoints; embed quiz; active WATCH.~~ **Done**
4. ~~**SCORM + xAPI** — align metadata with actual evidence and metadata-only scope.~~ **Done**
5. ~~**LinkedIn render** — replace generic listicle with scenario + skeptical CTA.~~ **Done**
6. **Learning objective** — align with revised DO evidence requirement.
7. **Source references** — cite or soften data quality dimensions.

Re-run review after items 1–6 are complete. Item 7 may ship with pilot if dimensions are softened rather than cited.

---

## Open issues (unchanged, non-blocking)

- [ ] Confirm final placement: `examples/` vs `learning-objects/foundations/`
- [ ] Decide whether to add non-JSON worked example in READ
- [ ] Confirm Skool submission and assessment workflow for pilot
