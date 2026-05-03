# Domain Investment Screener

Domain Investment Screener is a planned tool for comparing domain-name investment ideas with a simple, repeatable scoring process. The goal is to help avoid weak purchases, surface promising domains for manual research, and make domain-investing decisions less dependent on guesswork.

## Problem

Many inexpensive domains look attractive at first glance, but most never resell. Renewal fees, weak demand, misleading comparable sales, low-quality TLDs, and trademark risk can quickly turn a cheap purchase into a bad investment.

This project aims to create a practical screener that ranks domain candidates before money is spent.

## MVP Concept

The first version should accept a list of domain ideas and return a ranked shortlist with:

- Suggested action: `buy`, `watch`, or `avoid`
- Overall score
- Rough resale range
- Short explanation for the score
- Cost and renewal-risk notes
- Trademark-risk notes for manual review

The MVP can start as a spreadsheet or Python script before adding APIs, a database, or machine learning.

## Initial Scoring Model

```text
domain_score =
  demand_score
+ comparable_sales_score
+ brandability_score
+ tld_score
- cost_penalty
- trademark_risk_penalty
- renewal_cost_penalty
```

The score should stay explainable. Each output row should make it clear why a domain was ranked highly or poorly.

## Planned Inputs

- Domain candidate list
- Availability status
- Registration price
- Renewal cost
- Keyword or trend data
- Historical comparable sales
- TLD quality
- Trademark-risk notes

## Planned Outputs

- Ranked domain list
- Top 20-50 candidate shortlist
- Suggested action for each domain
- Estimated resale range
- Explanation of major positive and negative factors

## Project Status

This repository currently contains the project idea and early product documentation. No runnable implementation exists yet.

## Suggested MVP Roadmap

1. Define a CSV input schema for domain candidates.
2. Build a Python scorer with configurable weights.
3. Add a sample dataset and expected output.
4. Export ranked results to CSV.
5. Add tests for scoring rules and action labels.
6. Add optional data enrichment from registrar and market data sources.

## Important Disclaimer

This project is for research and decision support. It should not be treated as legal, financial, or trademark advice. Domain purchases can lose money, and manual review is required before buying any domain.
