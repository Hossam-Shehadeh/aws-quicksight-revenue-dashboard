# Topic Configuration Evaluation

## Status
This evaluation records the live `NovaTech Revenue Intelligence` Topic created in QuickSight. The Topic includes the four SPICE datasets and was used for the post-Topic Q captures in `NovaTech_Revenue_Intelligence_Submission/06_Evidence/live/`.

## Mock Topic vocabulary

| Business term | Intended meaning |
|---|---|
| campaign ROI | Revenue attributed compared with campaign spend |
| win rate | Won CRM deals divided by total deals |
| support burden | Ticket volume and recent ticket activity by account |
| account health | Combined sales and support view at account grain |
| response rate | Marketing responses divided by all marketing records |

## Baseline Questions
The project requires 2–3 strong baseline questions before Topic configuration. These should cover different business domains. Suggested categories include:

- Marketing performance and campaign efficiency
- Sales pipeline and deal conversion
- Support burden and customer health

Example baseline structure:

1. Which campaign generated the strongest lead-to-deal conversion?
2. Which sales segments have the highest win rate and pipeline value?
3. Which customers are creating the highest support burden relative to revenue?

## Expected Topic Role
A Topic should help Q understand the business vocabulary used by NovaTech, including:

- Revenue
- Pipeline
- Win rate
- Support burden
- Customer health
- Campaign performance
- Deal stage and status

## Before Topic
- Question: What is the CRM win rate?
- Q response: 63.1%, based on 315 won deals out of 499 total deals.
- Expected interpretation: The response should be evaluated against the actual business definitions in the source data dictionary.
- Problems/limitations: Without a Topic, Q may use generic assumptions or misinterpret business terms.
- Screenshot: evidence/ai/before-topic-questions.png (pending)

## After Topic
- Question: What is the CRM win rate?
- Q response: 81.51% from the dashboard calculation, with Q noting that the verified source calculation is closer to 63.1%.
- Expected interpretation: The response should become more semantically aligned with the NovaTech business model.
- Problems/limitations: Topic tuning must still be validated against actual dashboard math.
- Screenshot: evidence/ai/after-topic-questions.png (pending)

## Comparison Summary
The final evaluation should include an explicit before/after comparison showing:

- whether the same question produced a more accurate or more relevant answer
- whether business terms were interpreted correctly
- whether Q used the right dataset filters and definitions

## Required Final Deliverable
Once the real data is loaded, complete the following:

1. Run the baseline questions before Topic configuration.
2. Configure the Topic with field descriptions and business definitions.
3. Re-run the same questions.
4. Record the actual responses and screenshots.
5. Compare the results and document the improvement or remaining gap.

The win-rate discrepancy is a documented live limitation. Campaign and support questions matched their dashboard values. The Topic configuration screenshot and before/after Q screenshots are included in the live evidence folder.
