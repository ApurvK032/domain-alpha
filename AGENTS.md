# Project Guide

## Project Purpose
Domain Investment Screener is a planned tool for evaluating domain-name investment ideas with a repeatable scoring process. The first version should help rank domain candidates as `buy`, `watch`, or `avoid` based on demand, comparable sales, brandability, TLD quality, cost, renewal burden, and trademark risk.

## Tech Stack
- Current state: documentation plus clean Python-oriented project scaffold.
- Planned MVP stack: Python 3.11+, pandas, CSV/spreadsheet inputs, and simple CLI output.
- Later stack candidates: SQL database, registrar APIs, historical sales datasets, keyword/trend APIs, and basic ML after enough labeled outcomes exist.

## Setup, Run, and Test Commands
- No runnable screener command exists yet.
- Useful current commands:
  - `git status --short --branch`
  - `Get-Content README.md`
  - `Get-Content docs/PRD.md`
  - `Get-Content docs/WORKFLOW.md`
- Planned Python setup once implementation begins:
  - `python -m pip install -e .[dev]`
  - `python -m pytest`
  - `python -m ruff check .`

## Important Files
- `docs/domain-investment-screener-idea.md` - original project idea and scoring concept.
- `docs/PRD.md` - simple product requirements document for the MVP.
- `docs/WORKFLOW.md` - intended domain-screening workflow and project hygiene rules.
- `data/samples/domain-candidates.sample.csv` - safe sample input schema.
- `src/domain_screener/` - future Python package for reusable screener code.
- `tests/` - future automated tests.
- `outputs/` - generated ranked results and shortlists; ignored except placeholder.
- `README.md` - public-facing project overview.
- `AGENTS.md` - durable project context for future Codex sessions.
- `AGENT_LOG.md` - concise dated work log when useful.

## Coding Conventions
- Prefer small, focused changes.
- Keep documentation concise and high-signal.
- When code is added, favor clear Python modules, typed function signatures where helpful, and deterministic scoring logic with explainable outputs.
- Use structured data formats such as CSV, JSON, or SQL tables instead of ad hoc text parsing for screener data.

## Known Issues
- No implementation exists yet.
- No CLI, scoring implementation, or tests exist yet.
- Data-source integrations and trademark-risk checks are not implemented.
- Domain investing is high risk; documentation should avoid implying guaranteed resale outcomes.
- `data/raw/`, `data/processed/`, and `outputs/` should remain local/generated unless files are sanitized samples.

## Workflow Expectations
- Read this file before planning or editing.
- Update this file only when durable project knowledge changes.
- Use `AGENT_LOG.md` for important session history, not as a long diary.
- Run relevant checks once code exists, and clearly say when checks cannot be run.
