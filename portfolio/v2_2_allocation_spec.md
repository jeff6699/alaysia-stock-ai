# V2.2 Portfolio Allocation Engine Specification

## Purpose and boundaries
V2.2 ranks opportunities and estimates a capital budget using portfolio holdings, verified research outputs and configurable investor constraints. It is a decision-support system only. It does not place orders, execute trades or guarantee outcomes. It does not replace/recalculate V1.2 scoring, V1.3 moat, V1.4 valuation, V1.5 decision, V2.0 portfolio decision or V2.1 stock report.

Every factual input needs a dated source reference. Use N/A or REQUIRES_VERIFICATION for missing/unverified data. Separate FACT, ANALYSIS, INFERENCE and FORECAST; valuation and allocation assumptions are clearly ASSUMPTION. Average cost is informational and never determines whether to add.

## Inputs
For each portfolio holding and candidate collect:
- Ticker, company, shares, average cost.
- Current price and date, current market value and date, portfolio weight.
- Available cash, current portfolio value and optional minimum cash reserve.
- V1.2 Fundamental/Quality Score and coverage.
- V1.3 AI Moat Score, durability and coverage.
- V1.4 valuation range, current MOS, confidence, required MOS/buy-below ceiling.
- V1.5 Investment Decision, Risk Rating, Catalyst output and data confidence.
- V2.0 Portfolio Decision (ACCUMULATE / HOLD / WATCH / REDUCE / EXIT).
- Concentration exposure, sector/theme look-through, target horizon, position class, target weight and max weight.
- Source IDs, periods, timestamps, currencies, units, assumptions and validation status.

Missing required inputs remain N/A; if identity/current price/portfolio value/research decision cannot be verified, block allocation sizing for that candidate.

## Capital Allocation Score — 100 points
Weights are configurable at portfolio-policy level but must sum to exactly 100 for each run. The default weights below are policy starting points, not universal investment rules.

| Component | Weight | Existing input / V2.2 treatment |
|---|---:|---|
| Fundamental Quality | 20 | V1.2 valid standard score × 0.20 |
| Earnings / Cash Flow Quality | 15 | Evidence-based V1.1/V1.6 analysis rubric below; no fabricated metrics |
| AI Moat / Competitive Advantage | 10 | V1.3 final composite × 0.10, honoring V1.3 coverage |
| Valuation / Margin of Safety | 20 | V1.4 MOS mapped by valuation bands below; confidence cap/gate applies |
| Risk | 10 | V1.5 risk label translated using table below; severity cannot be averaged away |
| Portfolio Fit | 15 | Concentration 5 + position headroom 5 + diversification/overlap 5 |
| Catalysts | 5 | V1.5 catalyst score / 10 × 0.5 |
| Data Confidence | 5 | HIGH 5 / MEDIUM 3 / LOW 0 / unknown N/A |
| TOTAL | 100 | |

A valid weak result scores low and remains available. An N/A component contributes neither earned points nor available points. Report Earned / 100, Available / 100 and coverage = Available / 100. A provisional normalized comparison (Earned / Available × 100) may be shown only beside raw Earned / 100; it is not used to overcome missing-data gates. Do not call incomplete scores fully comparable.

### Component scoring and rationale
- **Fundamental Quality (20):** use V1.2's valid 0–100 score × 20/100. This carries through the existing financial-quality rubric rather than duplicating it. Missing/invalid V1.2 grade = N/A.
- **Earnings / Cash Flow Quality (15):** based on cited V1.1/V1.6 findings, not a fabricated ratio: 12–15 when earnings are explainable/repeatable and cash conversion is sound or sector-appropriate with no material unresolved quality warnings; 8–11 when generally sound but mixed/variable with bounded concerns; 4–7 when several material accrual, one-off, collection, inventory or cash-conversion concerns weaken reliability; 0–3 when reliable evidence shows severe deterioration, repeated unexplained divergence or unreliable earnings. Use the lower band only when supported. If required reporting data are unavailable, mark N/A. Explain criterion and sources.
- **AI Moat / Competitive Advantage (10):** V1.3 final composite × 10/100 when its final composite is valid under V1.3. Do not use just the current-moat subscore in place of the composite.
- **Valuation / MOS (20):** use V1.4 current Base MOS and confidence. MOS ≥40%: 20; 30% to <40%: 17; 20% to <30%: 14; 10% to <20%: 10; 0% to <10%: 6; MOS <0%: 0. N/A/invalid V1.4 MOS = N/A. These are V2.2 allocation-priority bands, not changes to V1.4. Low V1.4 confidence caps this component at 5/20 and prohibits PRIORITY ACCUMULATE/ACCUMULATE; Medium caps it at 15/20; high confidence does not guarantee addition. Compare MOS to V1.4's company-specific required MOS before any add action.
- **Risk (10):** use V1.5 aggregate Risk Rating: Low 10, Moderate 7, Elevated 4, High 1, Critical 0. Unknown = N/A. This score does not cancel a risk override or V1.5 HIGH RISK classification. A material Critical risk blocks new capital; high-risk-turnaround exception is tightly capped below.
- **Portfolio Fit (15):** sum three components, each 0–5. Concentration: 5 below 70% of any applicable cap, 3 from 70% to <90%, 1 from 90% to <100%, 0 at/above cap. Position headroom: 5 when proposed target is <50% of position max, 3 at 50% to <80%, 1 at 80% to <100%, 0 at/above max. Diversification/overlap: 5 when verified exposure reduces underrepresented risk without breaching policy limits, 3 neutral, 1 adds to an already-high correlated exposure, 0 breaches a configured limit. N/A if portfolio look-through cannot be validated.
- **Catalysts (5):** reuse V1.5 catalyst score as a fraction of its 10-point maximum, ×0.5; use its coverage/status. Catalyst probability is not allocation probability.
- **Data Confidence (5):** use integrated research confidence: HIGH 5, MEDIUM 3, LOW 0; unknown N/A. Apply the V1.5 decision confidence gates independently.

## Suggested actions and decision gates
Output exactly one V2.2 action per candidate: PRIORITY ACCUMULATE, ACCUMULATE, HOLD, WAIT FOR BETTER PRICE, WATCH, REDUCE or DO NOT ADD.

Apply hard gates before interpreting the score:
1. Invalid identity, missing current price/NAV, missing V1.5 decision, unverified critical sources, or allocation-score coverage below 80% → WATCH; suggested new amount RM0.
2. V1.5 HIGH RISK, V1.5 INSUFFICIENT DATA, V2.0 EXIT/REDUCE, active thesis invalidator, or material Critical risk → no new capital. If held, use V2.0/V1.5 result to choose REDUCE, WATCH or DO NOT ADD; do not override upstream rules.
3. Current price above V1.4 required-MOS buy-below ceiling, or V1.5 FAIRLY VALUED/OVERVALUED → WAIT FOR BETTER PRICE unless a stronger no-add/REDUCE gate applies.
4. No portfolio headroom, hard limit reached, or cash reserve would be breached → DO NOT ADD.
5. PRIORITY ACCUMULATE: score ≥85, V1.5 rating STRONG OPPORTUNITY or ATTRACTIVE, V2.0 ACCUMULATE, V1.4 confidence Medium/High and MOS meets V1.4 required MOS, overall risk Low/Moderate, no concentration breach and no critical data gap. LOW V1.4 confidence cannot pass this gate.
6. ACCUMULATE: score 70–<85 with the same evidence, valuation, V2.0, risk and capacity gates; high V1.4 confidence is not mandatory.
7. HOLD: owned position, score 55–<70, thesis intact, V2.0 HOLD, valuation not a no-add gate and risk manageable.
8. WATCH: score below 70 without a stronger action, unconfirmed thesis/catalyst, or information/timing limits. For an unowned candidate, do not disguise WATCH as a purchase.
9. REDUCE: only for an existing holding when V1.5/V2.0 or verified portfolio/risk rules support a reduction. No automated sale amount.
10. DO NOT ADD: no new capital because a hard cap/reserve/high-risk gate blocks additions or upstream verdict disallows them. It is not automatically a sell recommendation.

When gates conflict, the most restrictive action applies. A high score never cancels critical risk or excessive valuation.

## Price, cost basis and allocation rules
- Never add solely because current price is below average cost; average cost is not intrinsic value.
- Falling prices are not buy signals. Reassess thesis, evidence, V1.4 value, risk and concentration.
- Adding to winners may be allowed only if V1.4 required MOS, V1.5 and V2.0 gates pass and position capacity remains. Adding to losers follows the same gates and requires thesis revalidation.
- Preferred entry range comes from V1.4-supported scenario/sensitivity outputs. At minimum report the V1.4 MOS buy-below ceiling; if no defensible lower bound/range exists, show lower bound N/A rather than inventing one. Never state an entry as a guaranteed price.
- Position class caps: Core 15%, Growth 12%, Satellite 5%, High-risk turnaround 3%. These are configurable defaults, not universal rules. User policy may tighten/alter them; document every override and reason.
- High-risk turnaround: only when explicitly permitted by investor mandate, not Critical, no V1.5/V2.0 prohibition, thesis/recovery milestones evidenced, and total position ≤3% NAV. Otherwise DO NOT ADD; if current position exceeds its approved cap, flag for human review.
- Existing large positions receive lower incremental allocation because target headroom and concentration scores fall. No adding beyond the minimum of target, class max, issuer/sector/theme caps and cash limit.
- No automatic trade execution. Suggested amount is a budget estimate, not an order, share quantity or instruction.

## Cash reserve and suggested amount
Set defaults in automation/pipeline config:
- Core maximum: 15% NAV.
- Growth maximum: 12% NAV.
- Satellite maximum: 5% NAV.
- High-risk turnaround maximum: 3% NAV.
- Minimum cash reserve: 10% of post-valuation portfolio NAV.

All are configurable. If the user supplies a reserve percentage, it replaces the default; if a cash floor in RM is also supplied, preserve both by using the larger required reserve. State whether the reserve is a percentage or RM amount and the valuation date.

- Portfolio NAV = current marked market value of holdings + available cash + other included assets − liabilities, with definitions and sources. If liabilities/other assets are excluded, explicitly state this simplified basis.
- Reserve target = max(configured cash floor in RM, configured reserve percentage × post-allocation NAV). With no user override, use default 10% NAV.
- Deployable cash = max(0, available cash − reserve target − explicitly included known costs). If existing cash is below reserve target, allocate RM0.
- Candidate target gap = max(0, min(configured target weight, applicable maximum weight) − current weight) × portfolio NAV.
- Rank eligible candidates by action gate first, then Capital Allocation Score, then larger MOS above required MOS, then lower correlated concentration; document tie-break.
- Initial demand can be apportioned across eligible candidates in proportion to scores. Cap each amount by its target gap. Redistribute residual cash to the next ranked eligible candidate only while all caps and reserve remain satisfied.
- Suggested amount = min(candidate allocation budget, target gap, remaining deployable cash). Sum of all suggested amounts must be ≤ deployable cash and total portfolio cash after allocation must remain ≥ reserve target.
- Suggested percentage of new cash = suggested amount / deployable cash ×100%; if deployable cash is 0/N/A, percentage is N/A.
- Round budget amounts to stated currency precision; do not calculate trade quantity. Include transaction costs only when sourced or user-provided; otherwise disclose their exclusion.

## Concentration controls
Use current weights based on dated market values, not average cost. Reconcile holdings plus cash to NAV and disclose rounding. Look through funds/holding companies to underlying sectors/themes only where verified; avoid double counting a subsidiary if separately held.

Configurable default soft limits:
- Any one issuer: the position class cap above.
- Sector: 30% NAV.
- Banks: 25% NAV combined, including CIMB/MAYBANK and other verified bank holdings.
- REITs: 25% NAV combined, including SUNREIT/CLMT/AXREIT and other verified listed REIT holdings.
- AI/data-centre theme: 25% NAV look-through combined; include only verified direct/indirect exposure.
Alert at 80% of each limit. At a limit, DO NOT ADD to exposure absent explicit documented policy override. Above a cap, flag REDUCE/review; do not auto-sell. These default portfolio-policy limits are configurable and are not universal suitability advice. Sector/industry classification and look-through must be sourced and date-stamped.

## RM10,000 cash example — illustrative assumptions only
All company labels, scores, weights, amounts and portfolio values below are **ASSUMPTION — ILLUSTRATIVE ONLY**, not real holdings, financial data, current prices or a recommendation. Real V1.2–V2.1 outputs and evidence are N/A in this example.
- Portfolio NAV: RM50,000 (assumed).
- Available cash: RM10,000 (assumed).
- Minimum cash reserve: 10% NAV = RM5,000 (assumed policy).
- Deployable cash: RM10,000 − RM5,000 = RM5,000.
- Illustrative Candidate A: score 90, eligible, current weight 5%, target/max 15%, headroom RM5,000.
- Illustrative Candidate B: score 75, eligible, current weight 4%, target/max 12%, headroom RM4,000.
- Proportional initial split by score: A = RM5,000 × 90/165 ≈ RM2,727; B = RM5,000 × 75/165 ≈ RM2,273. Both are under assumed headroom and sum to RM5,000.
- Percentage of deployable cash: A 54.54%, B 45.46%; retained reserve RM5,000.
- Entry range/current price: N/A — DATA NOT AVAILABLE; no price is invented.
This is arithmetic illustration of the sizing rule only; it does not mean either candidate exists or passes an actual research gate.

## Required final candidate allocation table
The report includes one row per holding/candidate, including names receiving no new capital.

| Ticker | Current portfolio weight | Capital Allocation Score / coverage | Suggested action | Suggested amount | % of deployable new cash | Preferred entry range / V1.4 ceiling | Maximum position weight | Main reason | Main risk | What would invalidate allocation |
|---|---:|---:|---|---:|---:|---|---:|---|---|---|
|  |  |  |  |  |  |  |  |  |  |  |

Amounts are in the portfolio reporting currency and are budgets, not orders. Where an entry range, score, evidence or amount cannot be supported, show N/A and the controlling gate.
