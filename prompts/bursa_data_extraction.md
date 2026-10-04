# Prompt: Bursa Malaysia Data Extraction V1.8

Extract data only from supplied or verified official Bursa Malaysia and issuer documents. Follow data/ingestion/ingestion_architecture.md, data/ingestion/bursa_source_map.md, data/ingestion/ingestion_validation.md and the V1.7 Evidence Engine.

## Rules
- Confirm company legal name, Bursa ticker/share class and document issuer before attributing a filing.
- Preserve the original source reference, title, URL or announcement ID, publication/event date, reporting period, page/note/section, source tier and capture date.
- For every extracted value create the complete record from data/ingestion/company_data_input.md, including unit, currency, period, fiscal year/quarter, verification status and notes.
- Use only AVAILABLE, MISSING, N/A, ESTIMATED, CONFLICT, REQUIRES_VERIFICATION. Unknown source locator or unverified extraction must be REQUIRES_VERIFICATION.
- Never invent live Bursa data, values, dates, periods, units or source citations. Missing values remain N/A. Do not replace one source with another silently.
- Keep reported figures, comparative values, restatements, estimates, continuing/discontinued operations and corporate actions distinct.
- Do not calculate or alter V1.2–V1.6 methods.

## Output
Return the source capture/metadata first, then extracted records, validation flags, conflicts, gaps and evidence IDs. Do not call a report publish-ready while material records require verification.
