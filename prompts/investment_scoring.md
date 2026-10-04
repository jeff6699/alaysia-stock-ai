# Prompt: Apply Investment Scorecard V1

## Role and goal
Score a Bursa Malaysia listed company with the repository’s 100-point V1 framework. Use only supplied or verified source data; never fabricate values, citations, peer comparisons or forecasts. The result supports research and is not an automatic buy/sell recommendation.

## Required inputs
- Company name, Bursa ticker and sector: [Provide]
- Analysis date and dated share price/source: [Provide]
- Latest and comparable financial statements/filings: [Provide]
- At least 3–5 comparable years for growth/FCF when available: [Provide]
- Sector peer group and source/date: [Provide or explain unavailable]
- Market price/volume history and benchmark: [Provide]
- Intended trade size for liquidity score: [Provide]
- Industry outlook evidence: [Provide]
If inputs are absent, do not guess. Mark affected metric N/A and explain lost points/coverage.

## Fixed weights
A. Financial Quality (50): Revenue Growth 10; EPS Growth 10; ROE 10; Debt-to-Equity 10; Free Cash Flow 10.
B. Profitability & Valuation (15): Gross Margin 10; P/E 5.
C. Balance Sheet / Valuation (10): P/B 5; Dividend Yield 5.
D. Market / Technical (15): Price Trend 5; Trading Volume 5; RSI 5.
E. Business Quality (10): Industry Growth 5; Competitive Moat 5.
Total maximum = 100. Do not change weights. Follow scoring/scoring_rules.md for formulas, exact bands, warnings and sector rules; score_interpretation.md for grade and coverage.

## Per-metric output
For each of the 14 metrics provide:
- FACT: raw value, unit, period/date, formula, source/page/note/URL, data quality.
- ANALYSIS: score/max points, exact rule/band, rationale, peer/sector context and warnings.
- INFERENCE: what the metric may imply and uncertainty.
- FORECAST: only if forecast inputs are used; state horizon and assumptions, or say no forecast.

Use N/A only for missing, invalid or inapplicable data, not for valid weak performance. N/A does not earn points and removes that metric weight from Available Points. Coverage = Available Points / 100. Report TOTAL SCORE as earned / 100 if complete, otherwise earned / available and coverage. Optional normalized score = earned / available × 100 only at ≥80% coverage; mark provisional and show raw score. A partial-coverage case does not receive a standard grade. Below 80%, withhold a grade.

## Required report
Company:
Ticker:
Sector:
Analysis Date:

Financial Quality:
Revenue Growth:
EPS Growth:
ROE:
Debt-to-Equity:
Free Cash Flow:

Profitability & Valuation:
Gross Margin:
P/E:
P/B:
Dividend Yield:

Market:
Price Trend:
Volume:
RSI:

Business Quality:
Industry Growth:
Moat:

TOTAL SCORE:
Coverage:
Investment Grade:
Confidence:
High-Risk Flags:

Key Strengths:
Key Weaknesses:
Major Risks:
Potential Catalysts:
Data Gaps:

Investment View:
Bull Case:
Base Case:
Bear Case:

For the report, separate FACT, ANALYSIS, INFERENCE and FORECAST. Cite sources; do not merge forecasts into reported results. State data unavailable explicitly. Include score version, dated price, peer references, uncertainty and limitations. Explain why any high-risk flag applies. Conclude that the score is decision support, not an automatic buy/sell recommendation.
