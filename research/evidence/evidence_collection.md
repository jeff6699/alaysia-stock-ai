# Evidence Collection Workflow V1.7

## Purpose
Collect reproducible evidence for Malaysian listed-company research. Follow data/evidence_schema.md, data/evidence_quality_rules.md, data/data_quality_rules.md and research/evidence/source_priority.md. V1.7 defines collection and traceability; it does not alter V1.2–V1.6 methodologies.

## Collection sequence
1. Confirm company legal name, Bursa ticker/share class, sector, period and analysis date.
2. Search relevant Bursa Malaysia filings and issuer disclosures first; capture source ID, exact date, file/title, announcement number/page/note and relevant reporting/observation period.
3. Collect annual and quarterly/interim reports, presentations and company announcements relevant to the claim. Preserve audit/review status, basis, units and original wording.
4. Collect official regulator/statistical data for macro/industry claims. Use reputable secondary evidence only for context/corroboration or to identify a question to verify.
5. Create separate evidence records for distinct claims. Save the exact supporting datum or concise neutral paraphrase with locator; link conflicting/corroborating records.
6. Validate periods, unit, currency, share basis, corporate actions, revisions/restatements and calculations under data/data_quality_rules.md.
7. Map accepted evidence to downstream modules through research/evidence/evidence_mapping.md.
8. Identify gaps, unresolved conflict and source limitations. Mark MISSING/N/A; do not infer missing numeric values.

## Search and review log
For each research pass record:
- Company/ticker, scope, analysis date and collector/reviewer.
- Documents and data sources checked, including publication/retrieval date and locator.
- Periods and topics covered.
- Relevant source quality A/B/C and evidence strength.
- Claims confirmed, claims contradicted and source IDs.
- Search limitations, unavailable/paywalled material and N/A data.
- Review date and next update event.

## Collection rules
- Distinguish date published, date observed and period reported.
- For an issuer claim, FACT may say “the issuer reported/stated X”; that does not establish a forecast outcome or unverified cause.
- Use an exact source locator, not a repository-wide citation with no path to the claim.
- Do not copy stale market prices, summaries or reports as current.
- Keep original and translated wording distinguishable.
- Preserve restated/original values and identify which one governs current analysis.
- Do not use weak secondary sources as sole support for material investment claims.
- Collection gaps lower evidence confidence; no evidence found is not proof of absence.

## Evidence labels and missing data
- FACT: directly source-supported observation or reproducible calculation with its inputs and formula.
- ANALYSIS: interpretation of verified facts with method and limitations.
- INFERENCE: qualified conclusion derived from evidence, including uncertainty and alternatives.
- FORECAST: conditional forward view with horizon and explicitly identified ASSUMPTIONS.
Missing evidence is MISSING and displayed as N/A with its downstream effect; do not fabricate or silently substitute a value.
