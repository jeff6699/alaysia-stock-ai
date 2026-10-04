# Evidence-to-Research Mapping V1.7

## Purpose
Map source records to the existing V1.2–V1.6 modules while preserving the upstream rules. Each material statement in the final report must trace through one or more evidence IDs to a source/locator, or be marked N/A.

## Flow
Evidence → Financial Analysis → Moat Analysis → Valuation → Risk Analysis → Catalyst Analysis → Investment Thesis → 100-point Score → Investment Decision

This is a traceability path, not a requirement that every fact affect every module. Map relevant evidence only; disclose when an input is not used and why.

| Evidence topic | First research destination | Downstream destination | Existing framework / rule |
|---|---|---|---|
| Identity, segments, customers, geography, business drivers | V1.6 company profile | Competitive position, risks, thesis | Do not invent unknown names; N/A |
| Financial statements, margins, ROE/ROIC, debt, cash, FCF, shares | V1.6 financial analysis | Quality, valuation, risk, thesis | V1.1 financial framework; V1.2 unchanged scorecard/rules |
| Customer value, cost, scale, switching, network, IP, data, AI | V1.6 moat analysis | Thesis, disruption/opportunity, decision | V1.3 unchanged score/scoring/evolution rules |
| Price, share count, assumptions, peers, segment values | V1.6 valuation analysis | MOS, scenarios, decision | V1.4 unchanged valuation formulas, method selection and confidence |
| Balance sheet, cash flow, earnings, governance, competition, regulation, macro | V1.6 risk analysis | Overrides and final classification | V1.5 risk_engine.md and decision_rules.md |
| Contracts, capacity, products, industry and macro events | V1.6 catalyst analysis | Scenarios, thesis, decision | V1.5 catalyst_engine.md |
| Base/Bear/Bull input evidence and analyst probabilities | V1.5 scenario module / V1.6 master report | Decision and thesis | V1.4 fair values; V1.5 probability/override rules |
| Combined score, data confidence, gates and overrides | V1.5 decision output | Final investment thesis and report | V1.5 decision_rules.md; never replace N/A with a score |
| Macro series | Macro evidence record | Industry, financial forecast, valuation, risk, catalyst | Official dated series; causal effect is ANALYSIS/INFERENCE |

## Traceability chain
For each conclusion retain:
1. Final report claim ID or named section.
2. Relevant research module, metric ID or thesis statement.
3. Evidence ID(s), including contrary/conflicting evidence.
4. Source, date, locator, period, units and source/evidence quality.
5. Any transformation or formula and its complete inputs.
6. Analyst interpretation and uncertainty; assumptions/forecast horizon where relevant.
7. V1.2/V1.3/V1.4/V1.5 module/version and output, if consumed.

One source can support multiple claims; use separate mappings so each claim's actual scope stays clear. One claim may require multiple records. A score or valuation output is not a primary source: trace it both to its methodology version and to the underlying evidence/assumptions.

## Boundary with upstream frameworks
V1.7 provides source data and quality flags. It does not recompute V1.2's 100-point quality score, V1.3's moat score, V1.4's valuation/MOS, or V1.5's risk/catalyst/decision logic. V1.6 assembles and narrates those versioned outputs. If source inputs are missing or conflict, follow the existing module's N/A, coverage and confidence rules.

## Evidence labels and missing data
- FACT: directly source-supported observation or reproducible calculation with its inputs and formula.
- ANALYSIS: interpretation of verified facts with method and limitations.
- INFERENCE: qualified conclusion derived from evidence, including uncertainty and alternatives.
- FORECAST: conditional forward view with horizon and explicitly identified ASSUMPTIONS.
Missing evidence is MISSING and displayed as N/A with its downstream effect; do not fabricate or silently substitute a value.

## Upstream module references
- V1.2 Investment Quality: scoring/investment_scorecard_v1.md, scoring/scoring_rules.md, scoring/score_interpretation.md.
- V1.3 AI Moat Evolution: scoring/ai_moat_score_v1.md, scoring/ai_moat_scoring_rules.md, scoring/ai_moat_evolution.md.
- V1.4 Valuation: valuation/valuation_framework_v1.md, valuation/dcf_model.md, valuation/relative_valuation.md, valuation/scenario_valuation.md, valuation/margin_of_safety.md.
- V1.5 Decision: decision/investment_decision_engine_v1.md, decision/decision_rules.md, decision/risk_engine.md, decision/catalyst_engine.md, decision/bull_base_bear.md.
- V1.6 Assembly: research/research_pipeline_v1.md, research/company/full_research_report_template.md, reports/report_quality_checklist.md.
