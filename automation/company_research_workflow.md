# Automation Workflow Definition V1.9

## Scope
This file defines the orchestration contract for future automation. V1.9 does not add code, network collectors, or fabricated data. Any future implementation must preserve V1.2–V1.8 module behavior and V1.8 source provenance.

## Sequence
The orchestrator invokes the following stages in order, matching research/automation/research_workflow.md:
1. identity resolution
2. company and financial data collection
3. evidence/source metadata collection
4. reporting-period validation
5. financial analysis
6. earnings-quality analysis
7. cash-flow analysis
8. V1.3 AI Moat
9. V1.4 valuation
10. V1.5 risk analysis
11. V1.5 catalyst analysis
12. investment thesis
13. Bull/Base/Bear scenarios
14. V1.2 100-point score
15. V1.5 final decision
16. report generation

Each stage input/output is a versioned record set. A later stage may only consume records whose identity, period, unit, source reference and status are retained.

## Stage result contract
- stage_id and stage_version
- run_id / company / ticker / research_date
- input_record_ids and evidence_ids
- source module path/version
- output reference
- status: COMPLETE / PROVISIONAL / BLOCKED / NOT_APPLICABLE
- unresolved MISSING, N/A, ESTIMATED, CONFLICT, REQUIRES_VERIFICATION items
- confidence effect and reviewer/validation result

Do not treat COMPLETE as proof of factual accuracy. The V1.8 record verification state and V1.7 evidence quality remain attached.

## Reruns and failure handling
A failed stage does not fabricate a fallback. Mark affected output N/A or BLOCKED and continue only with independent stages. Do not issue a standard V1.5 classification if its own input, coverage or scenario rules fail. Reprocessing after new filings creates a new run with links to prior run and superseding evidence; it does not overwrite data history.
