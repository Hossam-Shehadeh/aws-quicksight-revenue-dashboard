# AI vs Dashboard Evaluation

## Status
This comparison uses live QuickSight responses captured on 2026-10-02.

## Comparison Table Format

| Question | AI Answer | Dashboard Answer | Match | Explanation |
|----------|-----------|------------------|-------|-------------|
| What is the CRM win rate? | Baseline Q: 63.1%; Topic Q: 81.51%, with Q noting the 63.1% source calculation. | 315 won / 499 total = 63.1% | Partially consistent | Topic response appears affected by a calculated-field or aggregation issue; correct the metric before final use. |
| Which campaigns received a response? | Q identified all six campaigns and ranked channels: Direct Mail 62.74%, Paid Social 49.20%, Partner Referral 28.06%, Organic Search 7.52%, Email 1.35%. | Marketing Funnel shows the same ranking and 22.41% dashboard rate. | Substantially consistent | Campaign/channel interpretation agreed with the dashboard. |
| What is the support priority mix? | Low 1,500; Medium 1,050; High 400; Critical 50. | Customer Health shows the same counts and percentages. | Exact match | Support semantics and totals agreed. |

## Classification Guidance
Use the classification labels exactly as required by the rubric:

- Exact match
- Substantially consistent
- Partially consistent
- Inconsistent

## Evaluation Principles
- The business team should compare Q output to actual dashboard calculations.
- Differences may occur because Q paraphrases, uses approximate logic, or interprets business terms more loosely than a metric card.
- Any mismatch must be documented honestly.
- The purpose of this evaluation is not to force perfect agreement, but to validate responsible AI use.

## Evidence
Live screenshots are stored in the submission evidence folder with `live-q-before-*` and `live-q-after-*` names.
