# Corporate Action Input V1.8

## Action record
Create a distinct immutable record for each action and revision. Use the required ingestion record fields in company_data_input.md and add:
- Action ID and action type.
- Announcement date, effective date, ex-date/record date/payment date as applicable.
- Terms, ratio, amount, consideration and currency exactly as disclosed.
- Share class, affected security and status (proposed, approved, completed, withdrawn or other exact state).
- Source document, Bursa announcement number, page/section/URL and evidence ID.
- Linked price/share-count records and superseding/conflicting action IDs.
- Extraction and verification dates, reviewer and notes.

Never infer an action ratio or completion status from a later price pattern.

## Supported action types
| Action | Capture |
|---|---|
| Dividend | DPS/aggregate, type, announcement and entitlement/payment dates, approval/status; link dividend record |
| Bonus issue | Ratio, eligible shares, key dates, fractional entitlements, new share basis |
| Rights issue | Entitlement ratio, subscription price/currency, dates, renounceability and take-up/results where disclosed |
| Share split | Old/new ratio, effective dates and share class |
| Share consolidation | Consolidation ratio, effective dates and fractional treatment |
| Private placement | Proposed/placed shares, price, dilution, approvals and completion status |
| Acquisition | Parties/assets, consideration, funding, conditions, approval/completion status and dates |
| Disposal | Assets/business, consideration, conditions, approval/completion status and dates |
| Major corporate transaction | Issuer-defined transaction description, terms, rationale as stated, conditions, approvals and event status |

## Effects and controls
Retain reported, unadjusted share/price data. If adjusted share counts, per-share data or price series are needed, create separate calculated records with explicit action terms, formula, effective date and linked sources. Never silently rewrite historical price, EPS, DPS, shares outstanding, market capitalization or valuation.

Do not infer transaction completion until the relevant official confirmation exists. Pending conditions, approvals, financing or legal disputes remain notes/status fields. Unavailable terms are N/A; unverified terms use REQUIRES_VERIFICATION.
