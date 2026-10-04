# Financial Data Input V1.8

## Purpose
Standardize extracted financial statement items while retaining source, period and accounting context. Align definitions with data/financial_data_schema.md and ingestion_validation.md. Do not calculate or change V1.2 scoring rules.

## Financial record fields
Use the complete required record shape in company_data_input.md for each metric. Additionally capture:
- Statement location: statement name, note number, page/table/row.
- Filing/publication date and report version.
- Reporting basis: consolidated/parent, continuing/discontinued operations, owners/NCI, basic/diluted.
- Audit/review status and whether value is reported, comparative, restated or derived.
- Accounting definition, reclassification, sign convention and any adjustment.
- Evidence ID and source/document metadata ID.

## Standard metrics
Create separate records for each applicable metric and reporting period.

| Metric | Definition / required distinction |
|---|---|
| Revenue | Filed revenue; specify continuing/discontinued operations and period |
| Gross profit | Filed or reproducibly derived revenue less cost of sales; identify definition |
| EBITDA | Reported or explicitly calculated; list D&A and adjustments |
| EBIT | Filed operating profit/EBIT and issuer definition; do not assume labels are equivalent |
| Profit before tax | Filed value, consolidated/parent basis |
| Net profit | State attributable to owners, NCI or total and operation status |
| EPS | Basic/diluted, unit, weighted average shares and restatement/corporate action basis |
| Cash | Cash/equivalents and restricted cash treatment |
| Total debt | Borrowings; identify current/non-current and lease inclusion |
| Net debt | State exact debt minus cash definition |
| Operating cash flow | Filed net cash from operating activities and period |
| Capital expenditure | Cash purchases versus asset additions distinguished; identify included items |
| Free cash flow | Explicit formula and input records; never use unqualified FCF label |
| Total assets | Filed consolidated/parent balance-sheet amount and date |
| Total equity | State total equity versus equity attributable to owners and date |
| ROE | Formula, earnings numerator, average/closing equity basis and period |
| ROIC | Formula, NOPAT/invested-capital definition, lease/goodwill treatment and period |
| Dividend | Separate proposed/declared/approved/paid status and dates; see dividend_data_input.md |

For all rows carry value, unit, currency, exact reporting period, fiscal year/quarter, source, source locator, tier, extraction date, verification status and notes. Mark unavailable as MISSING/N/A, unresolved disagreement as CONFLICT and unverified extraction as REQUIRES_VERIFICATION. An analyst/model estimate uses ESTIMATED and must show method and assumptions.

## Special treatments
- **Restated figures:** preserve original and restated records; link restatement announcement/report, effective period, reason and current-use selection. Never overwrite.
- **Comparative figures:** retain the comparative as presented, its target period and source filing; flag if the current filing recasts comparatives.
- **Continuing operations:** separately identify continuing/discontinued figures and consolidated total; do not compare unlike scopes.
- **Discontinued operations:** retain classification and disposal/held-for-sale context as disclosed; do not silently fold into normalized earnings.
- **One-off items:** retain reported results and separately record disclosed items/analyst adjustments with evidence and assumptions.
- **Extraordinary items:** use this label only where the issuer/accounting disclosure uses it; otherwise describe the item without implying a special accounting classification.
- **Different currencies:** preserve original reporting currency; converted records require explicit FX series/source/date/rate and conversion formula.
- **Different reporting periods:** retain exact dates and period type; do not mix quarterly, year-to-date, annual or TTM values. See reporting_period_control.md.
- **Negative values:** retain sourced negatives, explain sign/denominator and mark ratios N/A where invalid.

Do not use an ESTIMATED number as historical fact. Provide only verified source-grounded records to the V1.7 evidence stage.
