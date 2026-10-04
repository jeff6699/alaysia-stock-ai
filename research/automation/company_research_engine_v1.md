# Automated Company Research Engine V1.9

## Purpose
Define a standardized input-to-report workflow for Bursa Malaysia company research. V1.9 orchestrates existing V1.2–V1.8 frameworks; it does not recreate their scores, assumptions, source hierarchy, evidence rating or valuation methods. The engine documents a repeatable automation-ready process and Markdown interfaces; it does not invent data or promise live data access.

## Input
Required user inputs:
- Company name.
- Bursa ticker/security code.
- Research date.

Optionally accept sector/industry if the user provides them, but verify against a trusted source before using. An example such as Company: GAMUDA; Ticker: 5398 is an input illustration only, not a research result. Confirm the issuer and ticker before collecting evidence. If identity remains unresolved, stop attribution and mark the report INSUFFICIENT DATA.

## Execution sequence
Execute in this exact order; the ordered schema lives in research/automation/research_workflow.md.

| Step | Activity | Existing module / output |
|---:|---|---|
| 1 | Identify company and Bursa ticker | V1.8 identity ingestion and V1.7 source/evidence records |
| 2 | Collect available company and financial data | V1.8 ingestion schemas and input records |
| 3 | Collect evidence and source metadata | V1.7 Evidence Engine and V1.8 source capture |
| 4 | Validate reporting periods | V1.8 reporting_period_control.md and ingestion_validation.md |
| 5 | Run financial analysis | V1.6 financial analysis and V1.1 statement framework |
| 6 | Run earnings-quality analysis | V1.1 earnings_quality_framework.md |
| 7 | Run cash-flow analysis | V1.1 cash_flow_framework.md |
| 8 | Run AI Moat analysis using V1.3 | Existing V1.3 scoring, rules and evolution modules |
| 9 | Run valuation using V1.4 | Existing V1.4 valuation framework and model modules |
| 10 | Run risk analysis | V1.5 decision/risk_engine.md |
| 11 | Run catalyst analysis | V1.5 decision/catalyst_engine.md |
| 12 | Construct investment thesis | V1.6 investment thesis structure and evidence mapping |
| 13 | Run Bull / Base / Bear analysis | Existing V1.4 value scenarios and V1.5 probability rules |
| 14 | Run V1.2 100-point scoring | Existing V1.2 scorecard and scoring rules; no duplicate rubric |
| 15 | Run V1.5 Investment Decision Engine | Existing decision rules, gates and overrides |
| 16 | Generate final research report | V1.9 output schema, templates and quality controls |

A stage may return N/A or REQUIRES_VERIFICATION and continue only where safe. Never bypass issuer-identity, source, period, valuation or decision gates. A substantiated V1.5 HIGH RISK override follows V1.5 priority rules.

## Data and evidence contract
Use V1.8's supported ingestion statuses: AVAILABLE, MISSING, N/A, ESTIMATED, CONFLICT, REQUIRES_VERIFICATION. In narrative reports, write **N/A — DATA NOT AVAILABLE** for unavailable facts/metrics, and **REQUIRES_VERIFICATION** when source or extraction cannot be confirmed. Do not treat either as zero or as evidence of adverse performance.

Every imported item retains company/ticker, data category, metric, value, unit/currency, exact reporting or observation period, source/document reference, tier, extraction date and verification status. Map its evidence ID through V1.7. Every material conclusion must trace to one or more evidence IDs and module/version; otherwise mark N/A or explicitly label an unsupported hypothesis as not decision-usable.

Use only FACT, ANALYSIS, INFERENCE and FORECAST as conclusion classes. FACT is directly sourced or reproducibly calculated from sourced inputs; ANALYSIS interprets verified facts; INFERENCE is a qualified conclusion with alternatives; FORECAST is conditional and labels all analyst ASSUMPTIONS. Never present analysis, inference, estimate, management target or forecast as an accomplished fact.

## Research confidence
Rate HIGH / MEDIUM / LOW from source quality, data completeness, reporting-period consistency, evidence coverage, conflicts and financial-data reliability using research/automation/research_output_schema.md. Do not invent percentages or average ordinal ratings. A critical missing or unresolved item lowers confidence and must be carried into V1.5 gates and the final report. Low confidence cannot support an overly confident positive classification; V1.5 rules govern the final label.

## Output
Generate all sections specified in research/automation/research_output_schema.md using research/company/automated_company_report.md or reports/automated_company_report_template.md as the canonical report. A shorter summary may be generated with reports/investment_research_summary.md. Include source list, evidence quality, missing data and confidence. Do not issue a final standard classification if V1.5 coverage, inputs or scenario-probability requirements are unmet.

## Version control and boundaries
V1.9 consumes:
- V1.2 Scoring.
- V1.3 AI Moat.
- V1.4 Valuation.
- V1.5 Investment Decision.
- V1.6 Research Pipeline.
- V1.7 Evidence Engine.
- V1.8 Data Ingestion.

Use their published versions and preserve their outputs. If a schema mismatch is discovered, document an adapter/mapping in the V1.9 layer; do not silently alter upstream fields or methodologies.
