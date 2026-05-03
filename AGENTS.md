# Project Guide

## Project Purpose
Domain Investment Screener is a planned tool for evaluating domain-name investment ideas with a repeatable scoring process. The first version should help rank domain candidates as `buy`, `watch`, or `avoid` based on demand, comparable sales, brandability, TLD quality, cost, renewal burden, and trademark risk.

## Tech Stack
- Current state: documentation-only project.
- Planned MVP stack: Python, pandas, CSV/spreadsheet inputs, and simple CLI output.
- Later stack candidates: SQL database, registrar APIs, historical sales datasets, keyword/trend APIs, and basic ML after enough labeled outcomes exist.

## Setup, Run, and Test Commands
- No install, run, or test commands exist yet.
- Useful current commands:
  - `git status --short --branch`
  - `Get-Content README.md`
  - `Get-Content PRD.md`

## Important Files
- `domain-investment-screener-idea.md` - original project idea and scoring concept.
- `README.md` - public-facing project overview.
- `PRD.md` - simple product requirements document for the MVP.
- `AGENTS.md` - durable project context for future Codex sessions.
- `AGENT_LOG.md` - concise dated work log when useful.

## Coding Conventions
- Prefer small, focused changes.
- Keep documentation concise and high-signal.
- When code is added, favor clear Python modules, typed function signatures where helpful, and deterministic scoring logic with explainable outputs.
- Use structured data formats such as CSV, JSON, or SQL tables instead of ad hoc text parsing for screener data.

## Known Issues
- No implementation exists yet.
- No dependency file, tests, CLI, data schema, or sample data exists yet.
- Data-source integrations and trademark-risk checks are not implemented.
- Domain investing is high risk; documentation should avoid implying guaranteed resale outcomes.

## Workflow Expectations
- Read this file before planning or editing.
- Update this file only when durable project knowledge changes.
- Use `AGENT_LOG.md` for important session history, not as a long diary.
- Run relevant checks once code exists, and clearly say when checks cannot be run.
