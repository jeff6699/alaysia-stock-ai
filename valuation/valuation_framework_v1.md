# Multi-Method Valuation Framework V1

## Purpose and evidence
Estimate a fair-value range for Bursa Malaysia companies using suitable methods. Valuation is an estimate under assumptions, not a precise prediction. Do not force methods onto unsuitable businesses.
Keep these separate:
- FACT: sourced historical/market data, price date, period, currency/unit and formula inputs.
- ANALYSIS: method choice, normalization, comparison, reconciliation and interpretation.
- ASSUMPTION: every analyst-selected growth, margin, tax, capex, D&A, working capital, WACC/cost of equity, terminal growth, target multiple/yield, peer adjustment, scenario, blend weight and required MOS. Explain basis.
- INFERENCE: qualified conclusion, uncertainty and alternatives.
- FORECAST: modeled outputs derived from explicit ASSUMPTIONS, never facts.
Missing inputs = N/A with explanation. Never fabricate data, market price, peer values or model inputs.

## Bursa Malaysia setup
Record company/ticker/sector, analysis date, price date/source, reporting period, currency, units, consolidated/parent basis, filing status, fiscal year end, diluted shares, corporate actions and restatements. Prefer Bursa filings and issuer statements for financials. Reconcile RM/RM’000/RM million/sen/share units.
Keep cash-flow currency and discount-rate currency/inflation consistent (e.g. nominal MYR cash flows with nominal MYR WACC). Market-sensitive data must be dated.

## Method selection
Mark each Selected, Cross-check or N/A with a reason.

| Method | Use when | Caution / N/A when |
|---|---|---|
| DCF | Cash flows and reinvestment are forecastable | Financials, unstable/project cash flows, terminal value dominates |
| P/E | Positive normalized earnings and comparable capital structure | Loss, peak-cycle EPS, one-offs, leverage mismatch |
| EV/EBITDA | Comparable operating companies | Banks/insurers; EBITDA hides capex/working capital |
| PEG | Positive supportable medium-term EPS growth | Negative/volatile EPS or short-lived growth |
| P/B | Financials, asset-heavy firms, stable book/return economics | Impaired/stale book, negative equity, intangible-heavy |
| Dividend Yield / DDM | Mature sustainable distributers/REITs | Unstable payout, no dividend, debt-funded special dividend |
| FCF Yield | Mature cash generators with normalized FCF | Unstable/cyclical FCF, financial institutions |
| SOTP | Distinct segments/assets with separate supportable values | Weak disclosure, arbitrary multiples or double counting |

Adapt by sector: banks/insurers often use P/B, dividend/FCFE with capital constraints; industrial FCFF and EV/EBITDA may not apply. REITs need distribution, NAV and gearing context; developers/contractors need project timing; cyclicals need through-cycle inputs. State why requested methods are N/A.

## DCF formulas
For operating companies:
FCFF = EBIT × (1 − tax rate) + D&A − capex − change in operating NWC.
Enterprise value = PV(forecast FCFF) + PV(terminal value).
Gordon terminal value = final-year FCFF × (1 + g) / (WACC − g), requiring WACC > g.
Equity value = EV − debt − included lease liabilities − preferred claims − non-controlling interests + non-operating assets/excess cash not already included. Fair value/share = equity / diluted shares.
Use WACC for FCFF/EV; cost of equity for FCFE/equity dividends. Never subtract debt twice or mix FCFE with WACC. DCF must show revenue growth, operating margin, tax, capex, D&A, working capital, FCF, WACC, terminal growth and forecast period. All forward values are ASSUMPTIONS. See dcf_model.md.

## Relative method formulas
P/E price = normalized diluted EPS × justified P/E.
EV/EBITDA equity = normalized EBITDA × multiple − net debt/claims + non-operating assets; divide diluted shares.
PEG = P/E / EPS growth expressed in percentage points; no automatic PEG=1.
P/B price = sustainable BVPS × justified P/B; inspect asset quality and sustainable ROE.
Yield implied price = sustainable DPS / required yield; DDM discounts dividends at cost of equity.
FCF yield must pair FCFF with EV or FCFE with equity cap.
SOTP values segments suitably and reconciles debt, NCI, costs and shares once.
See relative_valuation.md.

## Blend, scenarios and MOS
Only blend comparable per-share equity values, never EV, yields, multiples or N/A. Explain each method’s ASSUMPTION weight and correlation; weights for included methods total 100%. If no method is usable, blended/base value is N/A.
Show BEAR/BASE/BULL revenue growth, margin, FCF, WACC, terminal growth, period and fair value. Normally Bear growth/margin/FCF lower, WACC higher, g lower, FV ≤ Base; Bull reverses. Explain justified exceptions. Upside/downside = (Base FV / current price) − 1. Current MOS = (Base FV − current price) / Base FV. Required MOS is separate ASSUMPTION. See scenario_valuation.md and margin_of_safety.md.

## Confidence
High: ≥3 relevant independent methods converge within 15% of blend and assumptions have evidence support.
Medium: ≥2 methods partly converge within 25%, but material uncertainty is bounded.
Low: methods diverge >25%, only one weak method applies, key data are N/A/unsupported, or earnings/cash flows are unstable.
Explain the rule applied; counting correlated methods does not increase confidence. These are process thresholds, not probabilities.

## Checks
- [ ] Price, diluted shares, periods, units, currency and EV/equity bridge align.
- [ ] Every analyst-selected input and blend weight is labeled ASSUMPTION.
- [ ] Unsuitable methods are N/A with impact stated.
- [ ] Debt, cash, leases and segments are not double-counted.
- [ ] Bear/Base/Bull order is checked or exceptions explained.
- [ ] Valuation is an estimate, not precise prediction or trade instruction.
