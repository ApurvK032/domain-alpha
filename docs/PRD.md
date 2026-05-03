# Product Requirements Document: Domain Investment Screener MVP

## 1. Overview

Domain Investment Screener helps users evaluate domain-name investment candidates with a simple, explainable scoring model. The MVP should make it faster to compare many possible domains and identify a smaller shortlist worth researching manually.

## 2. Target Users

- Individual domain investors
- Builders looking for brandable domain ideas
- Analysts researching domain-market opportunities
- Beginners who need a structured way to avoid poor purchases

## 3. Goals

- Score 500-1,000 domain candidates in one run.
- Rank candidates by expected investment quality.
- Label each domain as `buy`, `watch`, or `avoid`.
- Explain the main reasons behind each score.
- Include cost, renewal, and trademark-risk penalties.
- Produce a shortlist of the top 20-50 domains for manual review.

## 4. Non-Goals

- Guarantee profitable resale outcomes.
- Replace legal trademark review.
- Automatically purchase domains.
- Build machine learning in the first version.
- Build a marketplace or resale workflow.

## 5. MVP Inputs

The MVP should support a structured CSV or spreadsheet input with fields such as:

- `domain`
- `tld`
- `available`
- `registration_price`
- `renewal_price`
- `keyword`
- `keyword_demand_score`
- `trend_score`
- `comparable_sales_score`
- `brandability_score`
- `trademark_risk`
- `notes`

## 6. MVP Outputs

For each domain, the screener should output:

- `domain`
- `domain_score`
- `suggested_action`
- `estimated_resale_low`
- `estimated_resale_high`
- `top_positive_factors`
- `top_negative_factors`
- `review_notes`

## 7. Core Requirements

### Candidate Scoring

The system must calculate a weighted domain score using demand, comparable sales, brandability, TLD quality, registration cost, renewal cost, and trademark-risk factors.

### Action Labels

The system must map scores to simple actions:

- `buy` for strong candidates with acceptable risk
- `watch` for mixed candidates needing more evidence
- `avoid` for weak, expensive, or legally risky candidates

### Explainability

The system must include short explanations so users understand why each domain received its score and action label.

### Batch Ranking

The system must sort all candidates by score and highlight the top shortlist.

### Risk Handling

The system must penalize domains with high renewal costs, unclear demand, weak TLDs, or trademark-risk notes.

## 8. User Flow

1. User prepares a CSV of domain candidates.
2. User runs the screener.
3. Screener validates required fields.
4. Screener calculates component scores and penalties.
5. Screener exports a ranked result file.
6. User manually reviews the top shortlist before buying anything.

## 9. Success Metrics

- User can evaluate at least 500 candidates in a single run.
- Output includes a ranked shortlist of 20-50 candidates.
- Each result includes an action label and explanation.
- User can identify and avoid obviously bad purchases before registration.

## 10. Key Risks

- Historical domain-sales data can be incomplete or biased.
- Keyword demand does not guarantee resale demand.
- Trademark risk can be difficult to detect automatically.
- Renewal fees may reduce expected value over time.
- TLD promotions can hide expensive long-term costs.

## 11. Open Questions

- Which data source should be used first for comparable domain sales?
- Should TLD weights be hardcoded or configurable?
- What score thresholds should map to `buy`, `watch`, and `avoid`?
- How should trademark risk be represented in the first CSV schema?
- Should the MVP be a spreadsheet template, a Python CLI, or both?
