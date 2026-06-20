# Slide outline: Why Data Formatting Matters

Estimated delivery: 25–35 minutes (workshop or executive briefing)

---

## Slide 1 — Title

**Why Data Formatting Matters: A Manager's Guide to Structured Information**

Format Plus · Foundations · ~30 minutes

Speaker note: This is a business literacy lesson, not a coding lesson.

---

## Slide 2 — Learning objective

Given a simple structured data example, learners will:

- Explain what the format communicates
- Identify how formatting affects data quality or automation
- Describe one business risk caused by poorly structured data

---

## Slide 3 — Setup: messy vs structured

Side-by-side comparison:

- **Example A:** Unstructured customer notes (renewal "sometime in June," owner "maybe Carlos?")
- **Example B:** Structured JSON with labeled fields and consistent values

Discussion prompt (anticipation):

Which is easier for a system to process, automate, and trust in a dashboard?

---

## Slide 4 — READ: Formatting is not decoration

Key message:

**Formatting is the structure that tells people and systems what information means.**

Supporting points:

- AI amplifies messy inputs; it does not magically fix them
- Better structure → better inputs → better outputs (not perfect outputs)

---

## Slide 5 — READ: Four core messages

1. Bad formatting creates bad decisions
2. AI and automation depend on structured data
3. Managers must recognize usable, risky, and ambiguous data
4. JSON is one example — the same issue appears in spreadsheets, forms, logs, and CRM records

---

## Slide 6 — READ: Manager's data formatting lens

Five questions for any structured record:

1. What thing is being described?
2. What fields are included?
3. Are the values clear?
4. Is anything missing?
5. Could a system act on this reliably?

---

## Slide 7 — READ: Data quality and governance

Formatting supports accuracy, completeness, consistency, timeliness, validity, and uniqueness.

Governance depends on evidence. Structured records make gaps visible — missing approvers, null review dates, status/approval conflicts.

---

## Slide 8 — WATCH: Customer Renewal Reminder scenario

Walk through structured automation JSON:

- Active automation owned by Customer Success
- Required field missing: `account_owner`
- Workflow action: send email to account owner
- Governance shows approval, but approval does not erase the missing field

Manager takeaway: The issue is a missing business field, not JSON syntax.

---

## Slide 9 — WATCH: Decision points

Ask the room:

1. What business process is described?
2. What field is missing and why does it matter?
3. Could this automation work reliably at scale?
4. What question should a manager ask before expanding it?

---

## Slide 10 — DO: AI Contract Summary Routing

Learners review a pilot workflow JSON and submit:

1. Plain-English summary (2–3 sentences)
2. Three fields that matter for decision-making
3. One formatting or data quality issue
4. One specific manager-level follow-up question

No coding required. Output is assessable.

---

## Slide 11 — Quiz / check for understanding

Five questions covering:

- Why formatting matters for AI adoption
- Which values automation can process reliably
- Business risk when status and approval conflict
- What null review dates may indicate
- Strong vs weak manager follow-up questions

Target: 4 of 5 correct for mastery (80%).

---

## Slide 12 — Reflection

Return to opening messy vs structured customer examples.

Ask:

- Which version would you trust in a dashboard?
- What formatting standard should the team define before automating?
- Where have you seen formatting problems create business problems?

---

## Slide 13 — Closing and next steps

**Formatting is how information becomes usable. That makes it a management issue.**

Next Format Plus objects:

- Tables and dashboard disagreement
- Spreadsheets as governance traps
- JSON for AI, APIs, and automation
- Data quality for AI adoption

Soft advisory CTA: Before asking whether the AI tool is ready, ask whether the data is structured enough for the tool to be useful.
