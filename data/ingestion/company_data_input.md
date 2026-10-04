# Company Data Input Record V1.8

## Company master record
Create one versioned company record per issuer/security identity. Field names should align with data/data_schema.md and V1.7's standardized data structure.

| Field | Value | Status | Source / evidence ID | Notes |
|---|---|---|---|---|
| Company name |  |  |  | Legal name and/or commonly reported name, distinguish |
| Bursa ticker |  |  |  | Exact Bursa code and security class |
| Sector |  |  |  | Classification and source/date |
| Industry |  |  |  | Definition and source/date |
| Exchange / board |  |  |  | Bursa Malaysia board, if verified |
| Reporting period |  |  |  | Exact start/end and annual/interim/quarterly |
| Reporting currency |  |  |  | ISO code |
| Fiscal year end |  |  |  | Month/day or fiscal period label |
| Consolidation basis |  |  |  | Consolidated or parent-only |
| Market capitalization |  |  |  | Date and formula/provider basis |
| Source set |  |  |  | Source IDs and capture date |

## Required ingestion record fields
Use one row/object per item. Do not omit a required key; use N/A with an explanation for genuinely inapplicable period attributes.

| Record ID | Company name | Bursa ticker | Data category | Metric | Value | Unit | Currency | Period start | Period end | Fiscal year | Fiscal quarter | Source | Source URL / document reference | Source tier | Extraction date | Verification status | Notes |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|  |  |  | Company / financial / market / dividend / corporate action / macro / industry |  |  |  |  |  |  |  |  |  |  | Tier 1 / 2 / 3 |  | AVAILABLE / MISSING / N/A / ESTIMATED / CONFLICT / REQUIRES_VERIFICATION |  |

This is a blank schema, not a data example. Do not insert dummy companies or financial amounts. Detailed data types belong in financial_data_input.md, market_data_input.md, dividend_data_input.md and corporate_action_input.md.

## Company identity controls
Verify legal company name, ticker and share class using Tier 1 material. Record former names/tickers and effective dates separately when relevant. Do not attach a filing to an issuer solely because a name string is similar. If issuer/security identity cannot be verified, status is REQUIRES_VERIFICATION; do not proceed with company scoring.
