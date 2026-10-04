# Decision Rules V1.5

## 1. Weighted components
The fixed maxima are Quality 30 + AI Moat 20 + Valuation/MOS 25 + Risk Profile 15 + Catalysts 10 = **100 points**.

### Quality (0–30)
Use the valid V1.2 standard score without changing it: points = V1.2 score / 100 × 30. V1.2 requires 100% available coverage for its standard grade. If incomplete, mark this component N/A; preserve its reported raw partial score in the input summary.

### AI Moat (0–20)
Use the valid V1.3 final AI Moat Evolution composite: points = V1.3 composite / 100 × 20. V1.3 requires its stated ≥80% composite coverage for a final rating; if not met, mark N/A. Never substitute Current Moat Score for the overall composite.

### Valuation / MOS (0–25)
Use V1.4 Base MOS, computed by V1.4, and its confidence. The following fixed decision-policy bands translate that output; they do not modify V1.4 or its required-MOS assumption.

| V1.4 Base MOS | Points | Rationale |
|---:|---:|---|
| ≥40% | 25 | Large modeled cushion |
| 30% to <40% | 22 | Strong modeled cushion |
| 20% to <30% | 18 | Meaningful modeled cushion |
| 10% to <20% | 14 | Limited cushion |
| 0% to <10% | 10 | Little or no cushion |
| −10% to <0% | 5 | Price modestly above Base FV |
| <−10% | 0 | Price materially above Base FV |
| N/A / invalid | N/A | MOS cannot be calculated reliably |

If V1.4 confidence is Low, cap this component at 10/25 and do not classify above WATCHLIST. If confidence is Medium, retain the band but classification cannot be STRONG OPPORTUNITY. High confidence permits, but does not assure, those labels. The bands are policy cutoffs, not return probabilities or a replacement for the V1.4 margin-of-safety selection.

### Risk Profile (0–15)
Use the aggregate risk rating from risk_engine.md and its control-point band: Low = 15, Moderate = 12, Elevated = 8, High = 4, Critical = 0. If aggregate rating is Unknown/N/A, component is N/A. Points reflect risk manageability supported by evidence, not the absence of risk.

### Catalysts (0–10)
Apply catalyst_engine.md: one point per category, max 10; each is 1 for evidence-backed and confirmable, 0.5 for credible but conditional, 0 for unsupported or no identified catalyst after adequate review. If reviewed evidence is unavailable, that category is N/A. Sum earned and available points without filling N/A categories.

## 2. Coverage and confidence gates
- Available points are the full component maximum when the component is scoreable; N/A components add neither available nor earned points. A valid low score remains available.
- Coverage = Available Points / 100. Below 80%: INSUFFICIENT DATA, irrespective of provisional score.
- At ≥80%, show Earned / 100; optionally show Earned / Available × 100 as a provisional normalized comparison. Classification still uses the unnormalized earned score and all gates. This avoids concealing gaps.
- Critical-data gate: if dated current price or V1.4 Base Fair Value is unavailable/invalid, or the required V1.2 standard score or V1.3 final composite is unavailable, classify INSUFFICIENT DATA. If scenario probabilities are incomplete or do not total exactly 100%, the scenario report is incomplete; do not publish a standard classification until corrected. A substantiated HIGH RISK override may still be reported, with the scenario section marked incomplete.
- HIGH confidence requires complete or near-complete key inputs, current primary sources, consistent evidence and few material unresolved assumptions. MEDIUM indicates bounded gaps or meaningful but manageable assumptions. LOW indicates material stale/unverified/conflicting data or numerous unresolved assumptions. Record the basis under all five factors; do not infer an average confidence score.
- LOW data confidence: no STRONG OPPORTUNITY or ATTRACTIVE; default to WATCHLIST after mandatory overrides.
- MEDIUM data confidence: no STRONG OPPORTUNITY.
- LOW valuation confidence: no label above WATCHLIST, except OVERVALUED or HIGH RISK may still apply.
- Conflict resolution is conservative: a weaker confidence/coverage gate prevails.

## 3. Score bands and decision hierarchy
The score bands below are eligibility guides, not automatic labels:
- 85–100: eligible for STRONG OPPORTUNITY only if all strong-opportunity tests below pass.
- 70–84.99: eligible for ATTRACTIVE subject to the tests below.
- 55–69.99: WATCHLIST range.
- 0–54.99: WATCHLIST by default; HIGH RISK applies only through the explicit risk/override rules. Explain low points and required evidence/actions.

Apply the following in order; first applicable rule determines the single classification:
1. **HIGH RISK** if reliable evidence establishes an automatic override in Section 4. Known severe risk is not diluted by unrelated missing inputs.
2. **INSUFFICIENT DATA** if a coverage/critical-data gate in Section 2 applies and no substantiated HIGH RISK override applies.
3. **OVERVALUED** if V1.4 Base MOS is below −10% and V1.4 confidence is not Low. If confidence is Low, use WATCHLIST unless HIGH RISK overrides, with valuation marked unreliable.
4. **FAIRLY VALUED** if Base MOS is from −10% through <10%, V1.4 confidence is not Low, and no higher-priority override applies.
5. **STRONG OPPORTUNITY** if score ≥85, Base MOS ≥30%, V1.4 confidence High, data confidence High, overall risk Low/Moderate, V1.3 assessment is Strengthening or Stable, no material thesis invalidator is active, and no unresolved high-severity risk.
6. **ATTRACTIVE** if score ≥70, Base MOS ≥20%, V1.4 confidence Medium/High, data confidence Medium/High, overall risk not High/Critical, and no critical thesis invalidator is active.
7. **WATCHLIST** in all remaining cases, including score-band eligibility failures, MOS 10% to <20%, conflicting evidence, low confidence, or timing-dependent thesis.

Fairly Valued and Overvalued are valuation-led labels and may apply even when the business score is high. A negative MOS can coexist with high quality. Decision explanation must state the gate, evidence and any score context. The policy cutoffs are screening conventions; they are not automatic trade instructions.

## 4. Decision overrides
Evidence-backed HIGH RISK overrides are evaluated first; data sufficiency gates follow unless a HIGH RISK override is already established. Other overrides may downgrade but never upgrade.

### Automatic HIGH RISK
Classify HIGH RISK when reliable evidence establishes any of these:
- Overall risk is Critical; or
- A Critical Governance, Accounting/Earnings, or Balance Sheet risk is active; or
- Two or more independent Critical risks are active; or
- A severe going-concern, solvency, fraud, material misstatement, or comparable threat is disclosed by a credible source; or
- V1.3 identifies severe AI disruption that threatens the core business, with no evidenced response path and material exposure.

Active requires current, cited evidence and material impact. Do not label allegations as established facts. If evidence is too weak to resolve the concern, reduce confidence and use INSUFFICIENT DATA or WATCHLIST under the gates rather than assert HIGH RISK.

### Valuation guard
Base MOS <−10% with non-Low V1.4 confidence forces OVERVALUED after critical risk checks, even where score is high. Base MOS between −10% and <10% similarly leads to FAIRLY VALUED. Low valuation confidence blocks these labels because price/value conclusions are unreliable; report WATCHLIST unless a higher-priority rule applies.

### Insufficient evidence
Missing critical inputs, coverage <80%, unverified issuer identity, materially inconsistent source data, or stale price/valuation inputs that cannot be aligned produce INSUFFICIENT DATA. Missing data alone is not HIGH RISK and is never silently scored as zero.

### Downgrade conditions
A company that meets a score band but has LOW/MEDIUM data confidence, low V1.4 confidence, an active material thesis invalidator, high risk, weak moat trajectory, or insufficient MOS must be downgraded according to the hierarchy above. Document each rule applied.

## 5. Data confidence record
For each factor record rating and evidence:
| Factor | HIGH | MEDIUM | LOW |
|---|---|---|---|
| Completeness | Key inputs and periods present | Bounded non-critical gaps | Critical gaps or major omissions |
| Recency | Current filings and aligned market date | Some dated but usable evidence | Stale or dates cannot align |
| Source quality | Primary disclosures or auditable calculations | Mixed primary/secondary, cross-checked | Unsupported claims or weak provenance |
| Consistency | Statements reconcile; contradictions resolved | Limited unresolved differences | Material conflict or unreliable basis |
| Assumptions | Few and sensitivity-bounded | Several disclosed, bounded | Numerous or decision-driving unsupported assumptions |

Overall confidence is the weakest material factor unless the analyst explains why a single non-critical weakness does not limit the decision. LOW factor in a critical input makes overall confidence LOW; do not mechanically average.

## 6. Required decision explanation
Report: raw component scores and availability, total/coverage, confidence, all gates checked, override status, decisive valuation and risk facts, why the chosen label fits, why the next more positive label fails, and what evidence could change the result.
