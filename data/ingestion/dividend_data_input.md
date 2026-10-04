# Dividend Data Input V1.8

## Record design
Use the full ingestion record from company_data_input.md and add dividend event ID, dividend type (ordinary/special/other as disclosed), share class, currency, per-share versus aggregate amount, source locator and linked corporate-action ID where applicable.

## Dividend fields and lifecycle
| Field | Meaning |
|---|---|
| Announcement / proposal date | Date issuer announced or proposed the distribution |
| Approval status/date | Proposed, board-declared, shareholder-approved, or other exact status |
| Ex-date | Entitlement trading date |
| Record date | Register date used for entitlement |
| Payment date | Scheduled or actual payment date; distinguish |
| DPS | Amount per share, currency and share-basis |
| Aggregate dividend | Total amount, reported or calculated with dated eligible shares and method |
| Period attribution | Financial period to which the dividend relates, if disclosed |
| Funding / coverage inputs | Linked earnings, OCF, FCF, cash and debt records; do not derive unsupported ratios |

A proposed, declared, approved, ex-dividend and paid amount are distinct statuses/events. Preserve each dated announcement and any revision/cancellation; do not overwrite the earlier record. If no announcement was found, say “not identified in sources checked” and list scope; do not assert no dividend.

## Validation and downstream use
Verify currency/unit, share class, DPS, dates, tax/withholding qualification if relevant, corporate-action adjustments and whether aggregate amount is reported or calculated. Use MISSING/N/A for unavailable fields; CONFLICT where official notices disagree pending resolution; REQUIRES_VERIFICATION when source or calculation cannot be confirmed.

Dividend yield is a separate dated market-data calculation with a stated DPS basis and share-price date. Keep dividend data separate from the financial reporting-period profit/cash figures used to assess sustainability.
