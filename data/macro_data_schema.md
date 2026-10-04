# Macro Data Schema V1.7

## Purpose
Provide dated, traceable Malaysian and relevant external macroeconomic context for company research. Macro inputs are not automatically company forecasts, and this schema does not alter scoring or valuation methods.

## Macro observation record
Each record includes:
- indicator_id and display name
- geography/economy and statistical agency
- value and status: AVAILABLE / MISSING / ESTIMATED / NOT APPLICABLE
- unit, currency, seasonal adjustment and definition
- reference period start/end and publication/revision date
- source ID, URL/table/series code and collection date
- original vs revised value and revision history
- FACT / ANALYSIS / INFERENCE / FORECAST label
- transformation, calculation or model if derived
- quality flags, limitations and comparability notes

## Possible indicators (select only when relevant and sourced)
Malaysian real GDP, industrial production, CPI/inflation, policy/market interest rates, unemployment/labor, MYR exchange rates, exports/imports, commodity prices, fiscal/regulatory changes and official sector indicators. External indicators may include trading-partner growth, global interest rates or relevant commodity benchmarks.

## Rules
Use the original agency definition and release period. Distinguish reference period from publication date and revision date. Preserve vintages where revisions affect historical analysis. Record nominal/real basis, seasonally adjusted status, index base, units and frequency. Do not combine series with different bases without an explicit transformation.

For comparisons and forecasts, cite the series, source/date and calculation. A macro FACT is evidence of the published indicator, not proof of a causal company impact. Explain the company transmission path as ANALYSIS and mark the expected future effect as INFERENCE or FORECAST with ASSUMPTIONS. If an indicator is unavailable, write N/A; do not fill from memory or an unverified source.
