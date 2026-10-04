# AI Moat Evolution Score V1

## Purpose
Evaluate the strength, durability and likely evolution of a Bursa Malaysia company’s competitive advantages over a 3-year base period, including risks and opportunities from AI. Use evidence, not product claims alone. The framework is decision support, not a buy/sell recommendation.

## Moat dimensions and current strength (100 points)
Each applicable dimension has a 10-point maximum. See ai_moat_scoring_rules.md for evidence and anchors.

| Dimension | Maximum |
|---|---:|
| Brand Power | 10 |
| Cost Advantage | 10 |
| Scale Advantage | 10 |
| Switching Costs | 10 |
| Network Effects | 10 |
| Distribution Advantage | 10 |
| Technology / IP | 10 |
| Data Advantage | 10 |
| AI Capability | 10 |
| Capital / Ecosystem Advantage | 10 |
| TOTAL | 100 |

Not every moat applies to every business. Mark a dimension N/R (not relevant) only with a business-model reason; mark N/A when relevant evidence is unavailable or unreliable. Weak/absent evidence on a relevant dimension is scored low, not N/A. Current Moat Score = earned dimension points / scoreable relevant points × 100. Report relevant points, scoreable points and evidence coverage = scoreable relevant / all relevant. If evidence coverage is below 70%, the Current Moat Score is N/A for composite calculation (a preliminary normalized observation may be shown as unweighted/provisional). If no dimension can be scored, it is N/A.

## Overall AI Moat Evolution Score (100 points)
The composite combines five explicitly distinct components:

| Component | Maximum | Meaning |
|---|---:|---|
| Current moat strength | 30 | Normalized Current Moat Score × 0.30 |
| Moat durability | 20 | Persistence of advantage, scored with the 5-factor rubric |
| 3-year trajectory | 20 | Average expected dimension direction, mapped from −2…+2 to 0…20 |
| AI disruption resilience | 15 | Inverse of residual AI disruption risk; 15 means low risk |
| AI opportunity | 15 | Credible ability and path to use AI to reinforce/extend moat |
| TOTAL | 100 | |

AI disruption component is explicitly an inverse risk score, not a direct risk rating. Always also report residual risk as Low / Moderate / High / Unknown with explanation. AI opportunity is incremental evidence-backed potential, not a duplicate of the current AI Capability dimension: assess expected additional moat impact and execution path, not current AI tools twice.

If a component is N/A, report composite as Earned / Available, with coverage = Available / 100. For the Durability component, normalize scored factors to the 20-point maximum only when at least 70% of its factor weight has evidence; otherwise mark the component N/A. For the 3-year trajectory component, average only scoreable relevant dimensions and require trajectory evidence coverage of at least 70%; otherwise mark it N/A. Do not silently assign zero or renormalize away missing components. An optional normalized comparison = Earned / Available × 100 may be shown only at ≥80% composite coverage, labeled provisional. A final rating requires ≥80% coverage and is provisional unless all five components are available; below 80%, overall score/rating is “N/A — insufficient evidence.”

## Evidence taxonomy
- FACT: sourced disclosures, observed outcomes, dated third-party evidence, or transparent calculation.
- ANALYSIS: comparison and causal interpretation.
- INFERENCE: qualified view beyond stated facts, including uncertainty and alternatives.
- FORECAST: Year +1/+2/+3 expectation, assumptions, dependencies, and falsifiers.
Keep the four labels separate in each dimension and in the final report. Never invent a customer, patent, market share, retention rate, AI deployment, cost saving, or moat claim.

## 3-year base
- Year 0 / Current: latest supportable evidence, normally current filings and up to 3 years of company history for trends.
- Year +1, +2, +3: expected direction of each relevant dimension and major dependencies. Distinguish management targets from analyst scenarios.
- Re-score at each reporting cycle; preserve the old score, evidence date and rubric version for comparison.

## Status vocabulary
Final Assessment must be one of Strengthening / Stable / Weakening / At Risk, subject to coverage. Use ai_moat_evolution.md for trajectory, composite and override rules. Identify applicable moat sources/threats, AI disruption risks, new moat opportunities, competitor threats and management actions.

## Output
Use research/company/ai_moat_report_template.md. Store per dimension: stable metric_id, applicability (relevant/N_R), evidence status (scored/N_A), value/evidence, score/max, trajectory (−2…+2), source/date, rationale and warning. Keep raw observations so a future structured implementation can calculate totals without changing evidence.
