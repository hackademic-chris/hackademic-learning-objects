# DO: Data formatting review

## Exercise

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

Complete four tasks.

## A. Plain-English summary

In two or three sentences, describe what this structured data appears to say.

## B. Identify three fields that matter for business decision-making

Use this format:

| Field | Value | Why it matters |
|---|---|---|
| `status` | `pilot` | Shows this is not yet a fully approved production workflow. |

## C. Identify one formatting or data quality issue

Look for missing, unclear, or inconsistent information.

Possible issues include:

- A required field is missing.
- A review date is blank.
- The workflow has automation enabled but is not approved for production.
- The routing process depends on a missing reviewer field.

## D. Write one manager-level follow-up question

Good questions are specific.

Weak question:

> Is this okay?

Better question:

> How will the workflow route contracts correctly when the required `reviewer` field is missing?

## Suggested answer key

### A. Plain-English summary

This structured data describes a pilot workflow that uses AI to summarize contracts and automatically route them to reviewers. It is not approved for production, and one required field, `reviewer`, is missing.

### B. Three fields that matter

| Field | Value | Why it matters |
|---|---|---|
| `status` | `pilot` | Shows the workflow is still being tested. |
| `approved_for_production` | `false` | Indicates it should not be treated as fully approved for broader use. |
| `missing_fields` | `reviewer` | The workflow needs a reviewer to route contracts correctly. |
| `auto_route_enabled` | `true` | The system can take action automatically, so data quality matters more. |
| `last_reviewed` | `null` | There is no recorded review date, which weakens governance evidence. |

### C. Data quality issue

The workflow requires a `reviewer`, but the `reviewer` field is missing.

That is a practical problem because auto-routing depends on knowing who should receive the contract.

### D. Follow-up question

How does the workflow handle contract routing when the required reviewer field is missing, and who is accountable for correcting that data before production approval?
