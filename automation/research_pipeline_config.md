# Research Pipeline Configuration Contract V1.9

## Purpose
Specify human-readable configuration keys for a future company research workflow. This document is not executable configuration and has no external dependencies. Do not enter credentials, fabricated values or live-market defaults.

## Required request keys
| Key | Type | Required | Rule |
|---|---|---|---|
| company_name | text | Yes | User input; resolve against official source |
| bursa_ticker | text | Yes | User input; validate security class/issuer |
| research_date | ISO date | Yes | User-defined report cut-off |
| run_id | text | Generated or supplied | Unique per execution |
| report_language | text | Yes | English for V1.9 documentation/output |
| source_cutoff_date | ISO date | Yes | Do not consume later evidence silently |

## Module registry
| Version | Module | Read/output boundary |
|---|---|---|
| V1.2 | Scoring | Read existing scorecard/rules/output; do not rewrite |
| V1.3 | AI Moat | Read moat outputs; do not rewrite |
| V1.4 | Valuation | Read value range, assumptions and confidence; no recalculation in V1.9 |
| V1.5 | Investment Decision | Read risks, catalysts, scenario rules and final decision |
| V1.6 | Research Pipeline | Reuse workflow/report structure |
| V1.7 | Evidence Engine | Read evidence/source quality and claim taxonomy |
| V1.8 | Data Ingestion | Read source map, record schemas, statuses and period validation |
| V1.9 | Orchestrator | Validate, sequence, map and assemble only |

## Run controls
- Do not enable live data by default; live integrations require their own approved source, access and capture configuration.
- Do not store tokens, cookies or secrets in configuration.
- No source substitution, silent price refresh, default financial values, false confidence percentages or fallback score.
- Freeze method versions, research date and source cut-off for reproducibility.
- Status vocabulary and confidence semantics come from the existing V1.7/V1.8 rules.
- Output locations: research/company/automated_company_report.md and/or reports/automated_company_report_template.md; optional summary reports/investment_research_summary.md.
- Quality gate: research/automation/research_quality_control.md.

## Version change control
A future change to an upstream module is adopted only when explicitly versioned and reviewed. V1.9 records the exact consumed version for every run. Schema adapters may map fields while preserving source values and lineage; they must not alter upstream calculation definitions.

Unavailable inputs are N/A — DATA NOT AVAILABLE; source/value details not confirmed are REQUIRES_VERIFICATION. Do not insert default values for either status.
