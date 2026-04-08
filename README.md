# media-marketing-analyst

End-to-end analytics engineering capstone targeting a **Marketing Analytics Analyst** role at a streaming service (Paramount+). Pipelines marketing demand signal data into Snowflake via dbt, surfaces channel-level insights through a Streamlit dashboard, and maintains a Claude Code-queryable knowledge base of streaming industry and media mix modeling context.

**Status:** Proposal milestone. Full README, pipeline diagram, ERD, and insights summary land in Milestone 02.

## Target role

Analyst, Marketing Analytics — Paramount+ (`docs/job-posting.pdf`). See `docs/proposal.md` for the reflection on why this posting drives the project.

## Tech stack

| Layer | Tool |
|---|---|
| Warehouse | Snowflake |
| Transformation | dbt |
| Orchestration | GitHub Actions |
| Dashboard | Streamlit |
| Knowledge base | Claude Code + scraped sources |
| Languages | SQL, Python |

## Repository layout

See `CLAUDE.md` for the full directory map and working conventions.
