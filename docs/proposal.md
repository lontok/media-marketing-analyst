# Project Proposal

**Name:** Greg Lontok

**Project Name:** media-marketing-analyst

**GitHub Repo:** https://github.com/lontok/media-marketing-analyst

## Job Posting

- **Role:** Analyst, Marketing Analytics
- **Company:** Paramount+ (Paramount Streaming)
- **Link:** https://www.indeed.com/ (posting saved at `docs/job-posting.pdf`)

**SQL requirement (quote the posting):** "Proficient in SQL with a solid comprehension of data infrastructure; experience extracting, cleaning, and transforming data within databases."

## Reflection

This posting is a direct match for the course because the Paramount+ Marketing Analytics Analyst role centers on SQL proficiency, warehouse data pipeline work, and translating analytical outputs into business insight for marketing stakeholders — the exact workflow we built through the dbt, Snowflake, and Streamlit lessons. It explicitly requires extracting, cleaning, and transforming data in databases, foundational predictive modeling concepts, and dashboard development, which map cleanly onto the capstone's raw → staging → mart → dashboard flow and the diagnostic analytics lens we practiced in class. To prove I can do this work I'll build an end-to-end pipeline that simulates media mix analysis for a streaming service: pulling marketing demand signal data from the Google Trends and TMDB APIs into Snowflake, transforming it through a dbt star schema, and surfacing channel-performance and ROI insights in a Streamlit dashboard, alongside a Claude Code knowledge base synthesized from Paramount+ press coverage and MMM methodology sources. The same project transfers cleanly to BI or marketing analyst roles at other streaming services like Netflix, Max, or Disney+ by swapping title metadata, to analytics engineer openings in consumer media where the dbt modeling and pipeline automation stand on their own, and to marketing analyst roles at any subscription or DTC business where channel ROI and attribution framing generalize directly.
