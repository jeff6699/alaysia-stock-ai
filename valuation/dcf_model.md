# Discounted Cash Flow Model

## Scope
Use DCF when operating cash flows and reinvestment can be forecast with defensible data. For banks/insurers, industrial FCFF is usually unsuitable; consider P/B, DDM or sector FCFE with capital constraints.
Historical values are FACTS with source, period, units and filing status. All projections and analyst-selected inputs are ASSUMPTIONS. Missing data = N/A, never invented.

## Forecast horizon and revenue
Select and justify a forecast period, typically 5–10 years depending on maturity and visibility. Use longer explicit forecasts if required to reach mature economics.
Revenue_t = Revenue_(t−1) × (1 + growth_t).
ASSUMPTION: annual growth from disclosed history, capacity, order book, demand, pricing, mix, FX, competition and sector evidence. Reconcile acquisitions/disposals and inflation versus volume; do not extrapolate seasonal quarters mechanically.

## Margin, tax and reinvestment
EBIT_t = Revenue_t × operating margin_t. NOPAT_t = EBIT_t × (1 − tax rate_t).
ASSUMPTION: margin path and normalized cash tax, including incentives, loss positions, one-offs and convergence to maturity.
Operating NWC = operating current assets less non-interest-bearing operating current liabilities, excluding cash and financing debt. Change in NWC = NWC_t − NWC_(t−1); an increase is cash use.
ASSUMPTION: D&A based on asset base/useful lives and new investment; cash capex, separating maintenance/growth only with evidence; NWC levels and changes.
FCFF = NOPAT + D&A − capex − change in NWC.
Show annual revenue/growth/margin/EBIT/tax/NOPAT/D&A/capex/NWC/change/FCFF with consistent currency and units.

## WACC
WACC = E/(D+E) × cost of equity + D/(D+E) × cost of debt × (1 − tax rate), using consistent market-value or justified target capital weights.
Cost of equity may use CAPM = risk-free rate + beta × equity risk premium, with any country/size premium separately supported. Cost of debt reflects normalized borrowing cost/credit risk. Cite observed inputs as FACT; selected beta window, premiums, capital weights and normalized rates are ASSUMPTIONS with rationale. Do not insert an unsourced “standard Malaysia WACC.”
Use nominal MYR cash flows with nominal MYR WACC. Model risk in cash flows or rate consistently; avoid double-counting.

## Terminal value and equity bridge
TV_n = FCFF_n × (1 + g)/(WACC − g). Require WACC > g. ASSUMPTION: terminal growth consistent with long-run economics; show sensitivity. PV(TV) = TV_n/(1+WACC)^n.
EV = Σ[FCFF_t/(1+WACC)^t] + PV(TV).
Equity value = EV − interest-bearing debt − included leases − preferred claims − NCI + non-operating assets/excess cash not already included. State adjustments and avoid double deductions. Fair value/share = equity / diluted shares.
For FCFE, value equity directly and do not subtract net debt again.

## Scenarios and sensitivity
Run BEAR/BASE/BULL with revenue growth, margin, tax, capex, D&A, NWC, FCF, WACC, terminal growth, period and fair value. All drivers are ASSUMPTIONS; outputs are FORECASTS. Normally Bear growth/margin/FCF lower, WACC higher, g lower; Bull reverses.
Show WACC versus terminal-growth sensitivity plus key growth/margin sensitivities. Disclose terminal value as a share of DCF EV.
If WACC ≤ g, terminal value is N/A and DCF must not use the invalid Gordon result.
