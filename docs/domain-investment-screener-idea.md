# Domain Investment Screener

## Simple Project Idea
Build a tool that helps find domain names worth considering as small investments. The tool should collect domain candidates, check whether they are available, estimate resale potential, and rank them as `buy`, `watch`, or `avoid`.

## Problem
People buy cheap domains hoping to resell them later, but most domain purchases are based on guessing. A simple data-driven screener could help compare many possible domains and focus only on names with better demand, lower cost, and lower legal risk.

## Core Concept
The project should score each domain using:

- current purchase price and renewal cost
- similar historical domain sales
- keyword demand and trend growth
- brandability and memorability
- TLD quality, such as `.com`, `.ai`, `.io`, `.app`, or `.co`
- trademark and cybersquatting risk
- expected resale value after marketplace fees and holding costs

## First Version
Start with a simple spreadsheet or Python script.

Inputs:
- list of domain ideas
- availability and registration price
- keyword/search trend data
- historical comparable sales
- trademark-risk notes

Output:
- ranked domain list
- suggested action: `buy`, `watch`, or `avoid`
- rough resale range
- short explanation for each score

## Basic Scoring Formula
Use a simple weighted score first:

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

Machine learning can come later after enough data is collected.

## Skills Needed
- data collection and cleaning
- Python, pandas, and SQL
- statistics and expected value thinking
- basic supervised machine learning later
- NLP/text analysis for domain quality
- domain market research
- trademark and legal-risk awareness

Reinforcement learning is not needed for the first version because domain resale feedback is slow and sparse.

## Possible Data Sources
- historical domain sales databases
- domain registrar APIs for availability and pricing
- marketplace trend pages
- Google Trends or keyword-volume tools
- trademark search databases
- domain zone files or registration datasets

## Main Risks
- Most domains never sell.
- Public sales data is incomplete and biased.
- A good-looking domain can still have trademark risk.
- Renewal fees can quietly destroy returns.
- Some TLDs have high initial discounts but expensive renewals.

## MVP Goal
Create a small screener that evaluates 500-1,000 possible domains and produces a ranked shortlist of the top 20-50 worth researching manually.

## Success Metric
The first success is not making a huge sale. The first success is avoiding bad purchases and building a repeatable process for comparing domain opportunities.
