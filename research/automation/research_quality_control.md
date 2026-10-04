# Research Quality Control V1.9

## Pre-publication gates
- Verify company name, Bursa ticker/security class and research date.
- Verify record/source metadata completeness under V1.8 and evidence linkage under V1.7.
- Verify every financial/market fact has a source, document/page or section locator, date, period, unit, currency and basis.
- Verify period, restatement, continuing/discontinued, comparative and corporate-action treatment.
- Mark unavailable data **N/A — DATA NOT AVAILABLE** and unverified evidence **REQUIRES_VERIFICATION**.
- Preserve CONFLICT records; do not silently choose or average conflicting figures.
- Separate FACT, ANALYSIS, INFERENCE, FORECAST and analyst ASSUMPTIONS.
- Ensure no forecast or management target is described as an accomplished fact.
- Confirm evidence quality and research confidence use V1.7 rules; no false precision.
- Confirm all results/outputs cite the unchanged upstream module and version.

## Upstream integrity
- V1.2 100-point quality score: source modules and original weights/coverage rules unchanged.
- V1.3 AI Moat: source modules and original score/durability/trajectory rules unchanged.
- V1.4 valuation: method selection, assumptions and formulas unchanged.
- V1.5 risk/catalyst/scenario/decision rules and overrides unchanged.
- V1.6 research pipeline/report structure remains a source assembly framework.
- V1.7 evidence grades/schema and V1.8 ingestion statuses/hierarchy/period rules remain unchanged.
V1.9 orchestration or formatting must never rewrite these methodologies.

## Research confidence controls
Rate each of the six required factors HIGH / MEDIUM / LOW with rationale. Do not average them. Any material unresolved identity, financial source, period or conflict issue prevents overall HIGH. A low critical factor prevents an overly confident final conclusion; apply V1.5 decision gates and report limitations.

## Release checklist
- [ ] Input company, ticker and research date shown.
- [ ] Sixteen workflow steps completed in specified order or marked blocked/N/A with reason.
- [ ] All required 21 output sections present; requested report sections are complete.
- [ ] Financial analysis, earnings quality and cash flow are separate.
- [ ] AI Moat uses V1.3 and valuation uses V1.4.
- [ ] Risk/catalysts/scenarios/decision use V1.5.
- [ ] Scenario probabilities total exactly 100% for standard final decision.
- [ ] 100-point quality score is V1.2 output, not a V1.9 duplicate.
- [ ] Evidence IDs resolve to sources and locators or are explicitly unverified.
- [ ] Source quality, evidence gaps, conflicts and confidence are explained.
- [ ] No fabricated financial data; all unknowns marked N/A.
- [ ] Source list and methodology versions included.
