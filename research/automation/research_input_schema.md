# Research Input Schema V1.9

## User-supplied request
| Field | Required | Validation |
|---|---|---|
| company_name | Yes | Name to resolve against official issuer identity; retain exact input |
| bursa_ticker | Yes | Bursa code/security identifier; verify exact issuer and share class |
| research_date | Yes | ISO date; report cut-off date, not assumed current market date |

Optional user context (sector, industry, investment horizon, document links or focus questions) must be labeled user-supplied and verified before being treated as fact.

## Resolved identity
- Canonical company name:
- Bursa ticker:
- Security class:
- Exchange / board:
- Sector / industry:
- Identity source/evidence IDs:
- Research date:
- Price observation date or N/A:
- Identity status: AVAILABLE / REQUIRES_VERIFICATION / MISSING:

If company/ticker cannot be verified, do not attach another issuer's records. Mark the research as identity-blocked and do not produce a company-specific V1.2–V1.5 decision.

## Data and evidence input manifest
Record each object passed to the workflow:
| Input ID | Data/evidence type | Record or evidence ID | Source metadata ID | Period / observation date | Status | Module consumer |
|---|---|---|---|---|---|---|
|  |  |  |  |  | AVAILABLE / MISSING / N/A / ESTIMATED / CONFLICT / REQUIRES_VERIFICATION |  |

Required manifests cover available company profile, financial reports/records, market and corporate action records where applicable, macro/industry evidence, source metadata, evidence IDs, and upstream framework outputs. “Not supplied” is not a verified absence; use MISSING/N/A and explain.

## Input handling
- Preserve user-provided text separately from verified company data.
- Do not treat a prompt example as issuer evidence.
- Preserve original source and exact period; no invented data, missing-value imputation, silent currency conversion or source substitution.
- Store analyst estimates separately with method, ASSUMPTIONS, evidence basis and horizon.
- Reuse the V1.8 record statuses and V1.7 evidence model; no new score or confidence scale is introduced.
