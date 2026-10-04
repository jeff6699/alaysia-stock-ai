# V2.2 Portfolio Capital Allocation Report

**Run date:** 5 October 2026 (Asia/Kuala_Lumpur)  
**Decision-support only:** No trade was executed or order quantity generated.

## A. Portfolio Snapshot

- **FACT:** User supplied 15 lines of holdings and RM10,000 of new capital.
- **FACT:** Latest quote data retrievable for this run is dated 25 September to 2 October 2026, depending on source. Quotes are not synchronous; two prices are older than 2 October.
- **FACT:** Repository review found V2.2 rules and upstream V1.2–V2.1 framework documents, but no holding-specific company scorecards, valuations, decision outputs, or V2.0 portfolio decisions to reuse.
- **FACT:** User entry for SUNMED uses Bursa code 5218. Code 5218 identifies Vantris Energy Berhad (formerly Sapura Energy); Sunway Healthcare Holdings / SUNMED is code 5555. The reported 820 shares and RM1.697 cost therefore cannot be safely attributed to either company pending confirmation.
- **ANALYSIS:** V2.2 hard gates are not satisfied: individual score inputs and upstream decision outputs are missing; report-wide V2.2 component coverage is 0/100 validated points, below the 80% minimum; the 5218 identity is conflicted; and there is no common-date quote set. A numeric Capital Allocation Score would be misleading.
- **INFERENCE:** No holding qualifies for a defensible new-capital ranking or price zone in this run.
- **DECISION:** Allocate RM0 to shares; retain the full RM10,000 as cash pending verified inputs. This is not a sell recommendation.

## B. Current Portfolio Weight

### Method and data limits

**ASSUMPTION:** For an indicative mark only, provisional NAV is the quoted value of the 15 listed positions plus the RM10,000 new cash: RM57,941.70. This excludes any other cash, investments, liabilities, accrued fees, and taxes. It is not a verified total household or brokerage NAV. The portfolio weights below use this provisional denominator. The market-value snapshot mixes quote dates and is not suitable for a trade or valuation decision.

| Holding as supplied | Shares | Average cost (RM) | Latest quote used (RM; date) | Indicative market value (RM) | Provisional NAV weight | V2.2 action |
|---|---:|---:|---:|---:|---:|---|
| CIMB 1023 | 600 | 6.941 | 7.650; 2 Oct | 4,590.00 | 7.92% | WATCH |
| ECOSHOP 5337 | 5,000 | 1.344 | 1.480; 25 Sep | 7,400.00 | 12.77% | WATCH |
| GAMUDA 5398 | 800 | ~4.335 | 5.100; 2 Oct | 4,080.00 | 7.04% | WATCH |
| GENTING 3182 | 1,000 | 2.090 | 1.860; 2 Oct | 1,860.00 | 3.21% | WATCH |
| MAYBANK 1155 | 700 | 10.270 | 10.020; 2 Oct | 7,014.00 | 12.11% | WATCH |
| MRDIY 5296 | 5,000 | 1.692 | 1.270; 2 Oct | 6,350.00 | 10.96% | WATCH |
| SPTOTO 1562 | 1,000 | 1.450 | 1.260; 2 Oct | 1,260.00 | 2.17% | WATCH |
| “SUNMED” 5218 — identity conflict | 820 | 1.697 | 0.335; 2 Oct, code 5218 / Vantris | 274.70* | 0.47%* | WATCH |
| SUNREIT 5176 | 1,000 | 2.130 | 2.040; 2 Oct | 2,040.00 | 3.52% | WATCH |
| TENAGA 5347 | 600 | ~13.860 | 12.960; 2 Oct | 7,776.00 | 13.42% | WATCH |
| YTL 4677 | 300 | 2.220 | 2.240; 2 Oct | 672.00 | 1.16% | WATCH |
| AXREIT 5106 | 500 | 1.810 | 1.830; 2 Oct | 915.00 | 1.58% | WATCH |
| IHH 5225 | 200 | 7.710 | 7.800; 2 Oct | 1,560.00 | 2.69% | WATCH |
| CLMT 5180 | 2,000 | 0.555 | 0.560; 1 Oct | 1,120.00 | 1.93% | WATCH |
| DNEX 4456 | 2,000 | 0.480 | 0.515; 2 Oct** | 1,030.00 | 1.78% | WATCH |
| **Quoted holdings subtotal** |  |  |  | **47,941.70** | **82.74%** |  |
| **New cash** |  |  |  | **10,000.00** | **17.26%** |  |
| **Provisional NAV** |  |  |  | **57,941.70** | **100.00%** |  |

* The value is calculated against code 5218 solely to expose the mismatch; it is not confirmed to be the user's intended security.  
** The retrieved daily history displays RM0.5150 in the quote header and rounds its daily table close to RM0.52; RM0.5150 is used for arithmetic. Verify against an exchange/broker statement before relying on this value.

**FACT:** The quote for 5337 is the latest date found in its retrievable daily history (25 September); 5180 quote is 1 October. Other rows use 2 October quotes.  
**ANALYSIS:** Positions with the largest indicative value are TENAGA (13.42% of provisional NAV), ECOSHOP (12.77%), MAYBANK (12.11%), and MRDIY (10.96%). These weights are provisional because of mixed quote dates and incomplete NAV.  
**FACT:** Average cost is displayed for audit only.  
**ANALYSIS:** No add decision here is based on whether price is above or below average cost.

## C. Sector Concentration

Classifications are broad exposure groupings from market-data/company descriptions, not a verified look-through analysis. Weight uses provisional NAV, includes RM10,000 cash in the denominator, and excludes any other assets or liabilities.

| Exposure grouping | Holdings included | Indicative value (RM) | Provisional NAV weight | V2.2 default reference |
|---|---|---:|---:|---|
| Consumer products / services | ECOSHOP, MRDIY, GENTING, SPTOTO | 16,870.00 | 29.12% | 30% sector soft limit; near limit |
| Banks | CIMB, MAYBANK | 11,604.00 | 20.03% | 25% combined bank soft limit; 80% alert threshold reached |
| Utilities / multi-utilities | TENAGA, YTL | 8,448.00 | 14.58% | No combined default cap specified |
| REITs | SUNREIT, AXREIT, CLMT | 4,075.00 | 7.03% | 25% REIT soft limit |
| Construction | GAMUDA | 4,080.00 | 7.04% | 30% sector soft limit |
| Healthcare | IHH | 1,560.00 | 2.69% | 30% sector soft limit |
| Technology | DNEX | 1,030.00 | 1.78% | 30% sector soft limit |
| Energy | Code 5218, if position confirmed | 274.70 | 0.47% | Subject to identity confirmation |
| Cash | New capital retained | 10,000.00 | 17.26% | Minimum reserve default is 10% of provisional NAV |

- **FACT:** Consumer products/services exposure is approximately 29.12% and bank exposure approximately 20.03% on this provisional basis.
- **ANALYSIS:** Consumer exposure is close to the configurable 30% sector limit. Banks are at roughly 80% of the configurable 25% combined limit, which triggers the V2.2 alert threshold. These are portfolio-policy alerts, not universal investment rules.
- **ANALYSIS:** AI/data-centre look-through exposure is N/A; no verified company exposure mapping was present in the reviewed portfolio data. Do not infer it from a broad corporate relationship or news headline.
- **INFERENCE:** Adding to a consumer or bank holding before completing upstream research could bring the portfolio close to or above configured exposure limits. No sector cap conclusion is treated as exact while the full NAV and classifications remain unverified.

## D. V2.2 Capital Allocation Score for All 15 Stocks

V2.2 combines V1.2 Fundamental Quality (20), earnings/cash-flow quality (15), V1.3 AI Moat (10), V1.4 Valuation/MOS (20), V1.5 Risk (10), Portfolio Fit (15), V1.5 Catalysts (5), and integrated Data Confidence (5). Upstream outputs were not present in the repository for any holding.

| Ticker | Fundamental /20 | Earnings & cash flow /15 | AI moat /10 | Valuation & MOS /20 | Risk /10 | Portfolio fit /15 | Catalysts /5 | Data confidence /5 | V2.2 score / coverage |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---|
| CIMB | N/A | N/A | N/A | N/A | N/A | N/A | N/A | N/A | N/A; 0/100 validated |
| ECOSHOP | N/A | N/A | N/A | N/A | N/A | N/A | N/A | N/A | N/A; 0/100 validated |
| GAMUDA | N/A | N/A | N/A | N/A | N/A | N/A | N/A | N/A | N/A; 0/100 validated |
| GENTING | N/A | N/A | N/A | N/A | N/A | N/A | N/A | N/A | N/A; 0/100 validated |
| MAYBANK | N/A | N/A | N/A | N/A | N/A | N/A | N/A | N/A | N/A; 0/100 validated |
| MRDIY | N/A | N/A | N/A | N/A | N/A | N/A | N/A | N/A | N/A; 0/100 validated |
| SPTOTO | N/A | N/A | N/A | N/A | N/A | N/A | N/A | N/A | N/A; 0/100 validated |
| 5218 / supplied “SUNMED” | N/A | N/A | N/A | N/A | N/A | N/A | N/A | N/A | N/A; identity conflict |
| SUNREIT | N/A | N/A | N/A | N/A | N/A | N/A | N/A | N/A | N/A; 0/100 validated |
| TENAGA | N/A | N/A | N/A | N/A | N/A | N/A | N/A | N/A | N/A; 0/100 validated |
| YTL | N/A | N/A | N/A | N/A | N/A | N/A | N/A | N/A | N/A; 0/100 validated |
| AXREIT | N/A | N/A | N/A | N/A | N/A | N/A | N/A | N/A | N/A; 0/100 validated |
| IHH | N/A | N/A | N/A | N/A | N/A | N/A | N/A | N/A | N/A; 0/100 validated |
| CLMT | N/A | N/A | N/A | N/A | N/A | N/A | N/A | N/A | N/A; 0/100 validated |
| DNEX | N/A | N/A | N/A | N/A | N/A | N/A | N/A | N/A | N/A; 0/100 validated |

- **FACT:** Quote-derived market values and provisional weights are available as shown above; they are not V1.2–V2.1 outputs.
- **ANALYSIS:** The V2.2 score cannot be populated by substituting prices, broker targets, or a general impression for upstream V1.x/V2.x evidence.
- **DECISION:** Score = N/A, not zero. Assigning 0 would falsely imply that the companies were assessed and scored at the bottom of the scale.
- **Coverage:** 0/100 validated allocation-score points per holding. The required coverage gate is at least 80%; all candidates fail the gate.

## E. Ranked New-Capital Opportunities

| Rank | Candidate | V2.2 status | Score / coverage | Gate result | Amount eligible |
|---:|---|---|---|---|---:|
| — | All 15 holdings | WATCH | N/A / 0% validated | Missing upstream outputs; insufficient coverage; quotes/NAV not fully validated | RM0 |

No defensible ordering among the 15 can be made from the available evidence. The V2.2 ranking procedure first applies action gates and then ranks eligible candidates using their scores and valuation/concentration headroom. No candidate clears the prerequisite gates.

## F. Recommended RM10,000 Allocation

| Candidate | Current weight* | V2.2 action | Suggested amount | % of deployable cash | Maximum position weight | Main reason | Main risk / invalidator |
|---|---:|---|---:|---:|---|---|---|
| CIMB | 7.92% | WATCH | RM0 | 0% | N/A | V1.2–V2.1 outputs and current V1.4 valuation absent | Reconsider after a complete, sourced score/decision package and verified portfolio NAV |
| ECOSHOP | 12.77% | WATCH | RM0 | 0% | N/A | Consumer-sector concentration alert; V1.4 MOS and upstream outputs absent | Recheck identity, latest quote, valuation/MOS, consumer-sector exposure |
| GAMUDA | 7.04% | WATCH | RM0 | 0% | N/A | V1.2–V2.1 outputs absent | Reconsider after sourced score, decision, valuation and capex/risk review |
| GENTING | 3.21% | WATCH | RM0 | 0% | N/A | V1.2–V2.1 outputs absent | Reconsider after earnings normalization, risk and valuation review |
| MAYBANK | 12.11% | WATCH | RM0 | 0% | N/A | Combined bank exposure alert; upstream outputs absent | Recheck bank exposure, V1.4 value/MOS and V1.5/V2.0 actions |
| MRDIY | 10.96% | WATCH | RM0 | 0% | N/A | Consumer-sector concentration alert; upstream outputs absent | Recheck verified results, valuation/MOS and thesis |
| SPTOTO | 2.17% | WATCH | RM0 | 0% | N/A | V1.2–V2.1 outputs absent | Reconsider after sourced outlook, risk and valuation |
| 5218 / supplied “SUNMED” | 0.47%* | WATCH | RM0 | 0% | N/A | Company/ticker mismatch | Confirm whether the security is Vantris 5218 or SUNMED 5555 before analysis |
| SUNREIT | 3.52% | WATCH | RM0 | 0% | N/A | V1.2–V2.1 outputs absent | Reconsider after current valuation/MOS, leverage and decision review |
| TENAGA | 13.42% | WATCH | RM0 | 0% | N/A | Largest supplied holding; V1.2–V2.1 outputs absent | Reconsider after portfolio NAV, valuation/MOS and risk review |
| YTL | 1.16% | WATCH | RM0 | 0% | N/A | V1.2–V2.1 outputs absent | Reconsider after company-specific valuation and exposure mapping |
| AXREIT | 1.58% | WATCH | RM0 | 0% | N/A | V1.2–V2.1 outputs absent | Reconsider after current value/MOS, financing and upstream decision review |
| IHH | 2.69% | WATCH | RM0 | 0% | N/A | V1.2–V2.1 outputs absent | Reconsider after sourced valuation/MOS and risk review |
| CLMT | 1.93% | WATCH | RM0 | 0% | N/A | Quote is 1 October; upstream outputs absent | Refresh quote and complete V1.2–V2.1 outputs |
| DNEX | 1.78% | WATCH | RM0 | 0% | N/A | Upstream outputs absent; historical financial summary warrants primary-source verification | Recheck primary financial statements, loss/impairment normalization and V1.4 MOS |

* Based on provisional NAV and mixed quote dates; 5218 position label remains unconfirmed.  
**Total allocated:** RM0. **Withheld:** RM10,000. No trades or share quantities generated.

## G. Recommended Entry Price Zones

| Ticker | Current quote used | V1.4 preferred entry range | V1.4 MOS buy-below ceiling | Decision |
|---|---:|---|---|---|
| All 15, including 5218/SUNMED conflict | See Section B | N/A | N/A | No entry zone without a company-specific V1.4 valuation, required MOS, and synchronized current price |

An entry range is not inferred from average cost, recent lows, broker targets, or a price chart.

## H. Stocks Receiving RM0 New Capital and Why

All 15 receive RM0 because the V2.2 missing-data hard gate applies: no individual V1.2, V1.3, V1.4, V1.5, V2.0, and V2.1 outputs were available, and no candidate has the required ≥80% component coverage. The V2.2 rules require WATCH and RM0 when critical inputs or coverage are missing.

Additional holding-specific blockers include:

- **CIMB / MAYBANK:** combined bank concentration alert; no company-specific decision or valuation.
- **ECOSHOP / MRDIY:** combined consumer products/services exposure is near the configurable sector limit; no verified valuation/MOS.
- **TENAGA:** largest listed position in the supplied holdings subtotal; no verified target weight or position-class cap.
- **5218 / “SUNMED”:** incorrect or conflicting company identity must be resolved.
- **CLMT:** latest quote located is dated 1 October, not 2 October.
- **All others:** no basis to infer a score, risk rating, target weight, or entry zone.

These are no-add decisions for this run, not automatic reduce/sell instructions.

## I. Cash Reserve

- **Available new capital (FACT, user-provided):** RM10,000.
- **Reserve policy (FACT, V2.2 default):** 10% of portfolio NAV, configurable and not universal.
- **Provisional NAV (ASSUMPTION):** RM57,941.70 = RM47,941.70 indicative holdings + RM10,000 cash; other assets and liabilities excluded.
- **Provisional 10% reserve floor (calculation):** RM5,794.17.
- **Provisional deployable amount before candidate gates:** RM4,205.83.
- **Recommended allocation (ANALYSIS applying V2.2 gates):** RM0.
- **Cash retained:** RM10,000, approximately 17.26% of provisional NAV.
- **Reserve check:** Passes the 10% provisional floor by RM4,205.83.
- **Transaction costs:** Not deducted; no transaction is recommended.

## J. Portfolio Risks

| Risk | Evidence / status | Impact on this allocation run | Monitoring |
|---|---|---|---|
| Incomplete upstream decisions | No holding-level V1.2–V2.1 outputs found in reviewed repository data | Blocks all scoring/ranking/add decisions | Import or generate all sourced per-holding outputs before rerun |
| Consumer-sector concentration | Approximately 29.12% of provisional NAV across ECOSHOP, MRDIY, GENTING and SPTOTO | Near configurable 30% sector threshold | Review after each price move and earnings release |
| Bank concentration | Approximately 20.03% of provisional NAV in CIMB and MAYBANK; about 80% of default 25% limit | V2.2 concentration alert; no bank add can be cleared here | Recalculate from synchronized prices and full NAV |
| Largest single issuer / cap | TENAGA approximately 13.42% provisional NAV | Near the 15% default core cap, if core classification applies; classification and NAV not confirmed | Confirm position class, all assets/liabilities and policy cap |
| Stale/non-synchronous market data | Most recent accessible prices range 25 Sep–2 Oct | Provisional weights may differ from current weights | Refresh all holdings against one dated market close |
| Security identity conflict | “SUNMED 5218” conflicts with listed identity; SUNMED is 5555, code 5218 is Vantris | Market value and company-level research may refer to wrong asset | Confirm broker/CDS security name and ticker |
| Financial information not primary-verified | Market-data pages summarize results; no filing pages were attached to holding records | Fundamental and data-confidence scoring cannot be validated | Capture Bursa/issuer report, page, period, currency and units |
| Theme/sector look-through | No verified holdings map for indirect AI/data-centre exposure | Thematic concentration N/A | Validate material revenue/asset exposures from filings |

## K. What Could Change the Allocation

A rerun can produce a valid score and rank once the following are supplied or built as sourced holding-level records:

1. Confirm whether 820 units represent Vantris Energy 5218 or Sunway Healthcare / SUNMED 5555; provide the correct share count and cost basis for that security.
2. Provide a full portfolio NAV reconciliation: all cash, all holdings, other included assets, and liabilities. Confirm whether RM10,000 is the entire current available cash.
3. Refresh all 15 prices to the same market close and source date.
4. Populate per-company V1.2 score and coverage, V1.3 current moat/evolution score, V1.4 fair value/MOS/required MOS/confidence, V1.5 decision/risk/catalyst outputs, V2.0 action, and V2.1 report, each linked to its evidence.
5. Verify financial periods and material metrics against Bursa/company primary filings; update the V1.7 evidence records and mark unresolved items REQUIRES_VERIFICATION.
6. Confirm applicable position classes, position limits, investment horizon, and any cash-reserve override.

No single lower share price or loss relative to average cost would by itself change the outcome. V2.2 requires the upstream gates, valuation/MOS, risk, and portfolio-capacity evidence to pass together.

## L. Final V2.2 Decision

- **V2.2 actions:** WATCH for all 15 supplied holdings for this run; no candidate is eligible to be ranked for additions.
- **Capital Allocation Scores:** N/A for all 15; 0/100 validated allocation-score component coverage. This means unassessed, not a score of zero.
- **Suggested allocation:** RM0.
- **Cash retained:** RM10,000.
- **Top five eligible stocks for new capital:** None. The evidence and upstream-gate requirements are unmet, so a top-five investment ranking would be fabricated.
- **Stocks receiving no new capital:** CIMB, ECOSHOP, GAMUDA, GENTING, MAYBANK, MRDIY, SPTOTO, supplied “SUNMED” 5218, SUNREIT, TENAGA, YTL, AXREIT, IHH, CLMT and DNEX.
- **Main concentration risk:** Consumer products/services at approximately 29.12% of provisional NAV, close to the configurable 30% soft limit. Bank exposure is approximately 20.03% of provisional NAV, at the V2.2 80%-of-limit alert threshold. Both figures are provisional.
- **What capital is withheld for:** Resolving security identity, obtaining synchronized prices/full NAV, and completing traceable V1.2–V2.1 company-level analysis.
- **Human review required before any trade:** Yes. No automatic execution or order generation.

### FACT / ANALYSIS / INFERENCE / FORECAST register

- **FACT:** Share quantities, average costs, and RM10,000 new capital were supplied by the user. Quote observations and dates are linked in Sources.
- **ANALYSIS:** Provisional holding/sector weights use those quote observations and the stated NAV assumption; V2.2 gates fail due missing upstream outputs, coverage and identity/data issues.
- **INFERENCE:** Withholding the capital is the only action consistent with the existing V2.2 hard gates.
- **FORECAST:** None made. No future price, earnings, fair value, return, or entry range is forecast in this report.

### Sources

Market quotes are secondary market-data sources and are not substitutes for primary filings. Quote dates are stated per holding. Financial facts were not treated as verified V1.x scoring inputs in this run.

- S1 [CIMB 1023 quote and 2 Oct history](https://www.marketscreener.com/quote/stock/CIMB-GROUP-HOLDINGS-6491205/quotes/)
- S2 [ECOSHOP 5337 daily history](https://stockanalysis.com/quote/klse/ECOSHOP/history/) — latest retrieved row 25 Sep; source says updated 2 Oct.
- S3 [GAMUDA 5398 quote and 2 Oct history](https://www.marketscreener.com/quote/stock/GAMUDA-6491223/quotes/)
- S4 [GENTING 3182 quote and 2 Oct history](https://www.marketscreener.com/quote/stock/GENTING-6491224/quotes/)
- S5 [MAYBANK 1155 quote and 2 Oct history](https://www.marketscreener.com/quote/stock/MALAYAN-BANKING-6491196/quotes/)
- S6 [MRDIY 5296 quote and 2 Oct history](https://www.marketscreener.com/quote/stock/MR-D-I-Y-GROUP-M-119080216/quotes/)
- S7 [Sports Toto 1562 quote and 2 Oct history](https://www.marketscreener.com/quote/stock/BERJAYA-SPORTS-TOTO-6491166/quotes/)
- S8 [Bursa code 5218 / Vantris identity and quote history](https://www.marketscreener.com/quote/stock/SAPURA-ENERGY-12615775/company/)
- S9 [SUNREIT 5176 quote and 2 Oct history](https://www.marketscreener.com/quote/stock/SUNWAY-REAL-ESTATE-INVEST-6775441/quotes/)
- S10 [TENAGA 5347 quote](https://www.marketscreener.com/quote/stock/TENAGA-NASIONAL-6491357/)
- S11 [YTL 4677 quote and company page](https://www.marketscreener.com/quote/stock/YTL-CORPORATION-6491348/)
- S12 [AXREIT 5106 quote and 2 Oct history](https://www.marketscreener.com/quote/stock/AXIS-REAL-ESTATE-INVESTME-6497889/quotes/)
- S13 [IHH 5225 quote and 2 Oct close](https://www.marketscreener.com/quote/stock/IHH-HEALTHCARE-12684654/)
- S14 [CLMT 5180 quote and 1 Oct close](https://www.marketscreener.com/quote/stock/CAPITALAND-MALAYSIA-TRUST-6553980/company/)
- S15 [DNEX 4456 daily history](https://stockanalysis.com/quote/klse/DNEX/history/) — history table rounds close to RM0.52; quote header displays RM0.5150.
- [The Star Market Watch: SUNMED is 5555](https://www.thestar.com.my/Business/Marketwatch/Stocks?qcounter=SUNMED) and [Bursa code 5218 is Vantris Energy](https://www.thestar.com.my/Business/Marketwatch/Stocks?qcounter=VANTNRG).

### Disclaimer

This report is a decision-support estimate, not personalized financial advice, an order, or a trade instruction. No automatic trade execution is performed. Verify security identity, prices, source documents and assumptions independently before acting.
