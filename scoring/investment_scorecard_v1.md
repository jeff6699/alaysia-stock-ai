# Investment Scorecard V1 — 100 Points

## Purpose
A standardized, evidence-led decision-support score for Bursa Malaysia listed companies. It combines financial quality, valuation, market/technical condition, industry growth, and competitive moat. It is not an automatic buy/sell recommendation or a substitute for full research.

## Weight allocation

| Category | Metrics | Points |
|---|---|---:|
| A. Financial Quality | Revenue Growth 10; EPS Growth 10; ROE 10; Debt-to-Equity 10; Free Cash Flow 10 | 50 |
| B. Profitability & Valuation | Gross Margin 10; P/E Valuation 5 | 15 |
| C. Balance Sheet / Valuation | P/B Valuation 5; Dividend Yield 5 | 10 |
| D. Market / Technical | Price Trend 5; Trading Volume 5; RSI 5 | 15 |
| E. Business Quality | Industry Growth 5; Competitive Moat 5 | 10 |
| TOTAL | 14 metrics | 100 |

Metric thresholds, formulas, interpretation, warnings and data rules are defined in scoring_rules.md. Apply one score version consistently; do not silently change weights or thresholds.

## Scoring protocol
1. Freeze analysis date, price date, issuer/Bursa code, reporting periods, sector, peer group, currency, units, source set and score version.
2. Prefer current Bursa filings and issuer reports for financial inputs. Record filing date, page/note, audited/reviewed/unaudited status, consolidated/parent basis and restatements.
3. Use like-for-like periods, normally a 3–5 year history for growth and cash-flow consistency. Document exceptions and sector-specific definitions.
4. For each metric, retain raw value, formula, periods, source, score awarded, max points, rationale, warning and data quality. Preserve decimals only if source precision justifies them.
5. Separate FACT, ANALYSIS, INFERENCE and FORECAST. A metric based on forecast inputs must be labeled FORECAST, with horizon and assumptions. No fabricated data.
6. Assign N/A only when data are unavailable, not meaningful, or inapplicable under the documented sector rules. Explain the missing input and its effect.
7. Use the scoring-rules rubric and sector context. Peer-relative scoring requires a named, comparable peer set and date; otherwise mark that comparison unavailable.

## Missing-data arithmetic
- A scored metric contributes its awarded points to Earned Points and its full weight to Available Points. N/A contributes neither; never silently assign zero.
- Coverage = Available Points / 100 × 100%.
- Report TOTAL SCORE as “Earned Points / 100” when fully scored, otherwise “Earned Points / Available Points (Coverage: x%)”.
- Optional comparable score = Earned Points / Available Points × 100. Show only when coverage is at least 80%, label it “coverage-normalized, provisional”, and show the unnormalized total beside it. Do not hide missing data with normalization.
- Assign the standard Investment Grade only for 100% coverage. With partial coverage, report “Provisional — insufficient coverage for a standard grade”; optionally state the provisional band of the normalized score if coverage is at least 80%. Below 80%, withhold the band.
- Do not count a zero as N/A. A metric with valid data but poor performance scores zero and remains in Available Points.
- If any high-risk override in score_interpretation.md applies, show it prominently beside the numeric score; it does not alter the arithmetic unless a rubric explicitly specifies a cap.

## Evidence labels
- FACT: value, period, unit, formula, source and source locator.
- ANALYSIS: comparison, score mapping, rationale, peer/sector context and caveats.
- INFERENCE: what the score may suggest, with uncertainty and counter-evidence.
- FORECAST: only explicit forward assumptions/scenarios; do not relabel forecasts as facts.

## Bursa Malaysia and sector adaptation
Use the latest comparable Bursa filings and note whether financials are audited, reviewed or unaudited. Confirm current corporate actions, share count and PN/GN status from current primary announcements when relevant. Use RM/sen consistently.
Peer-adjust margins, leverage, valuation, growth, yields and industry outlook for business model only where a defensible comparable cohort is available. Banks/insurers, REITs, developers, contractors, plantations and commodity cyclicals may require sector-specific definitions. Where the supplied metric is not meaningful (for example, industrial free cash flow for a bank), mark it N/A, explain the limitation and reduce coverage; do not substitute an unapproved metric or change the 100-point weights silently. A future version may publish a named sector variant with its own version and mapping.

## Output record
Use research/company/scorecard_report_template.md. Keep raw metric inputs and formulas so that future automation can read them. A machine-readable implementation should store metric_id, value, unit, period, source, method, score, max_points, status (scored/N_A), rationale, warning, and quality_flag without changing the human-readable audit trail.
