# NovaTech Revenue Intelligence & AI Decision Platform

## Project Overview
This project is a BI and AI case study for NovaTech Solutions, a B2B SaaS company. The objective is to unify marketing, sales, and customer support data into a single revenue intelligence dashboard and validate the resulting insights using QuickSight and Q.

## Verified Project Facts
The following facts were verified directly from the starter CSV files in the project resources folder:

- CRM Deals: 499 rows, 20 columns
- Marketing Campaigns: 2,240 rows, 20 columns
- Support Tickets: 3,000 rows, 20 columns
- Shared join key across all three datasets: account_id
- CRM account coverage: 85 unique accounts
- Marketing orphan IDs: ACCT-101 through ACCT-115, intentionally not in CRM
- Support orphan IDs: ACCT-101 through ACCT-115, intentionally not in CRM
- CRM deal date range: 2023-06-17 to 2025-01-25
- Marketing campaign date range: 2023-01-01 to 2025-01-31
- Support ticket date range: 2023-06-01 to 2025-02-28

## Business Problem
The Revenue Operations team manually combines reports from multiple systems every week. This creates operational drag and limits visibility into how marketing campaigns influence sales outcomes and customer health. The project addresses the need to understand:

- marketing campaign performance
- lead-to-deal conversion
- sales pipeline health
- win rates and lost deal reasons
- support burden and customer risk
- natural-language insight using QuickSight Q

## Solution
The project is structured to:

1. verify source schemas and data quality
2. import the datasets into QuickSight SPICE
3. clean and transform data using no-code preparation
4. create a unified dataset using account_id
5. build a multi-sheet executive dashboard
6. configure Topic vocabulary for Q
7. compare AI responses to dashboard logic
8. package artifacts for submission

## Architecture
The project data pipeline is:

CRM + Marketing + Support
→ Data quality review
→ Transformation and metric creation
→ Unified account-level dataset
→ SPICE
→ Dashboard + AI / Q
→ Business insights and executive recommendations

## Data Sources
The starter project includes the following verified source files:

- project-starter-resources/Structured Data/novatech_crm_deals.csv
- project-starter-resources/Structured Data/novatech_marketing_campaigns.csv
- project-starter-resources/Structured Data/novatech_support_tickets.csv
- project-starter-resources/Reference Docs/novatech_data_dictionary.txt

## Verified Quality Findings
These findings were checked against the starter files and the data dictionary:

- CRM nulls: 315 total, primarily in loss_reason for won deals
- Marketing nulls: 24 total, all in annual_income
- Support nulls: 118 total, in ticket_resolved_date and customer_sentiment
- CRM deal stages: 315 Won, 184 Lost
- Support priority distribution: low 1500, medium 1050, high 400, critical 50
- Marketing response rate: 609 / 2240 = 27.2%
- Marketing fields include documented orphan account IDs not present in CRM

## Data Strategy
The required join strategy is to use account_id as the common key. The CRM table is the most appropriate anchor table because it contains the core business account records and deal outcomes. Marketing and Support are then joined to account_id to build the unified customer health layer.

## Dashboard Requirements
The local project package includes the required dashboard story structure and documentation for:

- Marketing Funnel
- Sales Pipeline
- Customer Health
- AI / Q validation
- Executive reporting

## AI / Natural Language Analytics
The AI workflow includes:

- baseline Q questions before Topic configuration
- Topic vocabulary alignment with actual business terms
- same-question comparison before and after Topic tuning
- Q exploration log and AI-vs-dashboard comparison

## Business Metrics
The project uses real, traceable metrics from the dataset, including:

- Days to Close
- Campaign ROI
- Ticket resolution time
- Support burden using tickets_last_30_days
- Revenue contribution by account

## Technical Skills Demonstrated
- data validation and quality review
- QuickSight data preparation and SPICE modeling
- dashboard design and interactivity
- AI / Q evaluation workflow
- executive storytelling
- portfolio documentation

## Project Limitations
The live QuickSight layer is published and the package includes live dashboard, Q, Topic, and PDF evidence. Remaining rubric risks are the join/data-preparation screenshots, a real data-type-correction screenshot, one-click filter and cross-sheet navigation evidence, 3-5 visible dashboard annotations, and replacing the CSV-only verification responses with actual Q responses.

## Final evidence items still required in AWS/Vocareum
To close the remaining rubric gaps, capture these items in the live environment:

1. SPICE import counts and dataset screenshots
2. join diagram and join configuration screenshot
3. data type correction and calculated-field screenshots
4. one-click filter and cross-sheet navigation screenshots
5. 3-5 visible dashboard annotations
6. ten verification-log questions answered by live Q

## Portfolio Statement
This project is presented as a professional business intelligence and AI case study for NovaTech Solutions, using the actual starter data provided by the project materials.
