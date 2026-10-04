# Data Quality Rules V1.7

## General rule
Keep source observations intact and store transformations separately. Every value must include status, unit, currency where relevant, period/date, basis and evidence ID or calculation lineage. Never invent missing values. Apply these checks before mapping data into V1.2–V1.6.

## Status handling
- AVAILABLE: source-supported observation or reproducible calculation with cited inputs.
- MISSING: unavailable, conflicting beyond resolution, or unsupported. Value stays blank/N/A; state collection attempts and downstream impact.
- ESTIMATED: explicit estimate/forecast with method, assumptions, evidence inputs, horizon and uncertainty. Do not blend it into reported FACT data.
- NOT APPLICABLE: metric is not meaningful for this business model, with reason. Not a workaround for missing evidence.
- Zero is not missing. Negative values are valid only when the underlying source and metric definition support them.

## Validation checks
| Issue | Required handling |
|---|---|
| Missing values | Mark MISSING and N/A in reports; name missing period/source and affected calculations, coverage and confidence. Never substitute zero or silently normalize. |
| Conflicting data | Compare source priority, scope, period, unit, filing status and restatement. Preserve both records and conflict; resolve to an authoritative value only with reason. If unresolved, mark MISSING/CONFLICT for decision use. |
| Different reporting periods | Keep dates and period_type explicit. Compare like-for-like fiscal periods; disclose calendar mismatch, seasonality and duration. No silent annualization or period mixing. |
| Currency differences | Preserve source currency. Converted values are separate derived records with sourced FX rate, date/time, convention and formula. |
| Restated statements | Keep original and restated observations with version/date. Use the latest authoritative filing for current analysis and label restatement; historical reports remain auditable. |
| One-off items | Preserve reported value; separately identify disclosed non-recurring items and any analyst adjustment, with source, rationale and ASSUMPTION label if judgmental. Do not silently normalize earnings. |
| Negative values | Preserve supported negatives. Review denominator and sign interpretation for growth, EPS, margins, equity, cash flow and valuation ratios; avoid invalid percentage calculations and mark N/A where needed. |
| Unit inconsistencies | Record source unit, convert only through explicit arithmetic, and retain both values/lineage. Check RM, RM’000, RM million, sen/share, shares/lots and scaling. |
| Historical vs current | Tag each reporting period and observation date. Do not label stale market, ownership, segment or macro data as current. State latest usable date and refresh gap. |
| Source conflicts | Apply research/evidence/source_priority.md and source quality rules. Cite all material conflicting sources, choose by authority and exact scope, or leave unresolved/N/A. |

## Additional financial checks
Reconcile statements and notes where possible. Check arithmetic totals, reported versus derived values, basic versus diluted EPS, period length, consolidation basis, segment eliminations, cash-flow classification, share changes, corporate actions and debt/cash definitions. Flag large profit/operating-cash-flow divergence, unusual receivables/inventory, capitalization, provisions, related parties and subsequent events for investigation, not as proof of misconduct.

## Release gate
Do not pass a metric downstream when identity, period, currency, unit or definition is unresolved. Mark affected output N/A and explain confidence/decision impact. Keep raw source, record ID, calculation, reviewer and review date so results can be reproduced. Validation flags do not change any V1.2–V1.6 score or threshold.

## Evidence labels and missing data
- FACT: directly source-supported observation or reproducible calculation with its inputs and formula.
- ANALYSIS: interpretation of verified facts with method and limitations.
- INFERENCE: qualified conclusion derived from evidence, including uncertainty and alternatives.
- FORECAST: conditional forward view with horizon and explicitly identified ASSUMPTIONS.
Missing evidence is MISSING and displayed as N/A with its downstream effect; do not fabricate or silently substitute a value.
