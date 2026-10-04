# Prompt: Automated Company Research Engine V1.9

Generate a complete, evidence-traceable Bursa Malaysia company research report from the user inputs Company name, Bursa ticker and Research date.

## Frameworks and boundaries
Consume V1.2 Scoring, V1.3 AI Moat, V1.4 Valuation, V1.5 Investment Decision, V1.6 Research Pipeline, V1.7 Evidence Engine and V1.8 Data Ingestion. Do not redesign, recreate or silently change any methodology. V1.9 orchestrates and assembles outputs only.

Do not invent financial data, market prices, source citations, customers, competitors, catalysts or probabilities. Unavailable data must be shown exactly as **N/A — DATA NOT AVAILABLE**. Evidence that cannot be verified must be **REQUIRES_VERIFICATION**. Preserve source, source tier/quality, document locator, dates, periods, units, currency, basis and evidence IDs. Never silently replace one source with another.

Keep FACT, ANALYSIS, INFERENCE and FORECAST distinct. Forecasts and analyst-selected inputs are conditional and labeled ASSUMPTION; never state a forecast or management target as an accomplished fact. Include counter-evidence and unresolved conflicts.

## Required execution order
1. Identify company and Bursa ticker.
2. Collect available company and financial data.
3. Collect evidence and source metadata.
4. Validate reporting periods.
5. Run financial analysis.
6. Run earnings-quality analysis.
7. Run cash-flow analysis.
8. Run AI Moat analysis using V1.3.
9. Run valuation using V1.4.
10. Run risk analysis.
11. Run catalyst analysis.
12. Construct investment thesis.
13. Run Bull / Base / Bear analysis.
14. Run V1.2 100-point scoring.
15. Run V1.5 Investment Decision Engine.
16. Generate final research report.

Record each stage status and evidence IDs. Follow research/automation/research_workflow.md for gates and reruns. If identity, critical source, period, valuation input or scenario probability gate fails, report the limitation and apply existing upstream rules; do not bypass.

## Required report
Use research/automation/research_output_schema.md and research/company/automated_company_report.md. Include Executive Summary, Company Profile, Business Model, Industry Analysis, Financial Analysis, Earnings Quality, Cash Flow, AI Moat, Valuation, Risk Analysis, Catalysts, separate Bull/Base/Bear cases, Investment Thesis, V1.2 100-Point Score, V1.5 Investment Decision, Evidence Quality, Missing Data, Research Confidence and Source List.

Rate research confidence HIGH/MEDIUM/LOW using the six qualitative factors in the output schema. Do not create false precision. Complete research/automation/research_quality_control.md before presenting a report as complete.
