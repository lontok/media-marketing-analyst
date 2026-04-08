# Project Proposal: media-marketing-analyst

**Student:** Greg Lontok
**Course:** ISBA 4715 — Analytics Engineering
**Date:** April 13, 2026
**Repo:** https://github.com/lontok/media-marketing-analyst

## Target job posting

**Analyst, Marketing Analytics — Paramount+** (West Hollywood, CA / New York, NY)
Full posting saved at `docs/job-posting.pdf`.

The role sits on the Paramount+ Marketing Analytics team and primarily supports media mix modeling (MMM) and media optimization across paid acquisition channels. Core responsibilities include analyzing attribution and MMM outputs to quantify return on marketing investment, strengthening data pipelines for modeling inputs, maintaining reporting for marketing teams, and translating model outputs into activation strategies. Required skills include SQL proficiency, experience extracting and transforming data in databases, media measurement coursework, analytical tooling (Python, Tableau, Excel), and foundational predictive modeling concepts.

## Reflection: why this posting fits the class

This posting is a direct match for the course because it centers on SQL proficiency, warehouse data pipeline work, dashboard development, and translating analytical outputs into business insight — the exact stack we built through the dbt, Snowflake, and Streamlit lessons. The Paramount+ Analyst role requires extracting and transforming data inside a warehouse, collaborating with engineering on pipeline health, and building reporting for marketing stakeholders, all of which map cleanly onto the capstone's raw → staging → mart → dashboard flow. Building a media-mix-style project lets me practice the specific analytical lens the role demands (channel ROI, attribution, diagnostic "why did it happen" analysis) while the knowledge base gives me a way to internalize streaming industry context and MMM methodology I can speak to fluently in an interview.

## Project framing

An end-to-end pipeline that simulates how a marketing analyst at a streaming service would measure cross-channel media performance for Paramount+. Structured data flows from marketing-signal APIs into Snowflake, is transformed through dbt into a star schema, and surfaces in a Streamlit dashboard answering channel-performance and demand questions. A parallel knowledge base, built from scraped streaming industry coverage and MMM methodology sources, gives me interview-ready context on both Paramount+ and the analytical techniques the job calls out.

## Tentative data sources (finalized in Milestone 01)

- **API (structured path):** Google Trends via `pytrends` for streaming brand and title search demand, combined with the TMDB API for content popularity and release metadata. Together these act as a proxy for marketing-driven demand lift across titles and competitors, enabling MMM-style channel and demand analysis.
- **Web scrape (knowledge base path):** A hybrid set of sources — Paramount+ press releases and Variety / Deadline / Hollywood Reporter streaming coverage for company and industry context, plus Think with Google, Meta marketing science, and Nielsen methodology articles for MMM and attribution foundations. Target of at least 15 sources across 3+ distinct sites.

## Transferability

This project is designed to transfer beyond the Paramount+ posting. With minor adjustments to the source APIs or dashboard framing, the same repo supports applications to:

1. **BI / marketing analyst roles at other streaming services** (Netflix, Max, Disney+) — swap title metadata, keep the channel performance and demand modeling lens.
2. **Analytics engineer roles in consumer media or entertainment** — the dbt star schema, pipeline automation, and dashboard work stand on their own as evidence of warehouse modeling skill.
3. **Marketing analyst roles in any subscription / DTC business** — the MMM framing (channel ROI, attribution, diagnostic analysis) generalizes to any company spending on paid acquisition.
