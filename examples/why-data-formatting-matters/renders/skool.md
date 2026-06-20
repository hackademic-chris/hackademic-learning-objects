# Why Data Formatting Matters: A Manager's Guide to Structured Information

## Short intro

AI adoption, automation, reporting, and governance depend on structured information.

This lesson is active, not a read-and-forget post. You will respond at checkpoints, inspect a workflow record before the debrief, complete a readiness review, and answer five scenario questions inline.

JSON is the first worked example in the **Format Plus** pathway. The management lesson applies to spreadsheets, forms, CRM records, and dashboards too.

**Estimated time:** 30 minutes

---

## Before you begin (anticipation)

Compare these two customer records.

### Messy version

> Customer name: Jane Smith  
> Email jane.smith@example.com  
> Plan: Premium  
> Renewal date is sometime in June  
> Account owner maybe Carlos?  
> Notes: interested in AI features

### Structured version

```json
{
  "customer_name": "Jane Smith",
  "email": "jane.smith@example.com",
  "plan": "Premium",
  "renewal_date": "2026-06-15",
  "account_owner": "Carlos Rivera",
  "interest": ["AI features"]
}
```

**Post your answers before continuing:**

1. Which version would be easier for a system to process?
2. Which version would be easier to automate?
3. Which version gives a manager more confidence?
4. What could go wrong if the organization relies on the messy version?

---

## READ — Part 1: Formatting is structure

In digital systems, formatting is the structure that tells people and systems what information means.

Good formatting makes information easier to interpret. Bad formatting forces people and systems to guess.

**Checkpoint 1 — post a short reply:**

Look at the structured customer record above. Name **one field** that would matter for a renewal reminder automation and explain what could go wrong if that field were missing or vague.

Do not continue until you have posted a response.

---

## READ — Part 2: Why this matters for AI adoption

AI tools do not magically fix messy information. They often amplify it.

**Better structure creates better inputs. Better inputs create better outputs.**

Not perfect outputs. Better ones.

Four ideas to carry through the lesson:

1. Bad formatting creates bad decisions.
2. AI and automation depend on structured data.
3. Managers need to recognize when data is usable, risky, or ambiguous.
4. JSON is one example — the same problem appears in spreadsheets, forms, logs, and CRM records.

Example record for a governance conversation:

```json
{
  "tool": "AI Meeting Summarizer",
  "business_owner": "Operations",
  "data_access": ["calendar", "email", "shared_drive"],
  "retention_days": 365,
  "approved": false
}
```

You do not need to build this. You need to know how to read it.

**Checkpoint 2 — post a short reply:**

From the example above, identify **one business risk** a manager should discuss before approving wider use. Reference specific fields in the record.

---

## READ — Part 3: Manager inspection lens

When reviewing structured information, ask:

1. What thing is being described?
2. What fields are included?
3. Are the values clear?
4. Is anything missing?
5. Could a system act on this reliably?

**Checkpoint 3 — post a short reply:**

A record shows `"status": "active"` and `"approved": false` in the same object. In one or two sentences, explain why that combination should concern a manager even if the dashboard looks fine.

---

## WATCH — Inspect before the debrief

Read the record below **without scrolling ahead**. Do not look at the debrief until you post your WATCH responses.

```json
{
  "automation": {
    "name": "Customer Renewal Reminder",
    "business_owner": "Customer Success",
    "status": "active"
  },
  "data_used": {
    "systems": ["crm", "billing_platform"],
    "required_fields": ["customer_id", "renewal_date", "account_owner"],
    "sample_record": {
      "customer_id": "CUST-1044",
      "renewal_date": "2026-07-12"
    }
  },
  "workflow": {
    "trigger": "renewal_date_within_30_days",
    "action": "send_email_to_account_owner",
    "human_review_required": false
  },
  "governance": {
    "approved": true,
    "last_reviewed": "2026-04-20"
  }
}
```

**WATCH responses — post all six before reading the debrief:**

1. What business process is being described?
2. What systems does it use?
3. Compare `required_fields` to `sample_record`. What is missing or incomplete?
4. Why does that gap matter given the workflow action?
5. Could this automation work reliably at scale? Why or why not?
6. What one question should a manager ask before expanding this automation?

---

## WATCH — Debrief (read after you post)

Compare your answers to this facilitator walkthrough.

This record describes an active **Customer Renewal Reminder** owned by Customer Success. It pulls CRM and billing data, triggers when renewal is within 30 days, and sends email to the account owner without required human review.

The sample record includes customer ID and renewal date, but **not** account owner even though account owner is required. The workflow action sends email to the account owner.

If account owner is missing, the automation may fail, route incorrectly, land in an exception queue, or require manual cleanup. Governance shows approval and a review date, but approval does not erase the data gap.

**Manager takeaway:** The issue is not JSON syntax. The issue is that a business process depends on incomplete data, and structured metadata makes that visible.

---

## DO — Structured workflow readiness review

Review this record. You are deciding whether the workflow should expand beyond pilot.

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

**Submit all five parts in one post:**

1. Plain-English summary (2–3 sentences)
2. Three decision-relevant fields with why each matters
3. Highest-priority formatting or data quality issue — prioritize among visible problems; explain business consequence
4. Readiness decision: **Expand** / **Continue pilot only** / **Hold**, plus one-sentence rationale
5. One manager-level follow-up question naming a workflow dependency and accountability

### DO submission rubric (check before you post)

| Criterion | You should demonstrate |
|---|---|
| Summary | Workflow purpose, alert context, and automation scope |
| Field selection | Three fields tied to readiness or risk, not trivia |
| Prioritized issue | One **non-trivial** conflict or formatting problem with business consequence |
| Readiness decision | Decision matches your rationale and the record |
| Follow-up question | Specific; names dependency and who is accountable |

**Partial credit is not enough on the prioritized issue:** Naming only that `last_reviewed` is null, without explaining automation or formatting risk, is incomplete.

---

## Quiz — Check for understanding

Answer all five questions in one post or using the course quiz block. These scenarios are not reused from READ, WATCH, or DO.

### Question 1

A procurement team enables auto-routing when `contract_value` is below `auto_approve_threshold_usd`.

```json
{
  "workflow": "Vendor Intake Automation",
  "business_owner": "Procurement",
  "status": "active",
  "auto_approve_threshold_usd": 5000,
  "record": {
    "vendor_name": "Northline Supplies",
    "contract_value": "$4,800",
    "risk_tier": "medium",
    "security_review_complete": false
  },
  "automation": {
    "auto_route_enabled": true,
    "human_review_required": false
  }
}
```

What is the most likely **formatting-related** reason this automation produces unreliable routing decisions?

A. The vendor name should be abbreviated for system performance  
B. `contract_value` is stored as a formatted string, so numeric threshold rules may fail or behave inconsistently  
C. `risk_tier: "medium"` is too subjective for any business process  
D. Procurement ownership means IT should normalize the data later  

### Question 2

```json
{
  "employee_id": "E-4472",
  "name": "Jordan Wells",
  "department": "Marketing",
  "ai_tool": "Content Draft Assistant",
  "access_level": "full_export",
  "data_classification": "Confidential",
  "approved_by": "self-service enrollment",
  "approved": true,
  "last_reviewed": null
}
```

What is the primary business risk visible in this record?

A. Marketing should not use AI tools  
B. The record shows approved access to confidential data with export capability, but approval evidence is weak and no review date is recorded  
C. `employee_id` uses a hyphen, which makes the record invalid  
D. `full_export` is acceptable whenever `approved` is true  

### Question 3

```json
{
  "automation": "Expense Pre-Approval Bot",
  "status": "production",
  "trigger_amount_usd": 250,
  "sample_submission": {
    "submitter": "alex@company.com",
    "amount": "two hundred fifty",
    "category": "Travel",
    "receipt_attached": false,
    "manager_approval": null
  }
}
```

Which issue should the manager prioritize **first** when investigating formatting as the root cause?

A. `receipt_attached: false` — receipts should always block automation  
B. `manager_approval: null` — every submission must show approval before intake  
C. `amount` is expressed in words instead of a numeric value, so threshold rules cannot run reliably  
D. The submitter email domain should be standardized before any pilot  

### Question 4

**Record A**

```json
{
  "account": "Helios Analytics",
  "region": "EMEA",
  "revenue_usd": "1.2M",
  "close_date": "Q2",
  "pipeline_stage": "Committed"
}
```

**Record B**

```json
{
  "account": "Helios Analytics",
  "region": "EMEA",
  "revenue_usd": 1200000,
  "close_date": "2026-06-15",
  "pipeline_stage": "Committed",
  "last_updated": "2026-06-01"
}
```

Which record should a manager trust more for automated quarterly forecasting?

A. Record A, because `"1.2M"` and `"Q2"` are easier for executives to read  
B. Record A, because both records share the same account and stage  
C. Record B, because revenue and close date use consistent machine-readable formats and the record shows when it was updated  
D. Neither record matters if the dashboard looks correct  

### Question 5

```json
{
  "use_case": "HR Policy Q&A Bot",
  "status": "pilot",
  "knowledge_sources": ["shared_drive_hr_policies", "email_threads"],
  "source_document_dates": "various",
  "pii_filter_enabled": true,
  "approved_for_hr_use": false,
  "executive_sponsor": null
}
```

What is the best **manager-level next step** before approving wider rollout?

A. Purchase a more advanced model because accuracy is a vendor problem  
B. Ask IT to enable additional filters so formatting no longer matters  
C. Require a source inventory with document owner, version or effective date, and approved policy scope before expanding access  
D. Continue the pilot because `pii_filter_enabled: true` means the knowledge base is controlled  

**Quiz scoring:** 4 of 5 correct = mastery. Post your five letter answers (example: 1B 2B 3C 4C 5C).

---

## Reflection

Return to the opening messy vs structured customer examples.

**Post your reflection:**

1. Which version is more usable for AI or automation?
2. Which version is more likely to create reporting errors?
3. Which version would you trust in a dashboard?
4. What formatting standard would you want your team to define before automating this process?
5. Where have you seen formatting problems create business problems?

The point is not to make every manager technical. The point is to recognize when "the AI problem" is actually a data formatting problem with better marketing.

---

## Completion action

You are done when you have posted:

1. Anticipation answers (Before you begin)
2. READ checkpoints 1–3
3. WATCH responses (all six, before debrief)
4. DO activity (all five parts, using rubric)
5. Quiz answers (five letters)
6. Reflection (all five prompts)

**Community step (recommended):** Reply to one other member's DO post. State whether you agree with their readiness decision and identify one field they analyzed that you had not considered.

---

## Facilitator notes (do not require for learner completion)

**Quiz answer key:** 1B, 2B, 3C, 4C, 5C

**Strong DO prioritized issues:** auto-escalation without human review on `disable_account`; non-machine-readable `event_time`; `status: pilot` conflicting with `approved_for_production: true`.

**Defensible readiness decisions:** Hold or Continue pilot only when rationale cites automation or formatting risk. Expand should be challenged unless learner explains incomplete metadata.
