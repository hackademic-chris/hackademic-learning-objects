# WATCH: Scenario walkthrough

## Scenario: reading structured data like a manager

Use this example in a short video, live workshop, or Skool lesson.

**Delivery order:** Show the JSON first. Require learner responses before narration or debrief.

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

## Decision points (learner responds before debrief)

Ask learners:

1. What business process is being described?
2. What systems does it use?
3. Compare `required_fields` to `sample_record`. What is missing or incomplete?
4. Why does that gap matter given the workflow action?
5. Could this automation work reliably at scale? Why or why not?
6. What one question should a manager ask before expanding this automation?

## Narration guide (facilitator debrief after learner responses)

Start with what the data describes.

This JSON describes an automation called **Customer Renewal Reminder**. It is active. Customer Success owns it.

Now inspect the data used.

The automation uses CRM and billing platform data. It requires customer ID, renewal date, and account owner.

The sample record includes customer ID and renewal date, but not account owner.

That matters because the workflow action is to send an email to the account owner.

If the account owner is missing, the automation may fail, send to the wrong person, create an exception queue, or require manual cleanup.

Now inspect the workflow.

The automation triggers when a renewal date is within 30 days. It sends an email. Human review is not required.

That may be fine, but only if the data is reliable.

Now inspect governance.

The automation is approved and was last reviewed on April 20, 2026. That is useful, but approval does not erase the missing field problem.

## Manager takeaway

The issue is not "JSON."

The issue is that a business process depends on incomplete data.

Structured data makes that visible.

That visibility allows the manager to ask a useful question:

> How does the automation handle customers with no assigned account owner?

That is a management question, not a coding question.
