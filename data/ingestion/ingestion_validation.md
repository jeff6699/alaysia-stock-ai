# Ingestion Validation and Release Gate V1.8

## Supported statuses
Use only:
- **AVAILABLE** — value and source/document metadata are present, required fields validate, and the extraction has been checked.
- **MISSING** — expected/requested item could not be found after documented search.
- **N/A** — item is not applicable or meaningful for this issuer/record; state rationale.
- **ESTIMATED** — value is modeled or estimated, with method, assumptions and evidence inputs; never historical fact.
- **CONFLICT** — two or more credible records disagree and resolution is pending or cannot be made.
- **REQUIRES_VERIFICATION** — source, identity, extraction, locator, units or value has not yet been verified.

Do not use blank status. Zero is AVAILABLE only when source-supported; it is never a missing-value code. Keep status separate from source tier and V1.7 evidence strength.

## Ten-point data quality check
Before a record enters research, validate:
1. **Company identity:** legal issuer, Bursa ticker and security class.
2. **Reporting period:** exact start/end or dated observation; annual/quarter/interim/point-in-time.
3. **Currency:** original currency preserved; conversion metadata attached if derived.
4. **Unit:** RM/sen, RM’000/million, shares/lots, %, times and scaling validated.
5. **Source:** source title, URL/document ID and page/section/announcement locator.
6. **Data type:** financial, market, dividend, corporate action, macro or industry field and definition.
7. **Historical/current status:** distinguish reporting period from observation date; label stale market inputs.
8. **Restatement status:** original/restated/comparative version and governing record identified without deleting others.
9. **Verification status:** source, extraction, calculation and reviewer checks recorded.
10. **Notes and lineage:** evidence ID, formula/input links, extraction date, quality flags and downstream use.

## Validation outcomes
| Outcome | Action |
|---|---|
| All applicable required checks pass | AVAILABLE; capture evidence and metadata |
| Source unavailable after documented search | MISSING; display N/A, explain scope and downstream effect |
| Field not meaningful | N/A; give business-model reason |
| Estimate only | ESTIMATED; isolate from history and label assumptions |
| Credible sources conflict | CONFLICT; preserve both records and follow source hierarchy |
| A required detail is unverified | REQUIRES_VERIFICATION; do not pass as verified fact |

## Hard stops and downstream controls
- Unresolved issuer/security identity: stop attribution and downstream company scoring.
- Unverified source/value or material unresolved conflict: do not present as a verified FACT.
- Period, unit or currency mismatch: quarantine record from calculation until normalized with lineage.
- Restated data: no silent replacement; record and select explicit version for the intended comparison.
- Estimate as historical actual: reject and correct record.
- A downstream engine receives only validated data plus status and evidence IDs. V1.7 evidence rules and V1.2–V1.6 coverage, scoring, valuation and decision controls remain unchanged.
