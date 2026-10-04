# Reporting Period Control V1.8

## Required period metadata
Every financial record must specify period start/end, fiscal year, fiscal quarter (or N/A), period type (annual, quarter, year-to-date, TTM, point-in-time or forecast), duration, publication date, source report, audit/review status, consolidation basis and currency/unit. Market observations use an observation date/time and explicitly mark fiscal period fields N/A. Macroeconomic and industry data use reference period and release/revision dates.

## Prohibited mixing and required safeguards
- **Quarterly with annual:** Never add, compare or substitute a quarter, YTD, TTM and full-year value without an explicit bridge and compatible duration. Do not label interim data annual.
- **Different fiscal years:** Align fiscal-year end and exact periods for peers/time series. State calendar mismatch and seasonality; do not treat same year labels as same coverage.
- **Stale market data:** Label old price/share/volume data STALE with observation date and age. Do not call it current or calculate a current MOS/return from it without qualification.
- **Different currencies:** Preserve original currency. Convert only with sourced FX rate, rate date/time and formula in a separate record.
- **Restated and original figures:** Preserve both versions; link restatement/correction and explicitly identify which record is selected for which comparison. Never combine original in one period with restated comparative without disclosure.
- **Estimates and history:** Estimates belong to forecast/scenario records with assumptions and horizon. Never present them as historical actuals or merge with reported history.
- **Continuing/discontinued operations:** Keep scopes distinct; reconcile total only with disclosed figures and formula.
- **Share basis/corporate actions:** Record basic/diluted and action-adjusted share basis with event metadata; do not silently rebase historical EPS, per-share price or shares.
- **Quarter fiscal labels:** Specify quarter end and covered start/end; when source provides YTD values, mark YTD and derive a discrete quarter only with formula from comparable same-basis periods.
- **Point-in-time metrics:** Balance-sheet and market data represent dates, not flows over a period. Do not sum them across quarters.

## Comparability gate
Before calculating a growth rate, margin, return ratio, valuation multiple or score input, confirm identity, period length, accounting scope, currency, units, definition and restatement basis. If a mismatch is unresolved, mark the derived item CONFLICT or REQUIRES_VERIFICATION and do not use it as a verified input. Any justified normalization must retain source values, conversion method and resulting record ID.

## Currentness and refresh
Record a cut-off date for the report and list each data domain's latest source date. Refresh price-sensitive data at the valuation date; refresh financials when a new filing is available. Do not overwrite prior snapshots. When a report uses older but still relevant history, label its age and why it remains relevant.
