# Company Data Schema V1.7

## Purpose
Define a reusable, source-linked data record that feeds the V1.2–V1.6 research modules. This is a documentation schema, not an application or a new scoring methodology. Use one record per company, metric and reporting/observation period. Never invent a missing value.

## Required record envelope
Every field must carry its value and its status. Use:
- AVAILABLE — directly reported or reproducibly calculated from cited inputs.
- MISSING — expected or requested, but no sufficiently reliable value is available.
- ESTIMATED — an explicitly modeled/estimated value with method, input evidence, assumption, author/date and uncertainty. This is not a substitute for missing reported facts.
- NOT APPLICABLE — the field is not meaningful for this issuer/business model, with rationale.

Suggested record shape (human-readable or future structured implementation):
| Attribute | Required content |
|---|---|
| company_name | Issuer’s sourced legal/common name |
| bursa_ticker | Bursa Malaysia code; preserve the exchange identifier |
| sector | Sector label and classification source/date |
| industry | Industry label and classification source/date |
| metric_id | Stable field identifier from this schema |
| value | Numeric or text value; blank/N/A when status is MISSING or NOT APPLICABLE |
| status | AVAILABLE / MISSING / ESTIMATED / NOT APPLICABLE |
| unit | RM, RM’000, RM million, sen/share, shares, %, times, date, or explicit unit |
| currency | ISO currency code where monetary |
| period_start / period_end | Exact reporting period; observation date for point-in-time fields |
| period_type | Annual, interim, quarter, trailing twelve months, point-in-time, or forecast horizon |
| basis | Consolidated/parent, basic/diluted, gross/net, definition and other relevant basis |
| source_ids | One or more evidence IDs from research/evidence/evidence_schema.md |
| calculation | Formula and input metric IDs, if derived |
| quality_flag | Reconciliation, restatement, estimate, uncertainty or other validation note |
| as_of / collected_at | Observation date and collection date |

## Standard company and financial fields
| Metric ID | Display name | Typical unit / period |
|---|---|---|
| company_name | Company name | Text / point-in-time |
| bursa_ticker | Bursa ticker | Text / point-in-time |
| sector | Sector | Text / point-in-time |
| industry | Industry | Text / point-in-time |
| revenue | Revenue | Reporting currency / reporting period |
| ebitda | EBITDA | Reporting currency / reporting period |
| ebit | EBIT / operating profit as defined | Reporting currency / reporting period |
| net_profit | Net profit attributable to owners; identify if another basis | Reporting currency / reporting period |
| eps | EPS; distinguish basic/diluted and currency unit | Currency/share / reporting period |
| gross_margin | Gross profit / revenue with definition | Percent / reporting period |
| operating_margin | Operating profit / revenue with definition | Percent / reporting period |
| roe | ROE with numerator and equity basis | Percent / reporting period |
| roic | ROIC with NOPAT and invested-capital definition | Percent / reporting period |
| total_debt | Borrowings and included leases stated separately | Reporting currency / period-end |
| net_debt | Debt less included cash, with definition | Reporting currency / period-end |
| cash | Cash and equivalents; disclose restricted cash treatment | Reporting currency / period-end |
| operating_cash_flow | Net cash from operating activities | Reporting currency / reporting period |
| capex | Cash capex and/or additions, clearly distinguished | Reporting currency / reporting period |
| free_cash_flow | FCF with explicit convention and calculation | Reporting currency / reporting period |
| dividend | Dividend per share and/or total cash paid; identify status | Currency/share or reporting currency / date/period |
| shares_outstanding | Shares issued/outstanding; basic/diluted basis and date | Shares / point-in-time |
| current_share_price | Closing/observed price, venue, timestamp and source | Currency/share / observation date/time |
| market_capitalization | Market cap with share count/price basis and formula/source | Reporting currency / observation date |
| enterprise_value | EV with debt, cash, leases, NCI and other bridge items | Reporting currency / observation date |

Additional entity metadata such as reporting_period, fiscal year end, listing board, reporting currency, consolidation basis and source coverage should be stored in the record envelope. Sector-specific metrics may be added without changing these stable identifiers.

## Status semantics and missingness
- AVAILABLE: include the source ID, period, unit, definition and any calculation. If the value is a reproducible calculation, mark it as a calculated observation and retain all inputs/formula.
- MISSING: do not put a guessed value in value. State why it is unavailable, which source was checked and which downstream analyses are limited.
- ESTIMATED: identify it as an estimate wherever displayed; provide method, assumption IDs, source IDs, horizon, range/sensitivity if supportable and confidence. A forecast is ESTIMATED only as a modeled output, not a historical fact.
- NOT APPLICABLE: leave numeric value blank and explain why the metric is not meaningful for this issuer; do not use it merely because collection was difficult.
- Zero is a valid AVAILABLE value only when supported; it is distinct from MISSING.

## Conventions
Record original reported units and currency. Any normalized/conversion value is a separate derived record linked to original evidence, with FX rate/source/date or unit conversion formula. Never overwrite the reported value.

Use exact start/end dates, including quarter duration. Mark comparative restatements and fiscal-calendar changes. For current price, market cap and EV, retain timestamp/date and corporate-action/share basis. Do not mix historical statement values with current market values without labeling the periods.

For detailed validation see data_quality_rules.md. Financial definitions are in financial_data_schema.md; market and macro conventions are in market_data_schema.md and macro_data_schema.md.

## Evidence labels and missing data
- FACT: directly source-supported observation or reproducible calculation with its inputs and formula.
- ANALYSIS: interpretation of verified facts with method and limitations.
- INFERENCE: qualified conclusion derived from evidence, including uncertainty and alternatives.
- FORECAST: conditional forward view with horizon and explicitly identified ASSUMPTIONS.
Missing evidence is MISSING and displayed as N/A with its downstream effect; do not fabricate or silently substitute a value.
