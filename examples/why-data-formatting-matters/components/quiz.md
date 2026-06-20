# Quiz: Check for understanding

Answer from the scenario in each question. These examples do not appear elsewhere in the lesson.

---

## Question 1

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

**Correct answer:** B

**Rationale:** Threshold logic depends on comparable numeric values. A currency string with symbols and commas is not the same data type as `5000`, so automation may mis-route or error even when the deal is clearly below threshold.

---

## Question 2

A manager reviews access metadata before expanding an AI assistant to more teams.

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

**Correct answer:** B

**Rationale:** The fields conflict in governance terms: access looks approved and powerful, but approval provenance is self-service and review evidence is missing. That is an accountability and evidence problem managers should catch before expansion.

---

## Question 3

An operations leader asks why an expense pre-approval bot misfires on threshold checks.

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

**Correct answer:** C

**Rationale:** For threshold automation, the urgent formatting failure is the non-numeric amount. Receipt and approval gaps may also matter operationally, but the bot cannot consistently compare `"two hundred fifty"` to `250` without fragile interpretation.

---

## Question 4

Two pipeline records feed the same executive dashboard.

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

**Correct answer:** C

**Rationale:** Forecasting rules need comparable numbers and dates. Record B reduces ambiguity; Record A forces systems to interpret shorthand that can vary by team, tool, or region.

---

## Question 5

An executive says the HR policy assistant "gives inconsistent answers." The team shares this intake record:

```json
{
  "use_case": "HR Policy Q&A Bot",
  "status": "pilot",
  "knowledge_sources": [
    "shared_drive_hr_policies",
    "email_threads"
  ],
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

**Correct answer:** C

**Rationale:** Mixed formal and informal sources without version control is a structured-data and governance intake problem. Managers should fix source definition and approval evidence before scaling, not treat inconsistency as purely a model defect.
