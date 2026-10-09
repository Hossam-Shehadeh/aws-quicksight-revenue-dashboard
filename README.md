# 📊 AWS QuickSight Revenue Intelligence Dashboard

An interactive, business-ready revenue intelligence dashboard built using Amazon QuickSight, featuring unified data models, calculated KPIs, and natural language Q&A exploration.

## 📌 Project Overview
This project involves building a centralized data strategy and BI dashboard for **NovaTech Solutions**. It unifies CRM deals, marketing campaigns, and support ticket data into a single SPICE dataset, allowing executives to analyze cross-functional metrics like customer health, campaign ROI, and sales pipeline velocity.

## 🛠️ Tech Stack & Tools
* **BI Platform:** Amazon QuickSight
* **Data Engine:** SPICE (Super-fast, Parallel, In-memory Calculation Engine)
* **AI/NLP:** Amazon Q / Quick Chat (Natural Language Data Querying)
* **Data Sources:** CRM, Marketing, and Customer Support CSVs

## 📁 Repository Structure
* `01_Verification/`: Logs proving data accuracy and expected facts against Amazon Q queries.
* `02_Data_Transformation/`: Business metrics dictionary and the data strategy plan.
* `03_Dashboard/`: The final exported Dashboard PDF demonstrating visual layouts and KPIs.
* `04_AI/`: Documentation on Amazon Q topic configuration and exploration.
* `05_Executive_Report/`: A written summary interpreting the dashboard for leadership.
* `06_Evidence/`: Live screenshots of the AWS QuickSight environment, join schemas, and data pipelines.

## 💡 Key Features Implemented
* **Unified Data Model:** Joined disparate sales, marketing, and support datasets on `account_id` using QuickSight's data prep UI.
* **Calculated Business KPIs:** Created advanced calculated fields for *Campaign ROI*, *Win Rate*, and *Critical Tickets Count*.
* **Interactive Design:** Built cross-sheet navigation and visual filter actions across three analytical sheets: Marketing Funnel, Sales Pipeline, and Customer Health.
* **AI Integration:** Configured an Amazon Q Topic to allow non-technical stakeholders to ask natural language questions (e.g., *"Show me total revenue by region"*).

---
*Created as part of the AWS & AI for Business portfolio.*
