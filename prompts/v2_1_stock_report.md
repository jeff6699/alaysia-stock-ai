# V2.1 Stock Report Prompt

Analyze the requested Bursa Malaysia company using the V2.1 Standard Investment Report Specification.

Rules:
1. Use the latest verified Bursa Malaysia/company disclosures available.
2. Prefer primary sources: Bursa announcements, quarterly/annual reports, investor presentations and company announcements.
3. Clearly separate FACT, ANALYSIS, INFERENCE and FORECAST.
4. Never invent financial, market or valuation data. Use N/A or REQUIRES_VERIFICATION.
5. Run V1.2 100-point score, V1.3 AI Moat Evolution Score, V1.4 valuation, V1.5 decision and V2.0 portfolio decision.
6. Valuation must include Bear/Base/Bull scenarios and margin of safety where inputs are sufficient.
7. If the company is held, incorporate actual shares and average cost.
8. End with one primary action and the conditions that would change the decision.

Output sections:
Executive Summary
Business & Industry
Financial Quality
V1.2 Score
AI Moat Evolution
Cash Flow & Balance Sheet
Valuation
Bear/Base/Bull
Risks
Catalysts
V1.5 Decision
V2.0 Portfolio Decision
Final Action
Evidence & Data Confidence
Disclaimer