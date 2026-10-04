# Prompt: Company Data Collection V1.7

Collect source-linked, period-specific data for a Bursa Malaysia listed company using data/data_schema.md and related schemas.

## Instructions
- First confirm legal company name, Bursa ticker/share class, sector, industry, reporting currency and analysis date. If uncertain, mark the identity field MISSING/N/A and stop company-specific attribution.
- Capture all relevant fields from data/data_schema.md: company name, Bursa ticker, sector, industry, reporting period, revenue, EBITDA, EBIT, net profit, EPS, gross/operating margin, ROE, ROIC, total/net debt, cash, operating cash flow, capex, free cash flow, dividend, shares outstanding, current share price, market capitalization and enterprise value.
- For each field include value/status AVAILABLE, MISSING, ESTIMATED or NOT APPLICABLE; unit/currency; exact period or observation date; basis/definition; source/evidence ID; formula if calculated; quality flag.
- Prefer Bursa filings and official issuer disclosures for financials. Follow research/evidence/source_priority.md when sources conflict.
- Preserve reported values; calculated or converted values are separate records with formula and source inputs. Label all estimates and assumptions. Never invent, infer-to-fill, annualize silently, or substitute zero for missing data.
- Keep original and restated figures traceable. Identify audit/review status, units, period length, share adjustments and corporate actions.
- Use N/A for unavailable data and explain the impact on downstream modules and confidence. NOT APPLICABLE requires a business-model rationale.

## Output
Return:
1. Confirmed company metadata.
2. A structured table with one row per metric and required status/period/unit/basis/source/calculation fields.
3. Conflict and validation log.
4. Missing/N/A list and downstream effects.
5. Evidence IDs and source-quality grade for every material record.
Do not calculate scores or valuations; pass validated inputs to the unchanged V1.2–V1.6 modules.

## Evidence labels and missing data
- FACT: directly source-supported observation or reproducible calculation with its inputs and formula.
- ANALYSIS: interpretation of verified facts with method and limitations.
- INFERENCE: qualified conclusion derived from evidence, including uncertainty and alternatives.
- FORECAST: conditional forward view with horizon and explicitly identified ASSUMPTIONS.
Missing evidence is MISSING and displayed as N/A with its downstream effect; do not fabricate or silently substitute a value.
