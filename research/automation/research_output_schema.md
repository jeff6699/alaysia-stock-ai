# Research Output Schema V1.9

## Required report structure
Every complete automated company report contains:
1. Executive Summary
2. Company Profile
3. Business Model
4. Industry Analysis
5. Financial Analysis
6. Earnings Quality
7. Cash Flow
8. AI Moat
9. Valuation
10. Risk Analysis
11. Catalysts
12. Bull Case
13. Base Case
14. Bear Case
15. Investment Thesis
16. 100-Point Score
17. Investment Decision
18. Evidence Quality
19. Missing Data
20. Research Confidence
21. Source List

The 21 named sections include the requested topics and keep Bull, Base and Bear separately reviewable. The detailed report may add competitive position and monitoring sections from V1.6; do not omit these if required by its report checklist.

## Output record
- Run ID / report version:
- Company / Bursa ticker/security class:
- Research date / price observation date:
- Latest financial period / filing status:
- Currency / units / accounting/share basis:
- Methodology versions V1.2–V1.9:
- Evidence register and mapping:
- Report path:
- Reviewer / generation date:
- Overall completion status:

## Required per-claim fields
For every material number, claim, risk, catalyst, thesis reason, score, valuation and decision:
- Claim/metric and output section.
- Label FACT / ANALYSIS / INFERENCE / FORECAST; ASSUMPTION where selected.
- Evidence ID(s), source metadata ID(s), exact source/document locator and date.
- Period, unit, currency, basis and status, where applicable.
- Formula/methodology path and version for calculations or score outputs.
- N/A, conflict, verification or confidence limitation and downstream impact.

## Research confidence
Rate HIGH / MEDIUM / LOW qualitatively using six factors: source quality, data completeness, reporting-period consistency, evidence coverage, conflicting information and financial-data reliability. Explain each factor. Do not convert to a numeric average or claim statistical probability. Use weakest critical factor where unresolved; research/automation/research_quality_control.md governs.

## Missing and verification states
- Missing metric: display **N/A — DATA NOT AVAILABLE**.
- Unverified source/extraction: display **REQUIRES_VERIFICATION**.
- Conflicting credible values: display **CONFLICT**, retain both source IDs and resolution status.
- Estimate/model value: display **ESTIMATED**, label ASSUMPTIONS and forecast horizon.
Do not put an invented numeric value in any status.

## Version and method boundaries
Include explicit upstream output/version references:
- V1.2 Quality score and coverage.
- V1.3 AI Moat outputs.
- V1.4 valuation range/MOS/confidence.
- V1.5 risks, catalysts, scenario probabilities and decision.
- V1.6 research stages/template.
- V1.7 evidence/source quality.
- V1.8 ingestion records/period controls.
V1.9 assembles and traces; it does not replace any source engine.

## Confidence factor anchors
Use qualitative descriptions; do not assign numerical percentages.
| Factor | HIGH | MEDIUM | LOW |
|---|---|---|---|
| Source quality | Material claims trace to mostly Tier 1 / A or credible B evidence | Mix of reliable sources with bounded secondary reliance | Material claims depend on weak/unverifiable sources or C sources |
| Data completeness | Key company, financial and decision inputs are present or N/A is immaterial | Non-critical gaps remain and are explained | Important inputs missing or critical decision inputs unavailable |
| Reporting-period consistency | Periods, units, currency, basis and restatements reconcile | Limited, understood differences remain | Material period/basis conflicts prevent reliable comparison |
| Evidence coverage | Material claims and outputs map to source records and locators | Some non-critical claims have incomplete mapping | Important conclusions lack traceable evidence |
| Conflicting information | Material conflicts resolved and superseded records retained | Bounded conflicts do not change key conclusions | Material conflicts remain unresolved |
| Financial-data reliability | Statements are authoritative, status/definitions clear and checks reconcile | Some estimates or reconciliation gaps are bounded | Financial records are unverified, materially inconsistent or unreliable |

Overall confidence is a reasoned judgment, not an average. A low rating on a decision-critical factor prevents an overall HIGH rating. State what would improve confidence. Continue to follow V1.7/V1.5 gates; these anchors do not create new score thresholds.
