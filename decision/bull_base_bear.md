# Bull / Base / Bear Decision Scenarios

## Purpose
Describe conditional investment outcomes using V1.4 fair values and explicit scenario assumptions. This is not a second valuation model. The scenario Fair Value must trace to the matching V1.4 Bear/Base/Bull output or explain an approved V1.4 scenario mapping. Do not invent financial data or independently rebuild V1.4 formulas.

## Scenario record
For each scenario document:
- **Probability:** analyst ASSUMPTION with rationale; not a historical frequency unless sourced.
- **Fair Value:** V1.4 per-share value, date, currency and source; N/A if unavailable.
- **Expected Return:** (scenario Fair Value / dated Current Price − 1) × 100%, using consistent share/currency basis; N/A if either input is invalid.
- **Key Assumptions:** growth, margin, earnings, valuation, catalyst, time horizon and source; explicitly label all analyst choices ASSUMPTION.
- **Main Risk:** what could make the scenario fail and observable evidence.
- FACT, ANALYSIS, INFERENCE and FORECAST kept distinct.

### BEAR CASE
- Assumptions: lower growth/margins/earnings and/or adverse valuation context, as supported in V1.4.
- Probability: [0–100%]
- Fair Value: [V1.4 Bear FV or N/A]
- Expected Return: [formula above or N/A]
- Key Assumptions:
- Main Risk:

### BASE CASE
- Assumptions: central evidence-supported growth, margin, earnings, valuation and expected catalysts, mapped to V1.4 Base case.
- Probability: [0–100%]
- Fair Value: [V1.4 Base FV or N/A]
- Expected Return:
- Key Assumptions:
- Main Risk:

### BULL CASE
- Assumptions: favorable but supportable growth, margins, earnings, valuation and positive catalysts, mapped to V1.4 Bull case.
- Probability: [0–100%]
- Fair Value: [V1.4 Bull FV or N/A]
- Expected Return:
- Key Assumptions:
- Main Risk:

## Probability integrity
Assign each scenario probability once. The three probabilities must be numeric percentages and total exactly 100% (e.g. Bear + Base + Bull = 100%). Explain probability rationale and evidence; do not use probabilities as facts. If probabilities are unavailable or sum other than 100%, correct the assumptions before issuing a final V1.5 decision. Do not normalize silently. Report 100% exactly at whole-percent precision; if decimal percentages are used, their arithmetic sum must still equal 100.00%.

## Ordering and use
Check scenario fair values, expected returns and assumptions are directionally coherent (normally Bear FV ≤ Base FV ≤ Bull FV). Explain sourced/structural exceptions. Keep scenario probabilities distinct from V1.4 fair-value ranges and catalyst probabilities. Any weighted expected value is optional, must show the probability arithmetic and must not replace Base FV, margin of safety, Bear downside, or valuation confidence. A scenario set is conditional, not a guarantee.
