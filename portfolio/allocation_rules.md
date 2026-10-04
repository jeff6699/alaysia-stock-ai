# Portfolio Allocation Rules V2.2

## Policy scope and evidence
These are configurable decision-support rules, not universal investment recommendations. They reuse V1.2–V2.1 outputs and never replace their methodologies. All material portfolio values, sector/theme tags, issuer identities, scores and constraints require dated source references. Unknown = N/A; unverified = REQUIRES_VERIFICATION. Keep FACT, ANALYSIS, INFERENCE and FORECAST separate.

## Position classes and caps
| Class | Default maximum of NAV | Intended use |
|---|---:|---|
| Core | 15% | Higher-conviction, diversified, evidence-supported long-horizon holding |
| Growth | 12% | Growth exposure with material execution/valuation sensitivity |
| Satellite | 5% | Narrow, cyclical, thematic or less-proven exposure |
| High-risk turnaround | 3% | Speculative recovery case with explicit investor mandate and milestones |

These are configurable starting limits, not universal suitability rules. Record chosen class, target weight, max weight, reason, author/date and any policy override. Never silently raise a cap. A reduction alert is not an automatic sell order.

## Position-sizing formula and ranking
1. Validate shares, dated price, market value, NAV, cash, weight and source. Current value is shares × dated current price if both are verified; preserve source-reported value separately.
2. Current weight = current market value / current portfolio NAV ×100. Include cash/other assets/liabilities consistently in NAV; state simplified NAV if applicable.
3. Target gap value = max(0, min(target weight, class maximum, applicable issuer/sector/theme limit room) − current weight) × NAV.
4. Filter candidates through V2.2 action gates in portfolio/v2_2_allocation_spec.md. Ineligible names receive RM0.
5. Rank first by permitted action, then score, then MOS above V1.4 required MOS, then concentration diversification benefit. Document ties.
6. Allocate no more than target gap or deployable cash. If splitting across names, distribute in score proportion subject to caps; after a cap binds, reallocate residual only to eligible names.
7. Verify suggested budgets sum to ≤ deployable cash and retained cash meets reserve. Suggested percentage of new cash uses deployable cash as denominator.
8. Report amount only; do not create order quantity or execute trades.

A missing critical value or score coverage below V2.2's gate means WATCH/DO NOT ADD, not a guessed allocation. Money cannot be budgeted from market value based on average cost.

## Concentration control
Calculate issuer, sector, industry, country, bank, REIT, customer/commodity/FX and AI/data-centre theme exposure where data permit. Use look-through for funds/groups only with a sourced ownership/exposure map; do not double count a directly held subsidiary and its parent exposure. Mark unavailable look-through N/A and lower confidence.

Configurable default policy limits from the V2.2 spec:
- Single position: class caps 15% / 12% / 5% / 3%.
- Sector 30% NAV.
- Banks 25% NAV combined.
- REITs 25% NAV combined.
- AI/data-centre theme 25% NAV combined.
Alert at 80% of limit. At/above limit, do not add to that risk bucket; above limit flags a human review for possible REDUCE. Limits may be set differently by the user with explicit rationale and date; no silent overrides.

### Bank concentration
Aggregate all banks and bank-sensitive financial issuers by verified holdings and look-through exposure. Apply the configured combined bank limit. Review common credit cycle, funding, rates, geography and macro exposures using latest evidence. CIMB and MAYBANK are named portfolio examples; count their current exposure only after identity and data are verified. Strong individual bank score does not bypass the combined limit.

### REIT concentration
Aggregate direct REIT units and verified property/REIT look-through exposure under the configured REIT cap. Review rates, gearing, occupancy, tenant/asset/geographic concentration and distribution funding from current disclosures. SUNREIT, CLMT and AXREIT are examples to check; their classifications and exposure weights must be verified. Do not treat a high yield alone as diversification or a buy signal.

### AI/data-centre thematic concentration
Look through direct holdings and issuer segment exposure only where evidenced. Aggregate companies whose current disclosed revenues/assets/contracts create material exposure to AI/data-centre capex, power, construction, connectivity or real estate. Record attribution method and avoid counting the same underlying project twice. The default theme limit is configurable; new label claims do not establish exposure by themselves.

### Sector and correlated exposure
Sector limit applies to verified issuer classifications, while a separate correlated-risk view may group different sectors sharing rates, construction cycle, consumer demand, FX, commodity or government spending. Do not sum correlated categories as if independent or double count portfolio NAV. Explain the risk pathway.

## Valuation and margin of safety
- Consume V1.4 Current Price/date, Bear/Base/Bull fair value, current MOS, confidence, required MOS and buy-below ceiling.
- Do not run a second valuation or modify V1.4 formulas. Do not enter an entry price without a dated V1.4 supportable output.
- If current MOS is below the company-specific required MOS, classify WAIT FOR BETTER PRICE for otherwise sound candidates; do not add on price decline alone.
- If V1.5 is FAIRLY VALUED or OVERVALUED, no ACCUMULATE classification. If V1.5 HIGH RISK/INSUFFICIENT DATA, follow V1.5 priority/gates.
- Low V1.4 confidence caps allocation-priority score and blocks ACCUMULATE; Medium caps score under V2.2; high confidence does not guarantee addition.
- If V1.4 current price/value/date/share basis mismatches, use N/A and do not allocate.

## Existing cost basis neutrality
Average cost is retained for reporting unrealized gain/loss and tax/accounting context where relevant, never for intrinsic value, MOS or target weight. A position below cost is not automatically cheap; a position above cost is not automatically expensive. Decision uses current evidence, price versus V1.4 value, thesis, risk, concentration and cash policy.

## Adding to winners
Adding to an appreciated position is allowed only when current V1.4 MOS meets required MOS, V1.5 and V2.0 gates permit addition, evidence confidence is adequate and all issuer/sector/theme caps have headroom. An upward price move can reduce MOS; revalidate instead of extrapolating price momentum.

## Adding to losers
A falling price triggers research, not automatic buying. Re-check:
1. Thesis and invalidators with current evidence.
2. V1.2 fundamentals and earnings quality.
3. V1.3 moat direction and disruption.
4. V1.4 current value, MOS and confidence.
5. V1.5 risk/decision and V2.0 position state.
6. Position/sector/theme headroom and cash reserve.
If a thesis is broken, V2.0 says REDUCE/EXIT, a material risk override applies or a cap is reached, do not add. Never average down merely to lower average cost.

## Cash reserve
Default reserve is 10% of portfolio NAV; user may configure a different percentage or RM floor. If both are set, preserve the larger required amount. Reserve target is measured after proposed allocation. Deployable cash = max(0, available cash − reserve target − known included costs). If cash already falls below reserve, suggested allocation is RM0 until the reserve is restored. Do not allocate more than available/deployable cash. State whether the reserve is a user mandate or a default assumption.

## Action mapping
Use V2.2 score and decision gates; V1.5/V2.0 gates outrank the numerical score.
- PRIORITY ACCUMULATE: 85+ and all stricter eligibility, valuation, risk, confidence, capacity and V1.5/V2.0 gates pass.
- ACCUMULATE: 70–<85 and all eligibility gates pass.
- HOLD: existing holding, thesis intact, V2.0 HOLD and no stronger override.
- WAIT FOR BETTER PRICE: thesis/quality may qualify, but price exceeds V1.4 buy-below/MOS threshold or V1.5 value classification is FAIRLY VALUED/OVERVALUED; no new cash now.
- WATCH: insufficient evidence, unconfirmed thesis/catalyst, or no qualified action.
- REDUCE: existing position and V1.5/V2.0/verified concentration or risk process calls for review/reduction; amount needs human judgment.
- DO NOT ADD: explicit new-money block from risk, valuation, capacity, cash or upstream decision. Not an automatic sell instruction.
When more than one applies, choose the more restrictive valid action and explain why.

## Current portfolio examples — verify every classification
The following tickers are user-provided examples for applying exposure look-through and risk controls. They are not permanent sector labels, fixed portfolio holdings or recommendations. Before assigning a bucket, verify issuer/security, current disclosed segments and portfolio ownership from dated Tier 1 evidence. If identity/exposure is uncertain, mark REQUIRES_VERIFICATION/N/A and do not count a guessed exposure.

| Example ticker | V2.2 portfolio rule to apply |
|---|---|
| IHH | Verify current healthcare/service/geographic exposures; aggregate only evidenced health-sector overlap with other holdings and do not double count controlled entities held directly. |
| GAMUDA | Review current project/order-book, construction/infrastructure, property and geographic exposures; stress common project-cycle and working-capital risks before adding to correlated holdings. |
| SUNREIT | Verify current REIT/property assets, tenant mix and gearing; count toward combined REIT/property limits using disclosed look-through only. |
| ECOSHOP | Verify current retail/customer/supplier exposures; test combined consumer/retail concentration with other relevant holdings rather than treating ticker diversification as sector diversification. |
| SUNMED | First verify the exact listed issuer, security code and reporting history from current Bursa records. If confirmed as healthcare exposure, aggregate only evidenced overlap with IHH; do not assume identity, group linkage or financial history. |
| TENAGA | Review current utility/regulatory, capex, financing, fuel/FX and transition exposure; count any AI/data-centre power theme only with sourced revenue/asset/project evidence. |
| CIMB | Verify current bank identity/data and include in combined bank, credit-cycle, rates and geographic exposure limits. |
| MAYBANK | Verify current bank identity/data and include in combined bank, credit-cycle, rates and geographic exposure limits; bank diversification does not remove shared systemic risk. |
| MRDIY | Verify current retail footprint, suppliers, inventory and currency exposure; aggregate evidence-based consumer/retail overlap with ECOSHOP or peers. |
| CLMT | Verify current REIT assets, leases, occupancy, gearing and distribution; aggregate with SUNREIT/AXREIT under the configured REIT limit, without assuming identical property risk. |
| AXREIT | Verify current assets, tenant/lease profile, gearing and distribution; include in REIT concentration and assess property/tenant overlap with other verified holdings. |
| YTL | Review the latest disclosed group structure and segment look-through. Count utilities/infrastructure/digital themes only by current evidence; avoid double counting separately held affiliates or projects. |
| SPTOTO | Verify current operating and regulatory exposures; treat as a concentrated issuer risk and review any correlated leisure/discretionary/regulatory exposure with GENTING separately. |
| GENTING | Verify current segment/geographic mix and leverage/capital commitments; review travel/leisure/gaming/regulatory cycle correlations, without assuming identical exposure to SPTOTO. |
| DNEX | Use latest verified segment and corporate-action disclosures to determine current exposures; do not rely on historical business labels or count an unverified subsidiary/theme exposure. |

Company labels are examples only. Classification can change when filings, listing status, group structures, business mixes or portfolio holdings change. This table adds no company score or permanent holding classification.

## Execution boundary
V2.2 does not perform automatic trade execution. Allocation amounts are estimates for human review only.

This framework does not permit automatic trade execution.
Automatic trade execution is not permitted.
