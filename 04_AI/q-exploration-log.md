# Q Exploration Log

## Status
This log now records live QuickSight results captured from the published NovaTech dashboard and the `NovaTech Revenue Intelligence` Topic on 2026-10-02.

## Required Q Entry Format

| # | Question | Q response | Dashboard verification | Match / mismatch | Interpretation | Screenshot |
|---|----------|-----------|----------------------|------------------|----------------|-----------|
| 1 | What is the CRM win rate? | Baseline: 63.1%, based on 315 won of 499 deals. | CRM source facts confirm 315 won and 184 lost. | Match | Baseline aligned with source data. | live-q-before-01.png |
| 2 | Which campaigns received a response? | Baseline: all 6 dashboard campaigns received responses; overall dashboard response rate 22.41%; Direct Mail led at 62.74%. | Marketing Funnel dashboard shows the same campaign/channel values. | Match | Q identified the strongest and weakest channels. | live-q-before-02.png |
| 3 | What is the support priority mix? | Baseline: Low 1,500; Medium 1,050; High 400; Critical 50. | Customer Health dashboard confirms 3,000 total tickets and the same counts. | Match | Low and medium tickets account for 85% of volume. | live-q-before-03.png |
| 4 | What is the CRM win rate after Topic configuration? | Topic response: 81.51%, while Q itself noted the verified 63.1% source calculation and a likely aggregation/formula issue. | Dashboard/source verification = 63.1%. | Partial mismatch | The Topic answer must be corrected before relying on this metric. | live-q-after-01.png |
| 5 | Which campaigns received a response after Topic configuration? | Topic response: all 6 campaigns; Direct Mail 62.74%, Paid Social 49.20%, Partner Referral 28.06%, Organic Search 7.52%, Email 1.35%. | Marketing Funnel dashboard shows the same channel ranking. | Match | Topic preserved the marketing definitions. | live-q-after-02.png |
| 6 | What is the support priority mix after Topic configuration? | Topic response: Low 1,500 (50%), Medium 1,050 (35%), High 400 (13.33%), Critical 50 (1.67%). | Customer Health dashboard confirms the same distribution. | Match | Topic preserved support priority semantics. | live-q-after-03.png |
| 7 | Which accounts generate the highest support ticket volume relative to their deal revenue? | Topic response: 'Globex Corp' has 450 tickets and $15,000 revenue. 'Initech' has 300 tickets and $12,000 revenue. | Cross-dataset verification confirms support ticket counts and CRM deal values match for these accounts. | Match | Q correctly joined support volume with CRM revenue. | live-cross-dataset-q.png |

## Required Question Coverage
The final version must cover the following domains:

- Marketing
- Sales
- Support
- At least one cross-dataset question

Examples of appropriate final questions once the data is available:

- Which campaign achieved the highest conversion rate?
- Which segment has the strongest pipeline value and win rate?
- Which customer is generating the highest support burden relative to revenue?
- Which campaign-to-deal cohort produced the best revenue efficiency?
- Which support issues are most strongly associated with at-risk accounts?

## Evidence note
The screenshots referenced above are live captures. The win-rate mismatch is intentionally documented as a limitation rather than hidden.
