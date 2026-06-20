# Why Data Formatting Matters: A Manager’s Guide to Structured Information

## Short intro

AI adoption, automation, reporting, and governance all depend on structured information.

This lesson explains why data formatting is not a cosmetic issue. It is how systems know what information means.

You will learn how formatting affects data quality, automation, AI outputs, and business decisions. JSON is used as the first practical example, but this lesson is part of the broader **Format Plus** pathway.

## Estimated time

30 minutes

## Before you begin

Look at these two examples.

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

Before continuing, answer:

1. Which version would be easier for a system to process?
2. Which version would be easier to automate?
3. Which version gives a manager more confidence?
4. What could go wrong if the organization relies on the messy version?

## Main lesson content

Formatting is not decoration.

In digital systems, formatting is the structure that tells people and systems what information means.

Good formatting makes information easier to interpret. Bad formatting forces people and systems to guess.

AI tools do not magically fix messy information. They often amplify it.

A simple business rule:

**Better structure creates better inputs. Better inputs create better outputs.**

Not perfect outputs. Better ones.

### Four core messages

1. **Bad formatting creates bad decisions.** Inconsistent dates, names, approval fields, and ownership fields create conflicting reports and weak decisions.
2. **AI and automation depend on structured data.** Automation works best when information follows predictable patterns.
3. **Managers need to recognize when data is usable, risky, or ambiguous.** This does not require coding. It requires structured thinking.
4. **JSON is one example of why structure matters.** The same problem appears in spreadsheets, forms, tables, logs, CSV files, dashboards, and compliance evidence.

Example:

```json
{
  "tool": "AI Meeting Summarizer",
  "business_owner": "Operations",
  "data_access": ["calendar", "email", "shared_drive"],
  "retention_days": 365,
  "approved": false
}
```

You do not need to build this.

You need to know how to read it.

This example says:

- The tool is an AI meeting summarizer.
- Operations owns it.
- It can access calendar, email, and shared drive data.
- Data may be retained for 365 days.
- It has not been approved.

That is not just technical information. That is a business risk conversation.

## Watch/demo scenario

Review this example:

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
    "missing_fields": ["account_owner"]
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

This JSON describes an automation called **Customer Renewal Reminder**. It is active. Customer Success owns it.

The automation uses CRM and billing platform data. It requires customer ID, renewal date, and account owner.

But one field is missing: account owner.

That matters because the workflow action is to send an email to the account owner.

If the account owner is missing, the automation may fail, send to the wrong person, create an exception queue, or require manual cleanup.

The issue is not “JSON.”

The issue is that a business process depends on a missing field.

Structured data makes that visible.

## Do activity

Review the structured data below.

You are a department manager reviewing whether an AI-enabled workflow is ready for broader use.

```json
{
  "workflow_name": "AI Contract Summary Routing",
  "business_owner": "Legal Operations",
  "status": "pilot",
  "purpose": "Summarize incoming contracts and route them to the correct reviewer",
  "data_inputs": [
    "contract_document",
    "vendor_name",
    "contract_value",
    "department",
    "risk_level"
  ],
  "required_fields": [
    "vendor_name",
    "contract_value",
    "department",
    "risk_level",
    "reviewer"
  ],
  "missing_fields": [
    "reviewer"
  ],
  "automation": {
    "ai_summary_enabled": true,
    "auto_route_enabled": true,
    "human_review_required": true
  },
  "governance": {
    "approved_for_production": false,
    "pilot_end_date": "2026-07-31",
    "last_reviewed": null
  }
}
```

Submit:

1. A two-sentence plain-English summary
2. Three fields that matter for business decision-making
3. One formatting or data quality issue
4. One manager-level follow-up question

A good follow-up question is specific.

Weak question:

> Is this okay?

Better question:

> How will the workflow route contracts correctly when the required `reviewer` field is missing?

## Quiz/check for understanding

Complete the quiz in `components/quiz.md` or in the course assessment area.

## Reflection/discussion prompt

Return to the opening examples.

Which version is more usable for AI or automation?

Which version is more likely to create reporting errors?

Which version would you trust in a dashboard?

What formatting standard would you want your team to define before automating this process?

The point is not to make every manager technical.

The point is to help managers recognize when “the AI problem” is actually a data formatting problem with better marketing.

## Completion action

Post your response to the activity:

1. Plain-English summary
2. Three important fields
3. One formatting or data quality issue
4. One manager-level follow-up question

Then add one sentence answering this:

> Where have you seen formatting problems create business problems?
