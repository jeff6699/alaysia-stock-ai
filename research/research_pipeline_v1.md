# Automated Investment Research Pipeline V1.6

## Purpose and scope
A repeatable, modular end-to-end workflow for Malaysian listed-company research. “Automated” describes a standardized sequence and reusable prompts; this version adds no application code or external dependencies. Analysts or future automation complete each stage from dated evidence. N/A is required when evidence is unavailable.

Do not redesign the V1.2 Investment Quality Score, V1.3 AI Moat Evolution Score, V1.4 valuation, or V1.5 decision/risk/catalyst methodologies. Consume and cite their outputs. The final report is a decision-support document, not a buy/sell recommendation.

## Run controls
Before analysis, freeze issuer name and Bursa code, analysis date, price date, fiscal year and reporting period, units/currency/share basis, source set, and methodology versions. Prefer current Bursa Malaysia announcements, audited annual reports, interim financial statements, issuer presentations and official industry/regulatory data. Record source title, date, URL or document locator, page/note, filing status and retrieval date. Distinguish company claims from independently observed outcomes.

For every material conclusion, separate FACT, ANALYSIS, INFERENCE and FORECAST; use ASSUMPTION for analyst-selected inputs, especially valuation/scenario parameters. A missing fact is N/A, with its impact on coverage/confidence. Do not silently replace missing evidence with zero, a peer proxy or an invented estimate.

## Ordered workflow and stage records
Complete stages in order. Each stage writes into its matching research/company module and then into the master report. A failed data gate records the limitation and continues where useful; it cannot be bypassed to produce a confident conclusion.

| Step | Stage | Main output / source module |
|---:|---|---|
| 1 | Company identification | research/company/company_profile.md; confirm legal issuer, Bursa ticker, listing/exchange, analysis/price dates |
| 2 | Business model | company_profile.md; revenue/profit drivers, cost structure, capital intensity, cash conversion, advantages, dependencies |
| 3 | Industry analysis | company_profile.md; market, cycle, growth, pricing, regulation, technology/AI, demand, tailwinds/headwinds |
| 4 | Competitive landscape | company_profile.md; sourced peers, position, customer/supplier concentration, competition |
| 5 | Financial statement analysis | research/company/financial_analysis.md and V1.1 financial statement framework; preferably five comparable years and latest interim period |
| 6 | Earnings quality | financial_analysis.md and research/company/earnings_quality_framework.md; reconcile reported performance and identify estimation/one-off issues |
| 7 | Cash flow analysis | financial_analysis.md and research/company/cash_flow_framework.md; OCF, FCF convention, capex, working capital, funding |
| 8 | Investment Quality Score — V1.2 | scoring/investment_scorecard_v1.md, scoring/scoring_rules.md, scoring/score_interpretation.md; use original version, score, coverage, strengths/weaknesses |
| 9 | AI Moat Evolution Score — V1.3 | scoring/ai_moat_score_v1.md, scoring/ai_moat_scoring_rules.md, scoring/ai_moat_evolution.md; use original outputs, applicability and coverage |
| 10 | Valuation — V1.4 | valuation/valuation_framework_v1.md and supporting model/rules; select suitable methods, dated price, scenarios, MOS and confidence |
| 11 | Risk Engine | decision/risk_engine.md (V1.5); complete 11 risks and aggregate/override status |
| 12 | Catalyst Engine | decision/catalyst_engine.md (V1.5); evidence, timing, potential impact and confirmation signals |
| 13 | Bull / Base / Bear scenarios | decision/bull_base_bear.md; link V1.4 values, disclose assumptions/probabilities and sum probabilities to exactly 100% |
| 14 | Investment Decision Engine — V1.5 | decision/investment_decision_engine_v1.md and decision_rules.md; show components, coverage, confidence, gates, overrides and one classification |
| 15 | Final Investment Thesis | research/company/investment_thesis.md; explain thesis, what must go right, failure paths and invalidators |
| 16 | Monitoring checklist | master report §17 and company_profile.md or report-specific checklist; define signal, purpose, good/bad movement and frequency |

## Stage gates and handoffs
- Identity gate: resolve legal issuer and ticker before attaching company financials. If unresolved, stop company-specific scoring and mark decision INSUFFICIENT DATA.
- Financial gate: state the latest available financial period and audited/reviewed/unaudited status. Present history on consistent consolidation, fiscal period, unit and share basis. Use shorter history only when five years are unavailable and say so.
- Upstream gate: pass V1.2 and V1.3 outputs with their own required coverage/status; do not recompute them in V1.6.
- Valuation gate: V1.4 method selection, assumptions, price date, per-share basis, Bear/Base/Bull values, MOS and confidence must reconcile; unavailable values remain N/A.
- Decision gate: apply V1.5 coverage, evidence-confidence and override hierarchy. Bear/Base/Bull probabilities must total exactly 100% for a standard final decision; a substantiated HIGH RISK override remains reportable under V1.5 rules.
- Publish gate: complete reports/report_quality_checklist.md and include unresolved gaps and disclaimer.

## Final deliverables
Use research/company/full_research_report_template.md as the canonical assembled report. Detail modules are working papers; avoid copying untraceable values into the master. Every upstream result retains its date/version, and every material number traces to a source or a disclosed formula. Update monitoring indicators at results releases, material announcements and scheduled review dates. Keep prior report versions for change tracking; never overwrite historical facts with later periods without noting the revision.
