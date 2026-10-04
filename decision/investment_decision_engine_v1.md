# Investment Decision Engine V1.5

## Purpose and boundaries
Combine the existing V1.2 Investment Quality Score, V1.3 AI Moat Evolution Score, and V1.4 valuation outputs with explicit risk, catalysts, scenarios, and evidence confidence. This is a decision-support framework, not an automatic buy/sell recommendation. It does not change the prior versions' scoring rules or valuation formulas.

Use the source modules listed in the audit section and retain their versions, dates, inputs, and outputs. Never infer a missing upstream score; show N/A and its effect.

## Decision inputs
Freeze company, Bursa ticker, sector, analysis date, price date, reporting periods, currency, units, source set, and versions. Summarize:
- V1.2 quality score, rating, coverage, strengths, weaknesses.
- V1.3 current moat score, durability, evolution, AI disruption risk, AI opportunity, coverage.
- V1.4 current price, Bear/Base/Bull fair values, base MOS, valuation confidence and method coverage.
- The 11 risks, up to 10 catalyst types, scenario probabilities, and data confidence.
- Evidence labels: FACT, ANALYSIS, ASSUMPTION, INFERENCE, FORECAST.

## Decision Score (100 points)
| Component | Maximum | V1.5 treatment |
|---|---:|---|
| Investment Quality | 30 | V1.2 standard 0–100 score × 0.30, only when its standard-grade coverage requirement is met |
| AI Moat Evolution | 20 | V1.3 final composite 0–100 × 0.20, only when its final-rating coverage requirement is met |
| Valuation / Margin of Safety | 25 | V1.4 current MOS and confidence mapped by decision_rules.md |
| Risk Profile | 15 | Risk-control points from risk_engine.md; more points means lower evidenced risk |
| Catalysts | 10 | Evidence-quality points across the 10 candidate categories in catalyst_engine.md |
| TOTAL | 100 | |

These components are not averaged. V1.2 and V1.3 retain their own rubrics; V1.5 scales their valid results proportionally. Risk and catalysts use separate explicit rules. A high score cannot cancel an override. A substantiated severe-risk finding takes priority over unrelated data gaps.

For every component report earned points, available points, evidence, calculation/rule, and rationale. A valid poor result earns its actual low points and remains available; unavailable or unscoreable data is N/A and contributes neither earned nor available points. Coverage = available points / 100. If coverage is below 80%, or a critical upstream input is N/A, classification is INSUFFICIENT DATA unless reliable evidence independently establishes a HIGH RISK override. At coverage ≥80% an optional provisional comparison is earned / available × 100, shown beside the unnormalized earned/100; it cannot bypass a critical-data gate, a low-confidence cap, or an override. Do not award missing points through normalization.

## Calculation and interpretation order
1. Validate source versions, dates, units, upstream coverage, price and valuation consistency.
2. Determine component availability; calculate earned/available points and coverage.
3. Apply evidence-backed HIGH RISK overrides first, then insufficiency and confidence gates, as ordered in decision_rules.md.
4. If no override applies, use the provisional/complete score band plus valuation context and the decision rules to select one label.
5. Explain the decisive evidence and why adjacent labels were not selected.

The single final classification is one of: STRONG OPPORTUNITY, ATTRACTIVE, WATCHLIST, FAIRLY VALUED, OVERVALUED, HIGH RISK, INSUFFICIENT DATA. The score is a structured summary, not a probability of return or a price target.

## Integrated inputs and required display
### Quality — V1.2
Display original Quality Score, original rating/coverage, key strengths and weaknesses. Do not recompute metric scores. A partial V1.2 score is not a standard grade.

### AI moat — V1.3
Display Current Moat Score, Moat Durability, 3-Year Evolution, AI Disruption Risk, AI Opportunity, composite coverage, and the framework's final assessment. Do not replace the V1.3 dimension or composite rubric.

### Valuation — V1.4
Display dated Current Price; Bear, Base, Bull Fair Value; Base MOS; Valuation Confidence; Base Upside/Downside, Bear Downside and Bull Upside. Use V1.4 formulas only:
- Base upside/downside = (Base FV / Current Price − 1) × 100%.
- Bear downside = (Bear FV / Current Price − 1) × 100%.
- Bull upside = (Bull FV / Current Price − 1) × 100%.
- Base MOS = (Base FV − Current Price) / Base FV × 100%.
If price/value/denominator is invalid, show N/A and state the impact. Keep all value/share and currency bases aligned.

## Evidence and data confidence
For each material claim provide a source and locator/date or N/A. FACT is sourced observation/calculation; ANALYSIS explains comparison; ASSUMPTION identifies analyst-selected inputs; INFERENCE is a qualified interpretation; FORECAST is an explicitly conditional future outcome. Never present forecasts or management targets as facts.

Rate data confidence HIGH / MEDIUM / LOW using completeness, recency, source quality, consistency, and unresolved assumptions in decision_rules.md. LOW confidence prevents STRONG OPPORTUNITY or ATTRACTIVE; use WATCHLIST unless an insufficiency or HIGH RISK override applies. Missing evidence lowers coverage or confidence as specified; it is not evidence of a positive or negative outcome.

## Standard report
Use research/company/investment_decision_report_template.md. Include 3 reasons to own and not own, what must go right, thesis invalidators, five monitoring indicators, scenario probabilities totaling exactly 100%, and an audit trail. Scenario expected returns are based on each scenario FV and the dated current price; retain assumptions and do not replace V1.4 valuation.

## Audit trail
| Decision input | Source module | Required trace |
|---|---|---|
| Quality | scoring/investment_scorecard_v1.md and scoring/scoring_rules.md | V1.2 version, raw score, available/total, rating, source date |
| AI moat | scoring/ai_moat_score_v1.md, scoring/ai_moat_scoring_rules.md, scoring/ai_moat_evolution.md | V1.3 version, component outputs, coverage, evidence date |
| Valuation/MOS | valuation/valuation_framework_v1.md, valuation/scenario_valuation.md, valuation/margin_of_safety.md | V1.4 version, dated price/FVs, assumptions, confidence |
| Risk | decision/risk_engine.md | risk register, severity, probability, aggregation, override |
| Catalysts | decision/catalyst_engine.md | evidence, timeframe, impact, probability, confirmation test, points |
| Scenarios | decision/bull_base_bear.md | assumptions, probabilities, FV, return and source |
| Final classification | decision/decision_rules.md | score, coverage, confidence, applied gates and explanation |

## Bursa Malaysia use
Prefer current Bursa announcements and issuer filings for company facts. Record filing status and date, reporting basis, share/corporate-action basis, currency and units. Sector-specific N/A must follow the upstream rubric. Consider Bursa-specific regulatory, governance, liquidity, ownership and disclosure evidence only when sourced. This framework does not supply investment advice.
