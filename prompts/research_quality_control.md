# Prompt: V1.9 Research Quality Review

Review a generated company report against research/automation/research_quality_control.md, research/automation/research_output_schema.md, V1.7 evidence rules and V1.8 ingestion controls.

## Check
- Correct company/ticker/security identity and research date.
- Exact requested 16-stage workflow order.
- Required report sections all present.
- Every important claim/metric has evidence IDs and a source/document locator, date, period, unit/currency/basis, or is explicitly N/A.
- N/A data uses “N/A — DATA NOT AVAILABLE”; unverified evidence uses “REQUIRES_VERIFICATION”.
- Conflicts, restatements, comparative figures, estimates and stale data are visible and period-safe.
- FACT, ANALYSIS, INFERENCE and FORECAST are separated; all forecast inputs are ASSUMPTIONS.
- Existing V1.2/V1.3/V1.4/V1.5 outputs are traceable to those versions; no methodology is duplicated or changed.
- Scenario probabilities total exactly 100% before standard V1.5 classification.
- Evidence quality and research confidence are qualitative, supported and not falsely precise.
- No fabricated financial values, sources, live prices or conclusions.
- Missing/low-confidence inputs are not hidden by a polished narrative or summary.

## Output
Return findings by severity (Blocker / Needs correction / Note) with section, claim/evidence IDs, concrete correction and downstream impact. Do not invent sources while correcting. Conclude Publishable / Provisional / Blocked with a concise rationale. Preserve all upstream source-module files and rules.
