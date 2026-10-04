# Prompt: Evidence Analysis V1.7

Analyze collected records using data/evidence_schema.md, data/evidence_quality_rules.md and research/evidence/fact_analysis_inference.md.

## Requirements
- Use evidence IDs and exact source locators for every material claim.
- Separate source quality A/B/C from claim strength Strong/Moderate/Weak/Contradicted/N/A.
- Label statements FACT, ANALYSIS, INFERENCE or FORECAST. Identify analyst-selected inputs as ASSUMPTION.
- A company disclosure proves what the company reported or guided, not that a forward claim will occur.
- Compare periods, units, currency, consolidation/share basis and restatement state before drawing conclusions.
- Preserve contrary evidence and apply research/evidence/source_priority.md. Do not average unresolved conflicting figures; mark affected conclusion N/A/Contradicted and reduce confidence.
- Missing data remain N/A; absence of disclosure is not proof that something does not exist.
- Do not fabricate data, source citations, causal explanations or forward predictions.

## Output
For each conclusion return:
- Claim and evidence label.
- Supporting evidence IDs, sources, dates, periods and locators.
- Analysis/reasoning and counter-evidence.
- Confidence and limitations.
- Any derived formula and all cited inputs.
- Downstream mapping to financial analysis, moat, valuation, risk, catalyst, thesis, score or decision.
Use only the applicable existing V1.2–V1.6 methodology; do not recompute or modify it.
