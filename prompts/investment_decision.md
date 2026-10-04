# Prompt: Integrated Investment Decision V1.5

You are preparing an evidence-led decision-support report for a Bursa Malaysia listed company using the repository's existing V1.2, V1.3, V1.4 frameworks and V1.5 decision modules.

## Required discipline
- Do not modify or recreate the upstream V1.2 score rules, V1.3 moat rules, or V1.4 valuation formulas.
- Use the actual dated upstream outputs. If absent or invalid, write N/A and explain impact; never fabricate company data, prices, filings, source citations, scores, risks, catalyst evidence, or probabilities.
- Keep FACT, ANALYSIS, ASSUMPTION, INFERENCE and FORECAST separate. Label every analyst-selected scenario or probability as ASSUMPTION.
- Use primary Bursa Malaysia and issuer sources where available. Give source/date/locator. Mark unverified evidence.
- Calculate the five V1.5 components under decision/decision_rules.md. Show earned / available / maximum, coverage and rationale. Do not simply average inputs or use missing items as zero.
- Apply evidence-backed HIGH RISK overrides first, then data sufficiency/confidence gates, then valuation and score rules; a numerical score never cancels critical risk.
- Scenario probabilities must total exactly 100% before a final classification. Use V1.4 Bear/Base/Bull values; no revaluation outside that framework.
- Use the report template at research/company/investment_decision_report_template.md. State both the classification and why a more positive classification fails.

## Workflow
1. Freeze issuer identity, ticker, sector, analysis date, market-price date, periods, currency, units, sources and methodology versions.
2. Summarize V1.2 quality output and key strengths/weaknesses.
3. Summarize V1.3 current moat, durability, evolution, AI disruption risk/opportunity, coverage.
4. Summarize V1.4 current price, Bear/Base/Bull values, MOS, confidence and method selection. Calculate returns only with the stated V1.4-compatible formula; N/A if inputs are unusable.
5. Complete all 11 risks and the 10 catalyst categories; N/A evidence affects coverage/confidence.
6. Complete Bear/Base/Bull assumptions, values, returns, main risks, and probabilities totaling 100%.
7. Rate HIGH/MEDIUM/LOW data confidence using five factors; explain unresolved assumptions.
8. Calculate score, apply hierarchy/overrides, and write investment thesis, reasons, invalidators and five monitoring indicators.
9. Complete the source-module audit table and final review checklist.

## Required output fields
Company, ticker, sector, analysis date; Decision Score and coverage; Decision Rating; Investment Quality; AI Moat; Valuation; Risk; Catalysts; Current Price; Bear/Base/Bull Fair Value; Base Upside/Downside; Margin of Safety; Risk Rating; AI Disruption Risk; Bull/Base/Bear probabilities; Investment Thesis; Top 3 Reasons to Own; Top 3 Reasons Not to Own; What Must Go Right; Top 3 Thesis Invalidation Conditions; Key Catalysts; five Key Monitoring Indicators; Evidence Confidence; Final Decision; Decision Explanation.
