# Evidence Quality Rules V1.7

## Source quality grades
Grade the source itself, separately from whether its evidence supports a particular claim.

- **A — Primary source:** Bursa Malaysia announcements and filings; issuer quarterly and annual reports; investor presentations; official company announcements and disclosures; official regulator/statistical-agency publications for their own data. Record filing/publication date, issuer/publisher, exact page/note/announcement/series and whether audited, reviewed, unaudited or management-prepared.
- **B — High-quality secondary source:** reputable broker research, established financial news, credible industry reports and reputable financial databases with disclosed provenance/methodology. Record author/publisher, date, cited underlying data and any paywall/extract limitation.
- **C — Weak secondary source:** unattributed commentary, social posts, reposts without provenance, promotional summaries, unreliable aggregators or any source where methods or underlying evidence cannot be checked. Use only as a lead for verification; do not rely on it alone for material facts, scoring, valuation or a decision.

A source grade is not a truth score. A primary presentation may be promotional or incomplete; a secondary source may reveal a conflict but must not silently override a filing. Grade each source in context and document limitations.

## Evidence strength
Rate each claim independently:
- **Strong:** exact, relevant, current for the claim, traceable to the original source, and corroborated where material or directly filed by the responsible authority.
- **Moderate:** relevant and identifiable but with limited corroboration, scope, timeliness or detail.
- **Weak:** indirect, vague, stale, unattributed, promotional or not independently verifiable.
- **Contradicted:** credible evidence materially conflicts with the claim; list both records and resolve or preserve as unresolved.
- **N/A:** insufficient information to judge; explain the gap.

For primary issuer disclosures, Strong means strong evidence that the issuer made/reported that statement, not independent proof that a forward target will occur.

## Evidence confidence
Rate research confidence HIGH / MEDIUM / LOW, not by averaging letter grades. Consider:
1. Completeness of records and required reporting periods.
2. Recency relative to the claim and decision/market date.
3. Source quality and traceability.
4. Consistency across documents and calculations.
5. Number and importance of unresolved assumptions and conflicts.

HIGH requires the critical records to be complete, current enough and substantially consistent, principally supported by A/B evidence, with few non-decision-driving gaps. MEDIUM permits bounded gaps/conflicts with explainable effects. LOW applies where key evidence is missing/stale, important claims depend on C sources, material conflicts remain unresolved, or assumptions control the conclusion. A critical unresolved item prevents HIGH confidence.

Missing evidence does not mean adverse evidence; it lowers coverage/confidence and can trigger the existing V1.2–V1.6 data gates. Do not create a confidence percentage unless a documented method requires it. Do not change any upstream scoring thresholds.

## Conflicts and source hierarchy
Apply research/evidence/source_priority.md. Preserve both sides, exact scopes and dates. A newer filing may supersede an old report for current facts, but the earlier source remains in the audit trail. If conflict cannot be resolved by scope, recency and authority, label Contradicted and mark affected downstream metric/claim N/A.

## Evidence labels and missing data
- FACT: directly source-supported observation or reproducible calculation with its inputs and formula.
- ANALYSIS: interpretation of verified facts with method and limitations.
- INFERENCE: qualified conclusion derived from evidence, including uncertainty and alternatives.
- FORECAST: conditional forward view with horizon and explicitly identified ASSUMPTIONS.
Missing evidence is MISSING and displayed as N/A with its downstream effect; do not fabricate or silently substitute a value.
