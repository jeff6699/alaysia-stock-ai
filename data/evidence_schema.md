# Evidence Schema V1.7

## Evidence record
Create one stable evidence record per source-backed claim or closely related group of claims. Do not merge claims with different sources, dates or periods in a way that loses lineage.

| Field | Required content |
|---|---|
| evidence_id | Unique stable ID, e.g. issuer-ticker-date-sequence; never reuse for a changed claim |
| company | Company name and Bursa ticker; N/A if issuer not identified |
| date | Publication/event date and, where different, observation date |
| source | Exact source title/issuer/publisher and URL, document/page/note/table/announcement number |
| source_type | Bursa filing, annual report, quarterly report, investor presentation, company disclosure, broker research, financial news, industry report, database or other specified type |
| source_quality | A / B / C from evidence_quality_rules.md; state unresolved conflict or limitations |
| claim | Atomic, neutral statement supported by the source |
| supporting_data | Exact text/numeric observation, unit, currency, period and basis; quote only what is necessary |
| reporting_period | Exact start/end, fiscal year/quarter, or N/A for point-in-time claim |
| evidence_strength | Strong / Moderate / Weak / Contradicted / N/A under evidence_quality_rules.md |
| related_research_section | Named downstream module/section and version, e.g. Financial Analysis, V1.4 Valuation |
| evidence_label | FACT / ANALYSIS / INFERENCE / FORECAST; a source record most often supports FACT, not analyst conclusions |
| collected_at | Retrieval date/time and collector, where available |
| status | AVAILABLE / MISSING / ESTIMATED / NOT APPLICABLE |
| linked_evidence_ids | Corroborating, conflicting or superseding evidence IDs |
| notes | Method, context, conflict, reliability limits, translation or extraction caveat |

## Record rules
One record must distinguish source publication date from the date the evidence describes. Retain original language/source document where material. Any translation is identified; translated wording is not treated as an exact original quotation.

A calculation supported by evidence should link every input and record the formula. Analyst-selected assumptions must be identified separately; they are not transformed into FACT merely because a spreadsheet or model contains them.

If a source cannot be located or claim verified, mark evidence strength Weak or N/A and downstream value MISSING/N/A. “No evidence found” must identify search scope; it is not proof that the claim is false.

## Compact record template
- Evidence ID:
- Company / Bursa ticker:
- Publication date:
- Observation date:
- Source / locator / URL:
- Source type:
- Source quality: A / B / C
- Claim:
- Supporting data / unit / period / basis:
- Reporting period:
- Evidence strength: Strong / Moderate / Weak / Contradicted / N/A
- Related research section:
- Evidence label: FACT / ANALYSIS / INFERENCE / FORECAST
- Status: AVAILABLE / MISSING / ESTIMATED / NOT APPLICABLE
- Linked / conflicting / superseding evidence IDs:
- Limitations / collection date:
