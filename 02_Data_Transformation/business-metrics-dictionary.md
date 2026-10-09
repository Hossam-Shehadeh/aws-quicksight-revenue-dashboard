# Business Metrics Dictionary

## Status
This dictionary defines the metrics used by the live NovaTech QuickSight dashboard and the verified source data.

## Verified Metrics

| Metric | Definition | Business purpose | Source | Relevant dashboard sheet | Notes/limitations |
|--------|------------|------------------|--------|--------------------------|------------------|
| Campaign Spend | Total campaign spend. | Understand marketing investment. | Marketing Campaigns | Marketing Funnel | Live field: campaign_spend. |
| Leads Generated | Distinct lead count. | Measure demand creation. | Marketing Campaigns | Marketing Funnel | Live field: lead_id. |
| Conversion Rate | Percentage of leads or campaign participants that convert to deals. | Measure top-of-funnel effectiveness. | CRM + Marketing | Marketing Funnel | Formula and denominator must be confirmed from the source definitions. |
| Deal Amount | Revenue or amount associated with a deal. | Quantify sales value. | CRM Deals | Sales Pipeline | Use distinct deal grain when querying the unified dataset. |
| Days to Close | Number of days between the deal creation date and close date. | Measure sales cycle efficiency. | CRM Deals | Sales Pipeline | Only valid when both dates are populated and comparable. |
| Win Rate | Percentage of won deals out of all deals in a given stage or cohort. | Measure sales effectiveness. | CRM Deals | Sales Pipeline | Must be defined as won deals / total deals or won / qualified. |
| Pipeline Value | Sum of open or active deal amounts in the sales pipeline. | Track pipeline coverage and sales forecast readiness. | CRM Deals | Sales Pipeline | Must match actual stage logic. |
| Ticket Volume | Number of support tickets for a customer or account. | Measure customer support burden. | Support Tickets | Customer Health | Requires customer/account key validation. |
| Resolution Time | Difference between ticket creation and resolution. | Understand operational health and service load. | Support Tickets | Customer Health | Live field: Resolution Time (days). |
| Revenue at Risk | A derived value representing customer revenue exposed to operational or support risk. | Highlight accounts needing intervention. | Unified dataset | Customer Health | Only valid if data supports a transparent, auditable definition. |
| Customer Health Status | Classification such as Healthy, Watch, or At Risk. | Prioritize account management actions. | Unified dataset | Customer Health | Must be clearly documented and based on real observable indicators only. |

## Required Derived Metrics
The actual project should implement at least two derived fields with business meaning, using real project data. Examples include:

- Days to Close
- Campaign ROI
- Ticket Frequency
- Support Burden Index
- Revenue at Risk

These metrics must be implemented only when the source schema supports them. They cannot be invented where the data dictionary does not provide the fields.

## Implementation Notes
- Do not include raw SQL or formulas in the executive report.
- Define each derived metric in plain business language.
- Use the actual QuickSight calculation logic to produce dashboard visuals.
- Prefer formulas that map directly to observed fields and documented business rules.

## Live implementation note
The dashboard uses these definitions, but the Win Rate calculated field requires correction because the Topic response returned 81.51% while source validation returns 63.1%.
