# Prompt: Fact vs Analysis V1.7

Review a draft Malaysian stock research report and enforce strict separation between FACT, ANALYSIS, INFERENCE and FORECAST.

## Review process
1. Split compound sentences into atomic claims.
2. For each claim, identify its label, source/evidence ID, locator, date, period, unit and reporting basis.
3. Verify FACT is directly supported; if a claim is derived, include formula and all inputs and identify it as a calculated fact.
4. Verify ANALYSIS interprets cited facts and states comparison method/caveats.
5. Verify INFERENCE shows its evidential chain, alternative explanations and uncertainty.
6. Verify FORECAST identifies horizon, source facts, all ASSUMPTIONS, dependencies and uncertainty; do not state it as fact.
7. Check source grade A/B/C separately from evidence strength.
8. Flag missing, contradictory, stale, restated, mismatched-period, currency/unit or unsupported claims. Replace unavailable specifics with N/A, not a plausible invented value.
9. Ensure company targets/management statements are reported as facts about the statement, not proven future outcomes.
10. Check that V1.2–V1.6 scores, valuation formulas, decision thresholds and outputs have not been changed.

## Output
Provide a table with: draft claim, current label, proposed label, evidence ID/source/locator, issue, correction or N/A handling, and downstream confidence impact. Conclude with unresolved conflicts and overall evidence confidence. Never manufacture citations while editing.
