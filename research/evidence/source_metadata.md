# Source Metadata V1.8

## Metadata model
A source/document record describes the source object; an evidence record describes a claim derived from it. Link them, but do not conflate them. See data/evidence_schema.md for claim records and research/evidence/source_capture.md for capture process.

| Metadata field | Definition |
|---|---|
| source_id | Stable unique ID; do not reuse for a changed document/version |
| publisher_or_issuer | Bursa, company, agency, database, broker, publisher or author |
| title | Exact document/page/series title |
| source_type | Filing, annual report, quarterly report, presentation, announcement, database, broker research, industry research, news or other specified type |
| source_tier | Tier 1 / Tier 2 / Tier 3 per data/ingestion/bursa_source_map.md |
| source_url_or_reference | URL, announcement ID, filename/repository reference or series code |
| publication_date | Date released/published |
| observation_or_event_date | Date the claim describes, if different |
| reporting_period | Period stated by source or N/A |
| document_version | Original, correction, restatement, revised series or version label |
| filing_status | Audited, reviewed, unaudited, presentation, management estimate or N/A |
| currency_and_units | Source conventions and scales |
| language | Original language and any translation details |
| captured_at | Date/time collected and collector |
| locator | Page/note/table/slide/section/announcement paragraph |
| source_quality | A / B / C under V1.7 evidence rules |
| integrity_reference | Content fingerprint or archived reference, if available and permitted |
| supersedes / conflicts_with | Linked source IDs and rationale |
| access_limitations | Paywall, unavailable attachment, partial extract, stale page or other limitation |
| review_status | AVAILABLE, MISSING, N/A, ESTIMATED, CONFLICT or REQUIRES_VERIFICATION |

## Rules
Keep original and corrected/revised source metadata as separate records. A new report does not delete the earlier record. Preserve publication date separately from the financial period and extraction date. If metadata cannot be verified, record N/A/REQUIRES_VERIFICATION rather than guessing.

Evidence grade A/B/C is source quality, not claim strength. An official filing can contain a target or estimate that remains uncertain as a future outcome. Link each assertion to its evidence record and exact locator.
