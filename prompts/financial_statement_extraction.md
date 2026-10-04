# Prompt: Financial Statement Extraction V1.8

Extract, but do not interpret beyond clearly labeled observations, from a supplied Malaysian listed-company annual or quarterly/interim report.

## Required metrics
Revenue, gross profit, EBITDA, EBIT, profit before tax, net profit, EPS, cash, total debt, net debt, operating cash flow, capital expenditure, free cash flow, total assets, total equity, ROE, ROIC and dividend. Include the metric definition and line item/statement location; if absent or not derivable from disclosed inputs, use MISSING/N/A.

## Extraction controls
- Create a separate record for each metric, period and basis using data/ingestion/financial_data_input.md.
- Capture company, Bursa ticker, source/document ID and URL, page/note/table, unit, currency, period start/end, fiscal year/quarter, extraction date, filing/audit/review status and verification status.
- Distinguish quarterly, YTD, annual and TTM; do not mix them or silently annualize.
- Preserve original and restated values, comparative as presented, continuing/discontinued operations and one-off/extraordinary items as separate records.
- Preserve negative values; check sign and denominator meaning.
- Calculated values show formula and all source inputs; do not assert a definition that the filing does not support.
- Estimates are never historical facts; mark ESTIMATED and identify assumptions.
- If exact source/location cannot be checked, mark REQUIRES_VERIFICATION.
- Never fabricate an amount or live market input; do not calculate V1.2 scores or V1.4 valuations.

## Output
Provide an extraction table, source metadata, evidence IDs, status, validation report, unresolved conflicts and missing-data list. Preserve the exact reported unit/currency and explain conversions separately.
