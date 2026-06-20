# DO: Structured workflow readiness review

## Exercise

Review the structured record below.

You are a department manager asked whether an AI-assisted security workflow should expand beyond its current pilot. The vendor demo looked fine. Your job is to read the metadata and decide whether the **data** supports reliable automation.

```json
{
  "workflow_name": "Security Alert Triage Copilot",
  "business_owner": "Security Operations",
  "status": "pilot",
  "purpose": "Summarize incoming identity alerts and recommend escalation actions",
  "sample_alert": {
    "alert_id": "SA-99214",
    "severity": "high",
    "source_system": "identity_provider",
    "user_principal": "jwells@company.com",
    "event_time": "June 18 afternoon",
    "recommended_action": "disable_account",
    "approval_status": "not_required"
  },
  "automation": {
    "ai_summary_enabled": true,
    "auto_escalate_enabled": true,
    "human_review_required": false
  },
  "governance": {
    "approved_for_production": true,
    "last_reviewed": null,
    "executive_sponsor": "CISO"
  }
}
```

Complete five tasks. Write in plain English. Do not assume you can see fields that are not shown.

## A. Plain-English summary

In two or three sentences, describe what this record appears to say about the workflow and the sample alert.

## B. Identify three fields that matter for business decision-making

Use this format:

| Field | Value | Why it matters |
|---|---|---|
| `severity` | `high` | Shows the sample alert is not a low-priority test case. |

Choose fields that would influence whether you trust automated action on a real account.

## C. Identify the highest-priority formatting or data quality issue

Multiple issues may be visible. **Prioritize one** and explain why it is more urgent than the others.

Do not treat field labels or metadata sections as a checklist of correct answers. Explain the business consequence.

## D. Readiness decision

Select one:

- **Expand** — ready for broader production use
- **Continue pilot only** — useful experiment, not ready to scale
- **Hold** — stop or freeze expansion until specific data and governance issues are corrected

Add one sentence defending your choice.

## E. Manager-level follow-up question

Write one specific question you would ask the business owner before signing off.

Name a workflow dependency and who should be accountable for fixing the data or control gap.

---

## Submission rubric

| Criterion | Meets expectation | Partial | Does not meet |
|---|---|---|---|
| Summary | Accurately describes workflow purpose, alert context, and automation scope | Omits automation or governance context | Misreads what the record describes |
| Field selection | Three fields tied to decision quality, not trivia | Fields listed without business rationale | Fields irrelevant to readiness |
| Prioritized issue | Identifies a **non-trivial** conflict or formatting problem with business consequence | Names a visible gap without prioritization or consequence | Only restates a single null field with no analysis |
| Readiness decision | Decision matches stated rationale and record evidence | Decision or rationale is vague | Decision contradicts visible record |
| Follow-up question | Specific, names dependency and accountability | Generic question to "IT" | Non-actionable or syntax-focused |

**Full credit on Task C** requires more than noting `last_reviewed` is null. Accept strong answers that prioritize, for example:

- non-machine-readable `event_time` breaking correlation and audit timelines
- `human_review_required: false` combined with `recommended_action: disable_account` and `auto_escalate_enabled: true`
- `status: pilot` conflicting with `approved_for_production: true`
- `approval_status: not_required` on a high-severity account-disable recommendation

---

## Suggested answer key (facilitator use)

### A. Plain-English summary

This record describes a pilot AI copilot that summarizes identity alerts and can auto-escalate recommended actions. The sample alert is high severity and recommends disabling an account. The workflow metadata shows automation can run without human review, while governance flags production approval even though no review date is recorded.

### B. Three fields that matter (sample responses)

| Field | Value | Why it matters |
|---|---|---|
| `recommended_action` | `disable_account` | Automated or escalated account disablement has immediate business impact. |
| `human_review_required` | `false` | Shows the workflow may act without analyst confirmation. |
| `event_time` | `June 18 afternoon` | Ambiguous timestamps weaken investigation, correlation, and audit evidence. |
| `approved_for_production` | `true` | Signals organizational intent to treat the workflow as production-ready. |
| `status` | `pilot` | Indicates the workflow is still experimental. |

### C. Strong prioritized issue (examples)

**Strong:** The most urgent issue is that `auto_escalate_enabled` is true, `human_review_required` is false, and the sample alert recommends `disable_account` for a high-severity event. That combination means formatting and control metadata allow consequential automated action without human confirmation.

**Also strong:** `event_time` is not machine-readable. Security automation and reporting depend on reliable timestamps for correlation across systems. "June 18 afternoon" forces interpretation and can break timelines during an investigation.

**Partial only:** `last_reviewed` is null. True, but that alone does not explain the automation risk visible in the alert and control fields.

### D. Readiness decision

**Hold** or **Continue pilot only** are both defensible if the rationale cites automation-on-disable-account risk, pilot/production conflict, or weak time formatting.

**Expand** should score as inconsistent unless the learner identifies a convincing reason the visible record is incomplete or misleading.

### E. Follow-up question (sample)

Who must approve changes to escalation rules before a high-severity `disable_account` recommendation can run with `human_review_required: false`, and what timestamp format will Security Operations require in alert intake before this workflow scales?
