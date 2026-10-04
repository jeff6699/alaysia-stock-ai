# Research Workflow V1.9

## Required inputs and preflight
Input is company name, Bursa ticker and research date. Verify company identity and security class from official source. Freeze research date, price observation date, source set, periods, currency, units and applicable module versions. Record unverified identity as REQUIRES_VERIFICATION and stop company-specific attribution if unresolved.

## Ordered workflow
Do not reorder the numbered stages. Each step records inputs, evidence IDs, result status, output path and unresolved issues.

1. **Identify company and Bursa ticker.** Match issuer legal name, code and share class. Output company profile identity fields and source IDs.
2. **Collect available company and financial data.** Use V1.8 company, financial, market, dividend and corporate-action input schemas. Do not require live data.
3. **Collect evidence and source metadata.** Capture documents, exact locators, publication dates and V1.7 evidence IDs.
4. **Validate reporting periods.** Apply V1.8 period controls; quarantine mixed periods, currencies, units and unresolved restatement conflicts.
5. **Run financial analysis.** Use V1.6 financial analysis and V1.1 financial statement framework. Prefer five years when available; identify latest period and filing status.
6. **Run earnings-quality analysis.** Apply V1.1 earnings quality framework; keep filed figures and adjustments separate.
7. **Run cash-flow analysis.** Apply V1.1 cash flow framework; state FCF convention and cash/capex lineage.
8. **Run AI Moat analysis using V1.3.** Run only existing V1.3 score, durability, trajectory and AI risk/opportunity rules.
9. **Run valuation using V1.4.** Select applicable methods under V1.4, identify assumptions, current-price date, fair-value range, MOS and confidence; missing inputs stay N/A.
10. **Run risk analysis.** Complete V1.5 risk register, aggregation and override rules.
11. **Run catalyst analysis.** Apply V1.5 catalyst categories, evidence, timing, impact and confirmation tests.
12. **Construct investment thesis.** Link each reason, dependency and invalidator to evidence IDs; include contrary evidence.
13. **Run Bull / Base / Bear analysis.** Use V1.4 fair values and V1.5 scenario documentation/probability rules; analyst probabilities must total exactly 100%.
14. **Run V1.2 100-point scoring.** Use original V1.2 quality rubric and missing-data coverage rules, without adapting point weights.
15. **Run V1.5 Investment Decision Engine.** Apply its score, gates, confidence caps and overrides unchanged.
16. **Generate final research report.** Populate master report, shorter summary where requested, source list and quality checklist.

## Stage record
For each step record:
- Stage number/name and run date.
- Input record IDs and source/evidence IDs.
- Module path and methodology version.
- Output file/section and status.
- FACT / ANALYSIS / INFERENCE / FORECAST labels.
- N/A, CONFLICT, ESTIMATED or REQUIRES_VERIFICATION items and downstream effect.
- Reviewer or automation identity and validation result.

## Failure and rerun behavior
A missing optional datum remains N/A. An unverified or conflicting critical datum blocks the affected calculation. On rerun, create a new run/version and retain the previous output; never silently overwrite source records or historical reports. Use V1.8 source-priority and restatement controls. Re-run downstream stages affected by changed evidence while preserving unaffected upstream source IDs. A downstream score, valuation, risk label or decision is always traceable to its original engine and version.
