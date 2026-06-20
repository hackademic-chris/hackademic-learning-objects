# READ: Core concepts

## Formatting is not decoration

In everyday business use, formatting often means fonts, colors, spacing, and presentation.

In digital systems, formatting means something more important:

**Formatting is the structure that tells people and systems what information means.**

A spreadsheet column labeled `Renewal Date` tells a system where to find renewal dates.

A form field labeled `Customer Email` tells the system where to find an email address.

A JSON field labeled `"approved": true` tells the system that something has been approved.

A log entry with a timestamp tells investigators when something happened.

Good formatting makes information easier to interpret. Bad formatting forces people and systems to guess.

Guessing is not a great foundation for AI adoption. It is also not ideal for compliance, reporting, finance, operations, or most known forms of management.

## Why formatting matters for AI adoption

AI tools do not magically fix messy information. They often amplify it.

If customer records are inconsistent, AI recommendations may be inconsistent.

If policy documents are poorly labeled, AI search tools may retrieve the wrong guidance.

If product data is incomplete, AI-generated sales proposals may include incorrect details.

If employee access records are not structured, AI governance reviews may miss exposure.

The issue is not only whether an AI model is “smart.” The issue is whether the organization gives the system information in a format it can reliably interpret.

A simple business rule:

**Better structure creates better inputs. Better inputs create better outputs.**

Not perfect outputs. Better ones.

## Four core messages

### 1. Bad formatting creates bad decisions

If data is inconsistent, leaders may see different versions of the truth.

```text
Renewal date: June
Renewal: 06/15/26
Renewal_Date: 2026-06-15
Next renewal: unknown
```

A person might understand these as similar. A system may not.

One report may count the renewal. Another may miss it. A dashboard may display it incorrectly. An AI tool may infer the wrong timeline.

The decision problem begins long before the meeting. It begins when information is captured inconsistently.

### 2. AI and automation depend on structured data

Automation works best when information follows predictable patterns.

```json
{
  "invoice_id": "INV-1045",
  "amount_due": 2400.00,
  "currency": "USD",
  "due_date": "2026-07-01",
  "approval_required": true
}
```

A system can read this and know which invoice is involved, how much is due, what currency applies, when payment is due, and whether approval is required.

That structure supports automation. The system can route the invoice, flag late payments, notify an approver, update a dashboard, or feed an AI assistant.

Now compare that with:

```text
Invoice 1045 is for twenty-four hundred dollars and needs to be paid around the beginning of July. Someone should approve it.
```

A human can read that. A system has to interpret it. That interpretation may be wrong.

### 3. Managers need to recognize when data is usable, risky, or ambiguous

Managers do not need to write code.

They do need to recognize when data is:

**Usable:** clear, consistent, complete, and structured  
**Risky:** missing fields, unclear labels, inconsistent values, or weak ownership  
**Ambiguous:** understandable to a person but not reliable enough for automation

Example:

```json
{
  "employee": "Morgan Lee",
  "department": "Finance",
  "ai_tool_access": true,
  "approved_by": "",
  "last_reviewed": null
}
```

A non-technical manager can spot the issue.

The employee has AI tool access. But there is no approver. There is no review date.

That does not require coding knowledge. It requires structured thinking.

### 4. JSON is one example of why structure matters

JSON is not the only data format. It is simply a useful first example because it appears often in modern systems.

JSON may show up in AI tool configurations, automation workflows, API examples, system integrations, audit evidence, application logs, vendor documentation, security tools, learning systems, and data exchange between platforms.

A JSON example looks like this:

```json
{
  "tool": "AI Meeting Summarizer",
  "business_owner": "Operations",
  "data_access": ["calendar", "email", "shared_drive"],
  "retention_days": 365,
  "approved": false
}
```

You do not need to know how to build this. You need to know how to read it.

This example says the tool is an AI meeting summarizer, Operations owns it, it can access calendar, email, and shared drive data, data may be retained for 365 days, and it has not been approved.

That is not just technical information. That is a business risk conversation.

## What is a data format?

A data format is a standard way of arranging information.

| Format | Common use | Why managers should care |
|---|---|---|
| Table | Reports, dashboards, databases | Organizes data into rows and columns |
| Spreadsheet | Planning, tracking, analysis | Flexible but easy to make inconsistent |
| CSV | Data exports and imports | Simple format used to move data between systems |
| JSON | APIs, automation, AI tools, system records | Common format for structured data exchange |
| XML | Older integrations, enterprise systems, compliance workflows | Still used in many formal systems |
| Logs | Security, operations, troubleshooting | Records events that support investigation and accountability |
| Forms | Data collection and workflow intake | Controls how information enters a process |

This module starts with JSON because it is common in AI and automation. Future Format Plus modules can examine each format separately.

## The manager’s data formatting lens

When looking at any structured information, ask five questions:

1. What thing is being described?
2. What fields are included?
3. Are the values clear?
4. Is anything missing?
5. Could a system act on this reliably?

That last question is the automation test.

If a system cannot reliably act on the data, then automation will require manual cleanup, exception handling, or human review.

That does not mean the system is bad. It may mean the data is not ready.

## How formatting supports data quality

Data quality is usually described through dimensions like accuracy, completeness, consistency, timeliness, validity, and uniqueness.

Formatting supports all of them.

| Data quality dimension | Formatting contribution |
|---|---|
| Accuracy | Clear fields reduce misinterpretation |
| Completeness | Required fields make missing information visible |
| Consistency | Standard formats prevent different versions of the same fact |
| Timeliness | Timestamps show when data was created or updated |
| Validity | Expected formats prevent unusable values |
| Uniqueness | IDs reduce duplicate records |

Example:

```json
{
  "customer_id": "CUST-10294",
  "customer_name": "Jane Smith",
  "email": "jane.smith@example.com",
  "renewal_date": "2026-06-15",
  "status": "active"
}
```

This is more useful than:

```text
Jane is active and renews in June.
```

The second sentence may be true. The first structure is more usable.

## How formatting supports automation

Automation requires predictable inputs.

A workflow might say:

> If renewal date is within 30 days, notify account owner.

That rule depends on a clean renewal date.

This works:

```json
{
  "renewal_date": "2026-06-15",
  "account_owner": "Carlos Rivera"
}
```

This creates problems:

```json
{
  "renewal_date": "middle of June maybe",
  "account_owner": "Carlos?"
}
```

The problem is not that the automation is picky. The problem is that the business process has not defined the information clearly enough.

Automation exposes weak process design. AI does too.

## How formatting supports governance

Governance depends on evidence. Evidence needs structure.

A governance record might include:

```json
{
  "system": "AI Meeting Summarizer",
  "business_owner": "Operations",
  "data_classification": "Confidential",
  "approved": false,
  "review_required": true,
  "last_reviewed": null
}
```

This tells a manager that the system has an owner, the data is confidential, the system is not approved, a review is required, and no review date is recorded.

That is enough to trigger action. Not panic. Action.

Good formatting does not solve governance. It makes governance possible to inspect.

## What JSON is, in plain language

JSON stands for JavaScript Object Notation. You can ignore the name.

For business purposes, JSON is a structured format for describing information using labels and values.

Basic example:

```json
{
  "department": "Finance"
}
```

The label is `"department"`. The value is `"Finance"`. Together, they communicate a fact.

JSON often uses objects, lists, true/false values, numbers, and empty or missing values.

For managers, the point is not syntax perfection. The point is interpretation.

## What managers should look for in JSON

When reviewing JSON, look for:

- Ownership: Who owns this?
- Access: What information can this system use?
- Approval: Has this been reviewed or accepted?
- Dates: Is the record current?
- Retention: How long is data kept?
- Status: Is this live, retired, paused, or experimental?
- Inconsistencies: Do the fields agree with each other?

Example:

```json
{
  "status": "active",
  "approved": false
}
```

This is the kind of thing leaders should notice.

Again: not because they are technical. Because they are accountable.
