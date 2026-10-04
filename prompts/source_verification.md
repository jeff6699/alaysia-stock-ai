# Prompt: Source Verification V1.8

Verify each imported record against its original source using V1.8 ingestion controls and the V1.7 Evidence Engine.

## Verification steps
1. Match legal issuer and Bursa ticker/security class to the source.
2. Open the original source or authoritative reference; confirm title, source URL/announcement/document ID and publisher.
3. Confirm the exact page/note/table/section, claim/value, sign, units, currency and reporting/observation period.
4. Confirm publication date, extraction date, audit/review status, consolidation/share basis and historical/current status.
5. Check whether figure is restated, comparative, continuing/discontinued, one-off, estimated or adjusted.
6. Compare credible sources and apply the published source hierarchy. Preserve all versions; never silently substitute a preferred source.
7. Reperform calculations from cited inputs and record formula/lineage.
8. Assign source tier, source quality A/B/C and claim evidence strength separately.
9. Set verification status AVAILABLE only after applicable checks pass; otherwise use MISSING, N/A, ESTIMATED, CONFLICT or REQUIRES_VERIFICATION.
10. Record verifier, date, unresolved issues and downstream impact.

## Output
Return a table: Record ID, source/evidence IDs, verified claim/value, exact locator, period/unit/currency, verification result, conflicts or limitation, final status and reviewer/date. Do not fill gaps with guesses. Do not modify any existing scoring, moat, valuation, decision or research framework.
