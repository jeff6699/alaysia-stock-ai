# Financial Data Schema V1.7

## Purpose and basis
Standardize issuer-reported and derived financial data for research and later automation. This schema does not change the V1.2 scoring or V1.1 financial-analysis rules. Follow data/data_schema.md for record status and research/evidence/evidence_schema.md for sources.

For each observation record company, Bursa ticker, metric_id, value/status, currency/unit, period start/end, annual/interim/quarter/T12M/forecast period type, consolidated or parent basis, audit/review status, source IDs, formula, restatement state and collection date. Retain source-reported and analyst-derived metrics separately.

## Core financial observations
Collect when available:
- Revenue, cost of sales, gross profit, operating expenses, EBIT/operating profit, EBITDA, finance costs, tax, profit before tax, net profit attributable to owners and non-controlling interests.
- Basic and diluted EPS, weighted average shares and period-end shares.
- Gross margin, operating margin, net margin, ROE and ROIC. Store numerator/denominator and averaging, tax, lease, goodwill and equity treatment.
- Cash and equivalents, restricted cash if disclosed, short/long-term borrowings, lease liabilities, total debt, net debt, equity, working capital and maturity profile.
- Net cash from operating, investing and financing activities; cash purchases of property/plant/equipment and intangibles; capex additions where separately disclosed; FCF with its exact convention.
- Trade and other receivables, contract assets/liabilities, inventory, payables, provisions, impairment/ECL and material non-cash adjustments when disclosed.
- Dividends proposed/declared/approved/paid, DPS, dates, share issue/buyback and dilution, acquisitions/disposals and segment revenue/profit/assets/capex when disclosed.

## Definitions and calculations
Store the issuer's reported metric with the issuer's definition. Any analyst-calculated metric is a separate record with status AVAILABLE only if all inputs are evidenced and formula is reproducible; otherwise mark ESTIMATED or MISSING as appropriate and explain.

Common conventions, subject to the existing module's definition:
- Growth = current period / comparable prior period − 1. Explain negative/zero bases, acquisitions, restatements and period-length differences; do not imply meaningful percentage growth from an unsuitable base.
- Gross margin = gross profit / revenue; operating margin = EBIT / revenue. Keep reported and calculated margins distinguishable.
- ROE and ROIC must specify profit numerator, average or closing balance denominator, tax and lease treatment, and period. Do not assume denominator convention.
- Net debt = defined debt less defined cash; say whether leases, restricted cash and non-controlling interests are included.
- FCF is not universal. State whether operating cash flow less cash capex, FCFF, FCFE or another convention; identify lease principal, acquisitions, capitalized development and disposals treatment.
- EPS must identify basic/diluted status, currency unit, weighted-average shares and corporate action adjustments.

## Periods and filings
Prefer at least five annual periods where available, plus latest quarterly/interim results and comparable prior periods. Mark whether annual figures are audited and interim figures reviewed/unaudited according to the filing. Preserve fiscal-year labels and exact dates. Do not annualize an interim value without labeling it ESTIMATED and disclosing the method and seasonality limitations.

Keep consolidated and parent-only statements separate. Do not combine interim quarters with annual totals or TTM without a documented bridge. Align fiscal periods when comparing companies; explain residual mismatch. Preserve original filings and restatements and designate the latest authoritative version for current analysis.

## Bursa Malaysia and sector notes
Capture Bursa announcements and issuer filings relevant to financial reporting, corporate exercises, related parties, shares, dividends, litigation and going concern. Financial institutions, insurers, REITs, developers, contractors, plantations and commodity cyclicals may need sector-specific definitions. Mark standard industrial metrics NOT APPLICABLE only with a rationale; do not substitute an unapproved metric into V1.2 scoring.

## Validation flags
Flag missing periods, unexplained restatements, mismatch in units/currency, unusual share-count changes, negative denominators, significant one-off/non-recurring items, negative cash/debt values that require definition review, unexplained gap between profit and OCF, and formula/input disagreement. Apply data/data_quality_rules.md before passing inputs to V1.2, V1.4 or V1.5.

## Evidence labels and missing data
- FACT: directly source-supported observation or reproducible calculation with its inputs and formula.
- ANALYSIS: interpretation of verified facts with method and limitations.
- INFERENCE: qualified conclusion derived from evidence, including uncertainty and alternatives.
- FORECAST: conditional forward view with horizon and explicitly identified ASSUMPTIONS.
Missing evidence is MISSING and displayed as N/A with its downstream effect; do not fabricate or silently substitute a value.
