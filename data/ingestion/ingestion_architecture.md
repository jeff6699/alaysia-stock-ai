# Bursa Malaysia Data Ingestion Architecture V1.8

## Purpose and boundary
Prepare a controlled, auditable path to ingest Bursa Malaysia company disclosures, financial statements, market/dividend/corporate-action data and macro/industry evidence. V1.8 is a Markdown architecture and operating specification; it does not fetch live Bursa data or introduce code/dependencies. All new records are sourced; no fabricated/live sample data is included.

V1.8 adds ingestion controls only. It does not change V1.2–V1.7 scoring, moat, valuation, decision, research or evidence rules. V1.8 records feed the V1.7 Evidence Engine; the V1.6 pipeline consumes validated evidence using its own steps.

## Data path
**V1.8 Data Ingestion → V1.7 Evidence Engine → V1.6 Research Pipeline → V1.2 Scoring → V1.3 AI Moat → V1.4 Valuation → V1.5 Investment Decision**

This is a handoff/data-lineage path, not a replacement workflow. V1.6 may conduct company/industry and financial research before scoring; each engine is run according to its existing versioned module. Preserve ingestion records, source evidence and downstream interpretations as separate objects.

## Source hierarchy
| Tier | Sources | Intended use |
|---|---|---|
| Tier 1 | Bursa Malaysia official disclosures; company annual reports; company quarterly reports; official investor presentations; official company announcements | Preferred support for issuer facts and reported financial results |
| Tier 2 | Reputable financial databases; broker research; industry research | Cross-checks, structured data, estimates and context; retain underlying source/definition |
| Tier 3 | Financial news; other secondary sources | Leads and context; verify material facts against Tier 1/2 where possible |

Use the exact source precedence and conflict procedure in research/evidence/source_priority.md. A tier is source authority for use, not a guarantee of claim accuracy. Never silently substitute a source; retain each source record, conflict links and the reason for any selected value.

## Ingestion lifecycle
1. Identify issuer, Bursa ticker/security class and requested data scope.
2. Capture original source metadata and source document before extracting values.
3. Assign stable Record ID and evidence ID; preserve source/report versions.
4. Extract each value into the applicable input sheet: company, financial, market, dividend, corporate action, macro/industry.
5. Add required record metadata, status, period, unit, currency, definition and source/document locator.
6. Validate identity, period, currency, unit, data type, historical/current status, restatement and verification.
7. Resolve or log source conflicts without erasing originals.
8. Pass verified records to V1.7 Evidence Engine with linked evidence IDs.
9. Map accepted evidence to V1.6 and existing scoring/valuation/decision modules. A module's own N/A, coverage and confidence rules remain authoritative.
10. Maintain revision history and log reviewer, extraction date, verification date and any supersession.

## Required ingestion record
Every record contains the fields defined in data/ingestion/company_data_input.md: Record ID; company name; Bursa ticker; data category; metric; value; unit; currency; period start/end; fiscal year/quarter; source; source URL/document reference; source tier; extraction date; verification status; notes. For instantaneous or inapplicable dimensions, preserve the field and use N/A with reason rather than omitting metadata.

Supported statuses are exactly **AVAILABLE, MISSING, N/A, ESTIMATED, CONFLICT, REQUIRES_VERIFICATION**. Interpret them under data/ingestion/ingestion_validation.md. A displayed value does not by itself mean verified.

## Source immutability and versioning
Keep the original downloaded/viewed source unchanged where storage is permitted; store its URL/document identifier, exact title, publication date, capture date and content fingerprint or local reference if available. Never overwrite the evidence record when a correction, restatement or new source arrives. Create a new version/record, link it as superseding or conflicting and explicitly select the current authoritative record for a named use. Retain the former record and selection rationale.

Do not store restricted documents or credentials without authorization. For inaccessible or unverified sources, record the access limitation and set REQUIRES_VERIFICATION or MISSING.

## Supported source families
- Bursa announcements and company disclosures
- Annual and quarterly/interim reports
- Investor presentations
- Financial-statement line items
- Dated share price, market capitalization, shares, volume and valuation inputs
- Dividends and corporate actions
- Official and reputable macro/industry series

Source discovery and mapping are specified in bursa_source_map.md. Collection details are in research/evidence/source_capture.md and research/evidence/source_metadata.md; strict period safeguards are in research/evidence/reporting_period_control.md.
