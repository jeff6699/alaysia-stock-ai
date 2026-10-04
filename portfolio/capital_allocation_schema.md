# Capital Allocation Schema V2.2

## Record conventions
Use one run-level portfolio record and one candidate/allocation record per ticker. Values are date-stamped and source-linked. Monetary values include currency; weights/percentages state denominator (portfolio NAV, current portfolio or deployable new cash). Preserve user inputs, calculated values and upstream outputs separately. Missing = N/A; unverified = REQUIRES_VERIFICATION; conflict = CONFLICT. Do not fabricate data.

## Run-level schema
| Field | Type / unit | Required | Definition / validation |
|---|---|---|---|
| run_id | text | Yes | Unique immutable run identifier |
| timestamp | ISO date-time + timezone | Yes | Calculation time; distinguish from market data date |
| portfolio_as_of | date | Yes | Common valuation date for holdings |
| available_cash | currency amount | Yes | Verified or user-supplied cash and source/as-of; no negative inferred cash |
| minimum_cash_reserve | currency amount and/or % NAV | Yes | Configured floor/default; source as user policy/ASSUMPTION |
| current_portfolio_value | currency amount | Yes | Dated holdings + cash + other included assets − liabilities; basis stated |
| target_investment_horizon | text/duration | Yes | User objective; N/A if not provided |
| data_sources | array | Yes | Source IDs, URLs/documents, dates, locators, tiers/quality |
| confidence | HIGH / MEDIUM / LOW / N/A | Yes | Qualitative research/data confidence, rationale and source |
| currency | ISO code | Yes | Reporting currency; conversions retain FX sources |

## Per-holding / candidate schema
| Field | Type / unit | Required | Definition / validation |
|---|---|---|---|
| company_name | text | Yes | Verified company or N/A |
| ticker | text | Yes | Bursa ticker/security class |
| shares | number / shares | Yes | Dated quantity, user/broker record source or N/A |
| average_cost | currency/share | Optional | Informational only; never triggers a buy |
| current_price | currency/share + date | Yes for sizing | Timestamped current quote; no stale quote labeled current |
| current_market_value | currency | Yes for sizing | Dated holding value; reconcile shares × price |
| current_weight | % of NAV | Yes for sizing | Current market value / stated NAV |
| target_weight | % of NAV | Configurable | Intended target; must be ≤ maximum_weight |
| maximum_weight | % of NAV | Yes | Position class/user cap |
| fundamental_score | 0–100 / coverage | Required for standard score | V1.2 unchanged output, source/version |
| moat_score | 0–100 / coverage | Required for standard score | V1.3 final composite, source/version |
| valuation | object | Required for adding | V1.4 price/FVs/MOS/required MOS/confidence/date |
| investment_decision | enum | Required | V1.5 classification with gates/overrides |
| portfolio_decision | enum | Required | V2.0 ACCUMULATE/HOLD/WATCH/REDUCE/EXIT |
| risk_level | enum / N/A | Required | V1.5 overall rating and evidence |
| concentration_exposure | object | Required | Issuer/sector/bank/REIT/theme current and post-allocation weights, source/basis |
| allocation_score | 0–100 / earned / available / coverage | Required if calculable | V2.2 score; weights and missing components |
| allocation_action | enum | Required | V2.2 action classification |
| suggested_amount | currency | Required | Budget, not order/trade instruction |
| suggested_percentage | % deployable new cash | Required | Suggested amount / deployable new cash; N/A if denominator invalid/zero |
| entry_range | currency/share bounds + basis/date | Required | V1.4-supported range or N/A; no invented lower bound |
| reasons | list | Required | Sourced evidence IDs + rationale |
| risks | list | Required | V1.5 risk IDs/levels/probabilities/impact/source |
| invalidation_conditions | list | Required | Observable thesis/capital-allocation falsifiers and source/signal |
| data_sources | array | Required | Evidence IDs/source docs for every factual input |
| status | AVAILABLE / MISSING / N/A / ESTIMATED / CONFLICT / REQUIRES_VERIFICATION | Required | V1.8-compatible status per field |
| notes | text | Required | Unit, currency, period, assumption, calculation, limitations |

## Enumerations and guardrails
- allocation_action: PRIORITY ACCUMULATE / ACCUMULATE / HOLD / WAIT FOR BETTER PRICE / WATCH / REDUCE / DO NOT ADD.
- confidence: HIGH / MEDIUM / LOW / N/A.
- Amounts must satisfy: sum(suggested_amount) ≤ deployable cash; post-allocation cash ≥ minimum reserve; post-weight ≤ all applicable caps.
- An invalid or missing critical value blocks a standard positive allocation. Do not replace upstream missing scores with estimates.
- Weight denominator, time, source and data status accompany each calculated value.

## Execution boundary
Suggested amounts are not orders; this schema contains no automatic trade execution instruction.
