# V2.1 Standard Investment Report Specification

## Purpose
V2.1 converts the V1.x research engines and V2.0 portfolio decision layer into one standardized stock report.

## Input
- Company name
- Bursa ticker
- Research date
- Optional portfolio position: shares, average cost, current price
- Latest verified Bursa/company financial data

## Pipeline
1. Company identification and business model
2. Industry and competitive position
3. Financial statement analysis
4. Earnings quality
5. Cash flow and balance sheet
6. V1.2 100-point investment score
7. V1.3 AI Moat Evolution Score
8. V1.4 multi-method valuation
9. Risk engine
10. Catalyst engine
11. Bull/Base/Bear scenarios
12. V1.5 investment decision
13. V2.0 portfolio position decision
14. Final action

## Required valuation output
- DCF
- P/E
- FCF Yield
- SOTP when appropriate
- Bear/Base/Bull fair-value range
- Margin of Safety
- Valuation confidence
Never invent missing inputs. Use N/A or REQUIRES_VERIFICATION.

## Portfolio-aware output
If a position is supplied, report:
- shares
- average cost
- current price
- market value
- unrealized P/L
- portfolio concentration when portfolio data is available
- V2.0 state: ACCUMULATE / HOLD / WATCH / REDUCE / EXIT

## Final decision
Return exactly one primary action:
STRONG OPPORTUNITY / ATTRACTIVE / WATCHLIST / FAIRLY VALUED / OVERVALUED / HIGH RISK / INSUFFICIENT DATA

Then provide one concise portfolio action.

## Evidence discipline
Every material factual claim must have a source reference. Separate FACT, ANALYSIS, INFERENCE and FORECAST. Prefer Bursa/company disclosures. Never fabricate data.