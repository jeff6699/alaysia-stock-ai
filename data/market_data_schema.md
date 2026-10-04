# Market Data Schema V1.7

## Purpose
Define date-sensitive market observations used in company research and valuation. This schema supplements V1.4 and does not change valuation formulas, score weights, technical indicators or decision rules.

## Market observation fields
| Field | Required detail |
|---|---|
| company_name / bursa_ticker | Issuer identity, Bursa security code and share class |
| observation_type | Share price, trading volume, market cap, shares outstanding, FX, benchmark/peer price, corporate action or other defined market item |
| value / status | Value and AVAILABLE / MISSING / ESTIMATED / NOT APPLICABLE |
| currency / unit | Explicit currency, RM/sen per share, shares, lots, turnover or other unit |
| observation_date_time | Market date/time and timezone where available |
| source_id | Evidence ID with source locator |
| price_basis | Close/open/intraday/VWAP/adjusted/unadjusted, exchange and any corporate-action treatment |
| shares_basis | Issued, treasury-adjusted, basic, diluted or other definition |
| calculation | Formula and input IDs for market capitalization or enterprise value |
| adjustment_notes | Splits, consolidation, rights, bonus issue, dividend, suspension or other action |
| collected_at / quality_flag | Retrieval date and validation notes |

## Core market fields
- Current share price: exact price, Bursa source/vendor, date/time, trading status, currency and adjusted/unadjusted basis. Do not call stale price current.
- Trading volume and turnover: date/period, shares/lots convention, unit conversion and data source.
- Shares outstanding: class and date; reconcile treasury shares, issued shares, diluted shares, options and other potential dilution.
- Market capitalization: identify formula and basis (price × defined shares), with date and currency; reproduce issuer/vendor value separately if definitions differ.
- Enterprise value: state EV bridge (market capitalization + included debt/leases/preferred claims/NCI − included cash and other adjustments), date, currency and each sourced component.
- Corporate actions: event/ex/record/payment dates and adjusted price/share series source. Preserve original raw prices.

## Quality and use
Market information is time-sensitive. Store collection time, market close and data vendor/source; identify holidays, stale observations, suspensions, illiquid trading or price limits where relevant. Do not silently forward-fill a stale price. Currency conversion requires a sourced FX rate and timestamp. Reconcile current price and share basis with V1.4 valuation output before computing returns or margin of safety; otherwise mark the affected output N/A and lower confidence.

Technical metrics such as RSI, price trend or trading volume indicators must use their existing score-module definitions, lookback, data source and date. This schema does not define new technical scoring rules.

## Evidence labels and missing data
- FACT: directly source-supported observation or reproducible calculation with its inputs and formula.
- ANALYSIS: interpretation of verified facts with method and limitations.
- INFERENCE: qualified conclusion derived from evidence, including uncertainty and alternatives.
- FORECAST: conditional forward view with horizon and explicitly identified ASSUMPTIONS.
Missing evidence is MISSING and displayed as N/A with its downstream effect; do not fabricate or silently substitute a value.
