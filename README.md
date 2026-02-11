# LatAm Pulse: Project Context & Standards

## Project Overview
Automated growth engine for WMG Latin America to reduce time-to-insight from 5 days to <24 hours. Focuses on the "LA7" markets (Brazil, Mexico, Argentina, Chile, Colombia, Peru, Ecuador).

## Technical Constraints
- **Cloud:** Google Cloud Platform (BigQuery)
- **Project ID:** `driiiportfolio`
- **Python:** Version 3.11+ (Optimized for Google Colab)
- **SQL Dialect:** Google Standard SQL
- **AI Tools:** Optimized for Claude Code, Cursor, and MCP-enabled agents.

## Business Logic & KPIs
- **Growth Score Formula:** $$Growth Score = (Streaming Velocity \times 0.4) + (TikTok Sentiment \times 0.3) + (Repeat Listener Rate \times 0.3)$$
- **FX Normalization:** All revenue must be converted to USD using live rates from `driiiportfolio.dim_currency_rates`.
- **Fraud Detection:** Flag any streaming spike where Z-score > 3.0.

## Coding Standards
- **Naming:** Snake_case for Python, lower_snake_case for SQL.
- **Documentation:** Every script must include an 'Executive Impact' header.
- **Logic Placement:** Push transformations upstream to BigQuery (Views) whenever possible to avoid Looker Studio latency.
