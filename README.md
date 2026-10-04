# AI Malaysian Stock Investment Research System

A reusable AI-powered investment research system focused on companies listed on Bursa Malaysia. The project is being built in stages, starting with a clear research structure and documented workflow before adding analytical frameworks and automation.

## Mission

Support consistent, evidence-based investment research by bringing market context, company analysis, reconstructed financial statements, valuation, scoring, and risk review into one repeatable process.

## Architecture

- `data/market/` — market prices, trading data, and market context.
- `data/financials/` — source financial statements and reconstructed company data.
- `data/macro/` — Malaysian and relevant global economic indicators.
- `data/ingestion/` — V1.8 ingestion records and validation.
- `research/company/` — company profiles, analysis modules, and reports.
- `research/evidence/` — V1.7 evidence records and V1.8 source capture.
- `research/automation/` — V1.9 company research engine and schemas.
- `research/industry/` — industry structure, peers, competition, and sector trends.
- `research/macro/` — macroeconomic analysis and implications.
- `valuation/` — V1.4 valuation methods, assumptions, and scenarios.
- `scoring/` — V1.2 investment quality and V1.3 AI moat scoring frameworks.
- `decision/` — V1.5 investment decision, risk, catalyst and scenario frameworks.
- `portfolio/` — V2.0 portfolio decisions, V2.1 standard stock report and V2.2 allocation engine.
- `reports/` — completed company, portfolio, evidence and allocation reports.
- `prompts/` — reusable prompts for research and portfolio allocation.
- `automation/` — workflow orchestration, including V2.2 portfolio allocation monitoring.
- `PROJECT_STATUS.md` — project version, status, mission, workflow and milestones.

### V2.2 Portfolio Files

```text
portfolio/v2_2_allocation_spec.md
portfolio/allocation_rules.md
portfolio/capital_allocation_schema.md
prompts/portfolio_allocation.md
reports/v2_2_allocation_report_template.md
automation/v2_2_allocation_workflow.md
```

## Research Workflow

1. Market and macro analysis
2. Company research
3. Financial statement reconstruction
4. Earnings quality analysis
5. Cash flow analysis
6. Competitive moat analysis
7. AI moat analysis
8. Valuation
9. Bull / Base / Bear scenarios
10. 100-point investment scoring
11. Risk and catalyst analysis
12. Investment research report

## V2.2 Portfolio Allocation Engine

### Purpose
V2.2 extends the V1.2–V2.1 research and portfolio decision system with portfolio-level opportunity ranking, position headroom, concentration checks and a cash-aware allocation budget. It is a decision-support framework only and does not execute trades.

### Inputs
Portfolio holdings, ticker, shares, average cost, dated current price/value/weight, available cash and NAV; V1.2 Fundamental Quality Score; V1.3 AI Moat; V1.4 valuation and margin of safety; V1.5 decision, risks, catalysts and confidence; V2.0 Portfolio Decision; V2.1 stock report; horizon, exposures and configurable limits/reserve.

### Capital Allocation Score
The 0–100 score uses configurable weights defaulting to Fundamental Quality 20, Earnings/Cash Flow Quality 15, AI Moat 10, Valuation/MOS 20, Risk 10, Portfolio Fit 15, Catalysts 5 and Data Confidence 5. These total 100. Existing V1.2–V2.1 methods are reused rather than recreated; missing components remain N/A with coverage reported.

### Position sizing
V2.2 ranks only candidates that pass upstream, valuation, risk and data gates. Suggested amounts are bounded by target-weight headroom, maximum position/portfolio limits and deployable cash. Cost basis is informational; a falling price alone never justifies an addition.

### Concentration control
The engine checks issuer, sector, bank, REIT, AI/data-centre and correlated exposure using verified portfolio/look-through data. Default caps are configurable starting policy values, not universal recommendations; additions stop when a configured cap is reached.

### Cash reserve
Default minimum cash reserve is 10% of portfolio NAV and is configurable. Allocation budgets cannot exceed available deployable cash or breach the reserve after proposed allocations.

### Entry price logic
Preferred entry zones must come from V1.4 valuation/MOS outputs and the company's required margin of safety. If a defensible range is unavailable, show N/A; V2.2 does not invent prices.

### Relationship with V1.2–V2.1
V2.2 consumes V1.2 Fundamental Quality, V1.3 AI Moat, V1.4 Valuation, V1.5 Investment Decision, V2.0 Portfolio Decision and the V2.1 stock report. It adds portfolio-fit and capital-budget rules without changing or duplicating their methodologies. V1.7 evidence and V1.8 source/period controls continue to apply.

### No automatic trade execution
The engine produces rankings, suggested allocation budgets, reasons and risks for human review. It never places, routes or executes trades.

## Disclaimer

This project provides research tools and informational analysis only. It is not financial, investment, legal, or tax advice, and it is not a recommendation to buy, sell, or hold any security. Investment decisions involve risk, including the possible loss of capital. Verify source data and assumptions independently and consult a qualified professional where appropriate.
