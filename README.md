# S&P 500 Financial Analytics — Power BI

A research-style financial analytics portfolio project combining **Power BI, DAX, Power Query, Python, SQL, and reproducible data modeling** to study market performance, sector trends, volatility, and company-level behavior.

## Project Objective
Build an end-to-end financial analytics solution that moves from public market data to a documented semantic model and interactive decision-support dashboard.

## Dashboard Design
The report is designed around three pages:

1. **Executive Overview** — latest close, daily return, period return, average volume, market trend, and sector comparison.
2. **Sector Analysis** — sector ranking, company comparison, and sector trend analysis.
3. **Company Drill-Down** — company-specific price history, return KPIs, high/low values, and trading-volume detail.

## Data Model
- `Companies` — company/ticker/sector lookup table.
- `Price History` — daily OHLCV market observations.
- Relationship: `Companies[Ticker]` **1 → *** `Price History[Ticker]`.
- Import-mode semantic model with reusable DAX measures.

## Core DAX Measures
- Latest Close
- Previous Close
- Daily Return %
- Start Period Close
- Period Return %
- Average Close
- Average Volume
- Max Close
- Min Close

## Live Data Connection
The Power BI project source includes a **Power Query M web-data pipeline** for public daily market data. A separate Python/yfinance pipeline is also included for reproducible offline dataset generation.

> Public market data can change and third-party endpoints can occasionally be unavailable. The repository therefore also includes a demo-data workflow for dashboard prototyping. Demo data must never be presented as real market performance.

## Repository Structure
```text
powerbi-project/     PBIP/TMDL source for the Power BI model
powerbi/             Power Query, DAX, theme, and build resources
dashboard/           location for exported/saved PBIX file
python/              market-data preparation and quantitative analysis
sql/                 analytical SQL examples
data/                public/demo datasets and documentation
images/              dashboard screenshots
documentation/       methodology, data dictionary, and model notes
```

## Research / Analytical Questions
- Which sectors outperform over a selected period?
- How do company returns and volatility differ across sectors?
- Which securities experience the largest drawdowns?
- How sensitive are rankings to the selected time window?
- Can a transparent BI model provide reproducible financial decision support?

## Technology
`Power BI` `DAX` `Power Query` `Python` `Pandas` `SQL` `Excel` `Git`

## Reproducibility
The project documents data sources, transformations, measures, assumptions, and limitations so another analyst can reproduce the model rather than relying only on dashboard screenshots.

## Status
🚀 **Active development.** The semantic-model source, Power Query connection logic, DAX measures, theme, Python pipeline, SQL examples, and dashboard specification are included. Final dashboard screenshots and the Desktop-saved `.pbix` are added after opening the project in Power BI Desktop and validating refresh/rendering.

## Author
**Lokesh Kancharla**  
M.S. Computer Science — University of Memphis  
Financial & Data Analytics | AI/ML Research Interests
