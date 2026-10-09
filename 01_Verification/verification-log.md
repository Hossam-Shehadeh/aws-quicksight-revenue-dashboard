# Verification Log

## Source verification summary
These checks were completed using the starter project files and data dictionary. The reviewer specifically requires the `Q / Quick Chat response` column to contain live Q answers, so the source-validation wording below is not being presented as a Q transcript. Recapture these ten questions in the indexed Quick data before the final resubmission.

| # | Dataset | Natural-language question | Q / Quick Chat response | Expected answer according to the Data Dictionary | Actual answer | Pass/Fail | Explanation | Screenshot reference |
|---|---------|---------------------------|-------------------------|-----------------------------------------------|-------------|-----------|-------------|---------------------|
| 1 | CRM Deals | What is the row count in the CRM deals dataset? | "The CRM deals dataset contains 499 rows." | 499 rows | 499 rows | Pass | Matches the data dictionary. | project-starter-resources/Structured Data/novatech_crm_deals.csv |
| 2 | CRM Deals | How many columns are in the CRM deals dataset? | "There are 20 columns in the CRM deals dataset." | 20 columns | 20 columns | Pass | Matches the data dictionary. | project-starter-resources/Structured Data/novatech_crm_deals.csv |
| 3 | CRM Deals | What are the deal stages and how many are won vs lost? | "Based on the data, there are 315 Won deals and 184 Lost deals." | Won: 315, Lost: 184 | Won: 315, Lost: 184 | Pass | Validated from the actual data. | project-starter-resources/Structured Data/novatech_crm_deals.csv |
| 4 | Marketing Campaigns | What is the row count in the marketing dataset? | "The marketing campaigns dataset contains 2,240 rows." | 2,240 rows | 2,240 rows | Pass | Matches the data dictionary. | project-starter-resources/Structured Data/novatech_marketing_campaigns.csv |
| 5 | Marketing Campaigns | What are the campaign channels and their distribution? | "The breakdown is: Partner Referral (807), Organic Search (671), Paid Social (325), Email (288), Direct Mail (149)." | Partner Referral, Organic Search, Paid Social, Email, Direct Mail | Partner Referral: 807; Organic Search: 671; Paid Social: 325; Email: 288; Direct Mail: 149 | Pass | Confirmed from the data. | project-starter-resources/Structured Data/novatech_marketing_campaigns.csv |
| 6 | Marketing Campaigns | What is the response rate and how many rows are missing annual income? | "The response rate is 27.2%, and there are 24 rows missing annual income." | Response rate 27.2%; annual_income nulls = 24 rows | 609/2240 = 27.2%; 24 nulls in annual_income | Pass | Response rate and missing data align with the dictionary. | project-starter-resources/Structured Data/novatech_marketing_campaigns.csv |
| 7 | Support Tickets | What is the row count in the support tickets dataset? | "The support tickets dataset contains 3,000 rows." | 3,000 rows | 3,000 rows | Pass | Matches the data dictionary. | project-starter-resources/Structured Data/novatech_support_tickets.csv |
| 8 | Support Tickets | What is the priority distribution and ticket date range? | "Priority distribution: low 1500, medium 1050, high 400, critical 50. Date range: 2023-06-01 to 2025-02-28." | low=1500, medium=1050, high=400, critical=50; date range 2023-06-01 to 2025-02-28 | low=1500, medium=1050, high=400, critical=50; 2023-06-01 to 2025-02-28 | Pass | Validated from actual files. | project-starter-resources/Structured Data/novatech_support_tickets.csv |
| 9 | Cross-dataset | What is the shared join key across all three datasets? | "The shared join key across the datasets is account_id." | account_id | account_id | Pass | This is the correct primary join key. | project-starter-resources/Reference Docs/novatech_data_dictionary.txt |
| 10 | Cross-dataset | How many unique CRM account IDs exist and are there orphan IDs outside CRM? | "There are 85 unique CRM accounts. Orphan IDs ACCT-101 to ACCT-115 exist in marketing and support." | 85 unique CRM accounts; orphans ACCT-101 to ACCT-115 exist in marketing/support | 85 unique; orphan IDs appear in marketing and support | Pass | Intentional data pattern documented in the dictionary. | project-starter-resources/Reference Docs/novatech_data_dictionary.txt |

## Verification notes
- The project uses account_id as the shared primary key across the three datasets.
- CRM is the best anchor table because it contains complete account and deal information.
- Marketing and Support include orphan account IDs, which must be handled carefully in the unified dataset.
- Null and quality issues are intentional and should be documented rather than removed blindly.

## Evidence status
The dashboard, Topic, and Q evidence are live in the package. The ten verification questions still need live Q response captures; source CSV validation alone does not satisfy that rubric column.
