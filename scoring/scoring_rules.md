# Scoring Rules V1

## Shared method and rationale
This rubric allocates points to transparent, ordered performance bands. The numeric thresholds below are initial screening anchors, not universal laws or empirically guaranteed return predictors. They encode directional investor logic (durable growth, returns, cash generation, balance-sheet resilience, reasonable relative valuation, liquidity, supportive trend, and evidenced moat). Apply them consistently, disclose judgment, and calibrate only in a new documented version using Bursa history and sector cohorts. Never tune a threshold after seeing a desired issuer result.

For every metric retain: FACT (raw value/formula/source/period/unit); ANALYSIS (score band, rationale, peer/sector adjustment and warning); INFERENCE (what it may indicate and uncertainty); FORECAST (only if forward data are used). Mark unavailable or inapplicable inputs N/A and explain the lost weight. A valid adverse value scores zero; it is not N/A.

## A. Financial Quality — 50 points

### 1. Revenue Growth — 10
- Measures: compound annual growth in reported revenue over the latest 3–5 comparable fiscal years; show organic growth separately if disclosed.
- Why: sustained sales growth can indicate demand and scale, but acquisitions, FX, inflation, one-off contracts and low-base effects can mislead.
- Required data: consolidated revenue by comparable FY, restatement/acquisition notes, units, period lengths; source filings.
- Method/range: CAGR = (ending revenue / starting revenue)^(1/years) − 1 when both are positive and comparable. Score: ≤0% = 0; >0–3% = 2; >3–5% = 4; >5–10% = 6; >10–20% = 8; >20% = 10. These bands distinguish contraction/flat, modest, healthy and strong growth; >20% receives the cap because high growth often includes a low base or is harder to sustain.
- Interpretation: higher bands mean stronger historical growth, not a forecast.
- Warnings: negative starting revenue, acquisitions, changed segment perimeter, inflation-only growth, cyclic peak/trough, single contract, or sharp deceleration.
- Data quality: use audited annual consolidated values where possible; if only YTD/quarterly values exist, do not annualize a seasonal period as a full-year CAGR. If calculation is invalid, N/A.

### 2. EPS Growth — 10
- Measures: growth in basic EPS attributable to ordinary shareholders over comparable annual periods.
- Why: per-share earnings show whether owners’ earnings grew after dilution, but EPS may move due to one-offs or capital changes.
- Required data: basic EPS and weighted-average shares, comparable periods, attributable profit, restatements, splits/bonus issues/placements/rights issues.
- Method/range: calculate CAGR over 3–5 years only when starting and ending EPS are positive and comparable; apply the Revenue Growth bands (0, 2, 4, 6, 8, 10 for the same thresholds). If CAGR is not meaningful due to a loss or sign change, use latest audited normalized EPS trend only if a transparent comparable series can be built; otherwise N/A, not an invented CAGR.
- Interpretation: higher score indicates stronger per-share earnings growth.
- Warnings: diluted share issuance, volatile tax, disposal gains, exceptional items, negative EPS, changing weighted-average shares, or growth below revenue due to margin dilution.
- Data quality: cite issuer-reported EPS; do not compute from period-end shares. Disclose any normalization as ANALYSIS, not reported FACT.

### 3. Return on Equity (ROE) — 10
- Measures: profit attributable to owners divided by average owners’ equity, normally latest audited FY and 3-year context.
- Why: gauges accounting returns on shareholder capital; high leverage or a shrunken/negative equity base can inflate it.
- Required data: attributable profit, opening/closing attributable equity, audited reports, unusual items and equity changes.
- Method/range: ROE = attributable profit / average attributable equity. For positive, meaningful equity: ≤0% = 0; >0–5% = 2; >5–10% = 4; >10–15% = 6; >15–20% = 8; >20% = 10. Bands reward returns above a low single-digit level and cap exceptional readings pending quality checks; they are screening bands, not cost-of-equity estimates.
- Interpretation: higher sustainable ROE is favorable only when supported by earnings quality and adequate capital.
- Warnings: negative/thin equity, exceptional profits, large buybacks, high leverage, financial-sector accounting, or volatile equity. Cap at 4/10 when a one-off item materially drives ROE; explain the judgment. Negative equity makes the ratio N/A and triggers a risk flag, not a misleading numeric ratio.
- Data quality: prefer average balances; annualize interim data only with a stated method. For banks/insurers use sector capital/return interpretation and peer context.

### 4. Debt-to-Equity — 10
- Measures: interest-bearing borrowings divided by stated equity; show lease-inclusive and lease-exclusive values when material.
- Why: debt can magnify returns and downside, constrain dividends and increase refinancing sensitivity.
- Required data: current and non-current borrowings, lease liabilities, cash, equity, guarantees, debt notes, sector and maturity profile.
- Method/range, general non-financial-company anchor: ≤0.25x = 10; >0.25–0.50x = 8; >0.50–1.00x = 6; >1.00–1.50x = 4; >1.50–2.00x = 2; >2.00x = 0. The declining scale reflects rising fixed claims and less balance-sheet headroom; it is only a starting anchor.
- Interpretation: lower debt/equity generally gives more financial flexibility, but zero debt is not automatically optimal.
- Warnings: negative/thin equity, restricted cash, off-balance-sheet commitments, near-term maturities, floating rates, covenant concerns, guarantees, lease obligations. Negative equity: score 0 and flag; do not use the ratio mechanically. Do not award high points solely because cash temporarily exceeds borrowings.
- Data quality: define debt/equity consistently, use latest balance sheet and notes, disclose lease treatment. Banks/insurers and REITs use sector-specific leverage context; if the supplied ratio is not meaningful, N/A and reduce coverage. If peer-relative method replaces the anchor, document peer set and percentile.

### 5. Free Cash Flow — 10
- Measures: cash generation after reinvestment, using FCF = net cash from operating activities − cash purchases of PPE and intangible assets; state exclusions.
- Why: cash can fund debt service, dividends and growth; one-year FCF is volatile and investment cycles matter.
- Required data: comparable 5-year OCF, cash capex, acquisitions/capitalized development notes, business model.
- Method/range: count positive FCF years out of the latest five comparable FYs: 0/5 = 0; 1/5 = 2; 2/5 = 4; 3/5 = 6; 4/5 = 8; 5/5 = 10. Count is a transparent consistency measure, rather than rewarding one unusually large year. Also disclose cumulative FCF and latest year; negative FCF due to disclosed expansion is still negative under this metric, with context in ANALYSIS.
- Interpretation: more positive years suggest more consistent internal funding, not necessarily higher growth or return.
- Warnings: working-capital reversals, asset disposals, acquired assets, lease principal, capital creditors, project cycles, or suppressed maintenance capex.
- Data quality: reconcile cash capex and OCF from filings. Banks/insurers and other sectors where industrial FCF is unsuitable: N/A, explanation and reduced coverage; do not substitute earnings per share or dividends as FCF.

## B. Profitability & Valuation — 15 points

### 6. Gross Margin — 10
- Measures: gross profit / revenue, latest audited FY, with 3-year trend and sector-peer comparison.
- Why: reflects pricing, product mix and direct-cost economics; absolute margins vary widely by industry.
- Required data: comparable gross profit/revenue and a named Bursa/industry peer cohort or a documented company trend.
- Method/range: primary method is percentile among comparable peers (same industry, similar business model and period): top decile = 10; 70th–<90th percentile = 8; 40th–<70th = 6; 20th–<40th = 4; below 20th percentile but non-negative = 2; negative gross profit = 0. If no credible peer cohort, use the 3-year direction: material sustained expansion = 8; broadly stable = 6; sustained contraction = 4; severe contraction/negative = 0; explain measured change and do not imply false percentile precision.
- Interpretation: stronger/stable relative margins can indicate pricing or operating advantage, but are not proof of moat.
- Warnings: accounting classification differences, mix shifts, commodity cycles, utilization shocks and unsustainable price peaks.
- Data quality: use same definition and fiscal period across peers; N/A if gross profit is not disclosed or comparable.

### 7. P/E Valuation — 5
- Measures: price per share divided by comparable diluted EPS; report trailing P/E, or forward P/E explicitly as FORECAST.
- Why: relates equity price to earnings; a low multiple may be cheap or reflect deteriorating/peak earnings.
- Required data: dated Bursa share price, diluted EPS/earnings, shares, peer or own-history median, earnings normalization notes.
- Method/range: compare issuer P/E with a documented peer median or its own 5-year median using the same basis: ≤0.75x reference = 5; >0.75–0.90x = 4; >0.90–1.10x = 3; >1.10–1.30x = 2; >1.30x = 1. Zero if valid normalized earnings are negative or P/E is not meaningful; N/A if price/earnings inputs or a defensible reference are unavailable. Discount bands reward relative valuation headroom; they do not prove undervaluation.
- Interpretation: higher score means a lower relative P/E, not a price target.
- Warnings: cyclically peak profit, loss-making issuer, one-off gains, share-count mismatch, stale price, peer-quality differences and growth differences. Discuss quality/growth; do not let low P/E override worsening fundamentals.
- Data quality: record price date, source, trailing/forward definition, earnings period, diluted basis and reference cohort.

## C. Balance Sheet / Valuation — 10 points

### 8. P/B Valuation — 5
- Measures: market price/equity market value relative to latest reported book value per share/equity.
- Why: useful for asset-heavy and financial businesses, but book value may not equal realizable value or earning power.
- Required data: dated share price, shares, latest equity attributable to owners, intangibles/goodwill where relevant, peer or own-history P/B and ROE.
- Method/range: compare with documented peer or own 5-year median P/B on consistent basis: ≤0.75x reference = 5; >0.75–0.90x = 4; >0.90–1.10x = 3; >1.10–1.30x = 2; >1.30x = 1. Zero if equity is negative; N/A if inputs/reference are unavailable. If ROE is below a reasonable sector cost-of-equity proxy or falling sharply, cap score at 2 and explain; cheap book can be a value trap.
- Interpretation: higher score means lower relative price/book only; assess asset quality and sustainable ROE.
- Warnings: stale or impaired assets, goodwill, negative equity, revaluation reserves, capital structure and sector differences.
- Data quality: use attributable equity and diluted/current shares consistently; cite price date and peer reference.

### 9. Dividend Yield — 5
- Measures: cash dividend per share over a stated trailing 12-month or indicated annual basis divided by dated share price; label the basis.
- Why: measures cash income at the observed price, but yield can rise because price falls and may be unsustainable.
- Required data: declared/paid dividends and dates, price date, payout, cash flow, debt and sector peers.
- Method/range: compare sustainable trailing yield with a named sector-peer median or suitable dated benchmark: ≥1.50x = 5; 1.20–<1.50x = 4; 0.80–<1.20x = 3; 0.40–<0.80x = 2; >0–<0.40x or zero yield = 1; no sustainable dividend or unsustainable payout = 0. N/A if dividend/price/peer basis unavailable. The relative scale accommodates different sectors and rate environments; it is not an absolute yield target.
- Interpretation: higher score means stronger relative cash income only if supportable.
- Warnings: special dividends, proposed vs paid, earnings/cash deterioration, borrowing-funded distributions, REIT distribution rules and price decline.
- Data quality: cite each dividend and ex/payment status; show benchmark and price date. Do not call an announced dividend paid.

## D. Market / Technical — 15 points

### 10. Price Trend — 5
- Measures: dated price trend using close versus 50- and 200-trading-day moving averages and 6/12-month total return relative to FBMKLCI (or a stated sector benchmark).
- Why: describes market condition and momentum; it is not business value or a guaranteed predictor.
- Required data: corporate-action-adjusted daily prices, dividends for total return, date, benchmark series.
- Method/range: 5 = price above both averages and positive 6/12-month relative total return; 4 = above 200-day with at least one positive relative return; 3 = mixed/near averages or broadly in line with benchmark; 2 = below 200-day and negative relative return; 1 = below both averages with materially negative relative return; 0 = severe breakdown supported by stated rule (for example, >30% 12-month underperformance) or invalid/failed market data (prefer N/A for invalid data). For overlapping conditions, use the highest fully satisfied band and explain; report raw signals.
- Interpretation: higher score indicates stronger trend condition on analysis date only.
- Warnings: low liquidity, corporate actions, suspension, rights issue, short history, event gap, broad market regime.
- Data quality: adjusted prices and correctly aligned benchmark are required; otherwise N/A.

### 11. Trading Volume / Liquidity — 5
- Measures: ability to trade without dominating typical turnover; this rewards usable liquidity, not high activity for its own sake.
- Why: illiquidity raises execution costs and exit risk, especially on Bursa small caps.
- Required data: at least 60 sessions of daily traded value (prefer median), free float if used, and stated assumed order size.
- Method/range: let L = median daily traded value / intended single-day order value. Score: L ≥10 = 5; ≥5–<10 = 4; ≥2–<5 = 3; ≥1–<2 = 2; >0–<1 = 1; no regular trading/zero volume = 0; missing series or no defensible order-size assumption = N/A. Bands limit intended order to ≤10%, 20%, 50%, or 100% of normal daily traded value as score declines; disclose that these are execution-risk guardrails, not return forecasts.
- Interpretation: higher score indicates more room for the assumed trade, not better fundamentals.
- Warnings: block trades, placement days, long no-trade runs, unusual spikes, free-float changes and price impact.
- Data quality: use median rather than mean to reduce spike distortion; state date window, currency and order-size assumption. Score changes if investor size changes.

### 12. Relative Strength Index (RSI) — 5
- Measures: 14-session RSI calculated from adjusted daily closing prices.
- Why: flags short-term momentum extremes; neutral conditions score best because overbought/oversold alone is not directional evidence.
- Required data: sufficient adjusted daily prices, calculation window, analysis date.
- Method/range: 45–65 = 5; 35–<45 or >65–70 = 4; 30–<35 or >70–75 = 3; ≤30 or >75 = 1. RSI is bounded 0–100; valid extreme readings remain scored, not N/A. Invalid/insufficient price history = N/A. Keep exact boundary definitions as written.
- Interpretation: score indicates technical balance, not intrinsic quality. RSI ≤30 may be oversold in a downtrend; >75 may indicate persistent momentum or overheating.
- Warnings: strong trends can stay extreme, low-volume prices distort signals, price gaps/corporate actions.
- Data quality: record formula convention (Wilder default), adjusted prices, sample window and date; use same convention across companies.

## E. Business Quality — 10 points

### 13. Industry Growth — 5
- Measures: sourced 3–5 year industry revenue/demand growth outlook, with historical context and relevant addressable market definition.
- Why: sector expansion can support company growth, but industry growth does not guarantee issuer share capture or profit.
- Required data: current primary/credible industry sources, defined geography/product scope, forecast period, growth basis and date.
- Method/range: use a cited nominal revenue/demand CAGR relevant to issuer: <0% = 0; 0–<2% = 1; 2–<5% = 2; 5–<10% = 3; 10–<15% = 4; ≥15% = 5. Rising bands recognize larger expected demand expansion; high growth earns full points only when the market definition/source is credible and not just a small-base projection. If source quality/scope is inadequate, N/A.
- Interpretation: indicates tailwind potential, not company forecast.
- Warnings: TAM hype, nominal inflation, cyclical rebound, policy dependency, oversupply, capacity and market-share shifts.
- Data quality: name the source/date, forecast horizon, geography and methodology; corroborate forecasts where feasible.

### 14. Competitive Moat — 5
- Measures: evidence that durable advantages protect returns or customer demand, such as cost advantage, switching costs, network effects, brand, distribution, licenses, IP or data.
- Why: durable advantage may support margins and returns through competition; a good product or management claim alone does not prove a moat.
- Required data: several years of margin/ROE/customer retention evidence where available, market/customer information, competitor comparison, contracts/IP/license disclosures and reinvestment needs.
- Method/range: evidence-based analyst rubric: 0 = no evidence or advantage clearly eroding; 1 = claimed or isolated advantage with little independent support; 2 = some observable differentiation but limited breadth/durability; 3 = established advantage with mixed durability evidence; 4 = multiple corroborating sources and durable economics versus peers; 5 = unusually durable, independently corroborated advantage with sustained economic evidence and credible barriers to replication. Score is ordinal; explain each point and evidence. N/A only when evidence is too sparse to assess, not merely because moat is weak.
- Interpretation: higher score means stronger documented durability, not certainty.
- Warnings: customer concentration, expiring licenses, subsidies, patents near expiry, rapid technological change, low switching costs, returns below peers, unsupported management claims.
- Data quality: cite multi-period primary evidence and competitor basis; mark unverified market share as unavailable.

## Shared sector adjustment and automation record
A sector adjustment must explain which baseline is unsuitable, give the replacement definition, peer cohort, period and rationale, and retain raw data. Do not alter metric weights or an individual score’s maximum. Unavailable/inapplicable inputs use N/A and reduce coverage. Keep stable metric IDs: revenue_growth, eps_growth, roe, debt_to_equity, free_cash_flow, gross_margin, pe, pb, dividend_yield, price_trend, trading_volume, rsi_14, industry_growth, competitive_moat.
