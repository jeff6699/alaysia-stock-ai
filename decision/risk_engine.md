# Risk Engine V1.5

## Purpose
Maintain an evidence-led risk register and a conservative aggregate rating for Bursa Malaysia issuers. This supplements upstream research; it does not replace V1.2/V1.3/V1.4 scoring. Record each important field as FACT, ANALYSIS, INFERENCE or FORECAST; forecasts and mitigations must be clearly labeled. Unknown evidence is N/A, not Low.

## Risk levels
- **Low:** limited potential to impair thesis/value; evidence indicates controls or exposure are contained.
- **Medium:** meaningful exposure with plausible mitigants; monitor at normal review cadence.
- **High:** material exposure could substantially impair earnings, liquidity, moat or valuation.
- **Critical:** severe, near-term or existential threat to solvency, integrity, core business or investment thesis.
Use documented evidence and company/sector context. Do not translate probability alone into severity.

## Risk register (complete all 11)
| Risk dimension | Risk Level | Evidence | Impact | Probability | Mitigation | Monitoring Signal |
|---|---|---|---|---|---|---|
| Financial Risk |  |  |  |  |  |  |
| Balance Sheet Risk |  |  |  |  |  |  |
| Cash Flow Risk |  |  |  |  |  |  |
| Earnings Risk |  |  |  |  |  |  |
| Competitive Risk |  |  |  |  |  |  |
| Industry Risk |  |  |  |  |  |  |
| Regulatory Risk |  |  |  |  |  |  |
| Governance Risk |  |  |  |  |  |  |
| AI Disruption Risk |  |  |  |  |  |  |
| Valuation Risk |  |  |  |  |  |  |
| Macro Risk |  |  |  |  |  |  |

For each row include source/date/locator, the affected business or valuation pathway, likely time horizon, and owner of any proposed mitigation where known. If evidence has not been reviewed, write N/A and explain its confidence impact. “No risk identified” requires adequate review evidence.

## Probability and impact
State probability as a sourced, disclosed estimate or a qualitative Low / Medium / High / N/A with rationale and horizon; do not imply statistical precision without a model. Impact is the plausible consequence and financial/thesis channel, with magnitude N/A where not supportable. Severity is the combined qualitative judgment of likelihood, impact, time to harm, and reversibility. Explain judgment rather than multiplying arbitrary numbers.

## Aggregate Risk Rating
1. Rate risks individually.
2. Aggregate by the highest active level: any material Critical risk makes overall Critical; absent Critical, any material High risk makes overall High.
3. Where no High/Critical risks exist, rate overall Elevated if at least three independent Medium risks collectively threaten a key thesis dependency; otherwise rate Moderate if any material Medium risk exists; rate Low only when reviewed exposures are Low or adequately contained.
4. If a material dimension is N/A and could plausibly change the rating, label aggregate Unknown and lower data confidence. If known evidence is sufficient to establish a Critical/High issue, missing unrelated inputs do not dilute that rating.
5. Identify correlated risks and avoid counting the same underlying exposure multiple times. State any justified exception to the max-severity rule.

## Risk-control points (0–15)
Map aggregate rating to the decision engine's Risk Profile component:
| Aggregate rating | Points |
|---|---:|
| Low | 15 |
| Moderate | 12 |
| Elevated | 8 |
| High | 4 |
| Critical | 0 |
| Unknown / N/A | N/A |

Use **Elevated** only when at least three independent Medium exposures collectively threaten a key thesis dependency but do not meet the High definition. If High/Critical evidence exists, it controls the aggregate label. Points are capped by the label, so averaging mild risks cannot offset a severe one. Explain why the label applies. This is the V1.5 risk-control component, not a substitute or edit of V1.2/V1.3/V1.4.

## Mandatory override links
Apply decision/decision_rules.md. Overall Critical, a current critical governance/accounting/balance-sheet risk, two independent Critical risks, a substantiated severe solvency/integrity threat, or severe unmitigated AI disruption triggers HIGH RISK. Missing/conflicting evidence is not itself a risk finding: use INSUFFICIENT DATA or WATCHLIST according to coverage and confidence gates.

## Monitoring
For each material risk define the observable signal, source, update frequency/event, threshold or qualitative trigger, and response/research action. Do not invent thresholds; label analyst-selected monitoring thresholds ASSUMPTION and justify them. Review at each results filing, material Bursa announcement, or identified risk event.
