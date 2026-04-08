# media-marketing-analyst — Project Context

## What this project is

An end-to-end analytics engineering capstone built against a real job posting: **Analyst, Marketing Analytics at Paramount+** (`docs/job-posting.pdf`). The project simulates how a marketing analyst at a streaming service would measure media mix performance, channel ROI, and demand signal — pulling data through a pipeline that mirrors the stack the role requires (SQL, warehouse modeling, dashboards, pipelines).

This is a portfolio asset, not a one-job artifact. It should transfer to similar roles: marketing analyst, BI analyst, analytics engineer, data analyst in media/streaming/entertainment.

## Target role skills this project demonstrates

From the Paramount+ posting:

- SQL proficiency and warehouse data modeling (dbt + Snowflake star schema)
- Extracting, cleaning, transforming data within databases
- Marketing measurement concepts (attribution, media mix, ROAS, channel performance)
- Dashboard development for marketing stakeholders (Streamlit)
- Translating analytical outputs into actionable recommendations
- Pipeline reliability and automation (GitHub Actions)
- Familiarity with GitHub for logic development and collaboration

## Architecture (planned)

```
Structured path:   API (pytrends + TMDB) -> GitHub Actions -> Snowflake raw
                   -> dbt staging -> dbt mart (star schema) -> Streamlit dashboard

Knowledge path:    Web scrape (Paramount+ press, Variety/Deadline, MMM methodology)
                   -> GitHub Actions -> knowledge/raw -> Claude Code -> knowledge/wiki
```

## Directory layout

- `docs/` — proposal, job posting, pipeline diagram, ERD, resume, slides
- `pipelines/` — Python extract/load scripts for each source
- `dbt/` — dbt project (staging + mart models, tests)
- `dashboard/` — Streamlit app
- `knowledge/raw/` — scraped source files (at least 15 sources from 3+ sites by M02)
- `knowledge/wiki/` — Claude Code-synthesized wiki pages
- `knowledge/index.md` — wiki table of contents
- `.github/workflows/` — scheduled GitHub Actions

## How to query the knowledge base

When asked a question about Paramount+, streaming industry context, or MMM methodology:

1. Start with `knowledge/index.md` to orient.
2. Read relevant wiki pages in `knowledge/wiki/` — these are the synthesized answer layer.
3. If the wiki doesn't cover it, search `knowledge/raw/` for primary sources and cite them.
4. Always cite which source file(s) an answer came from.

## Working conventions

- Python via a virtual environment (`.venv/`). Never commit `.venv/`.
- Secrets (Snowflake credentials, API keys) live in `.env`, never committed. See `.env.example` for required keys once they exist.
- Prefer meaningful, frequent commits over batch commits.
- No Claude Code attribution lines in commit messages.
- Update this file as the project evolves so future sessions have accurate context.
