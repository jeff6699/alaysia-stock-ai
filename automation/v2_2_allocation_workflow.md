# V2.2 Portfolio Allocation Workflow

## Data and decision flow
Portfolio data  
→ Market data  
→ Financial data  
→ V1.2 Quality Score  
→ V1.3 AI Moat  
→ V1.4 Valuation  
→ V1.5 Investment Decision  
→ V2.0 Portfolio Decision  
→ V2.1 Stock Report  
→ V2.2 Allocation Engine  
→ Allocation Report

Each arrow passes versioned source-linked inputs and status metadata; no upstream framework is recalculated in the V2.2 layer. V2.2 is decision support only and has no automatic trading/execution step.

## Allocation run
1. Freeze portfolio valuation date, research date, currency, share basis, source IDs and policy configuration.
2. Validate holdings, shares, average cost, current price/date, market value, NAV, cash and weights. Reconcile differences or mark CONFLICT/REQUIRES_VERIFICATION.
3. Load V1.2–V2.1 outputs with version, date, coverage and evidence. Missing critical outputs block new allocations for the affected candidate.
4. Calculate current issuer, sector, bank, REIT, thematic and correlated concentrations from verified look-through data.
5. Calculate each V2.2 score and N/A coverage. Apply score/action thresholds, upstream overrides, MOS and confidence gates.
6. Rank eligible candidates; compute target headroom and cash budget. Enforce all caps and the minimum reserve.
7. Run post-allocation arithmetic checks; publish report tables, rejected-candidate reasons, evidence and uncertainty.
8. No trade is transmitted or executed; the user decides separately.

## Monitoring and rerun triggers
| Trigger | Monitoring | Required response |
|---|---|---|
| Daily monitoring | Check available cash, dated market data freshness and configured portfolio limits when reliable data are supplied; do not imply unattended live feed exists | Refresh/label stale data; rerun only when an input materially changes |
| Earnings update | New quarterly/annual filing, earnings release or material guidance | Ingest V1.8 source, update V1.7 evidence, rerun financial/earnings/cash-flow and dependent engines |
| Material price movement | User-configured threshold, material change in price/MOS or stale quote correction | Recheck V1.4 valuation inputs, position weights and cash allocation; price fall alone is not a buy trigger |
| Valuation threshold | Current MOS crosses V1.4 required MOS, buy-below ceiling or user-configured watch threshold | Apply V1.4 output and V2.2 WAIT/eligibility gates; thresholds are configurable ASSUMPTIONS |
| Portfolio concentration | Position/sector/bank/REIT/theme reaches configured alert or cap | Block additions at cap; notify for review; do not automatically sell |
| Major company announcement | Bursa/company announcement changes business, capital, dividend, regulation, contract, acquisition, governance or thesis | Capture source metadata, assess impact and rerun affected analyses |
| Risk deterioration | V1.5 risk level/override, V2.0 state, solvency, governance, earnings quality or cash-flow signals worsen | Apply restrictive V1.5/V2.0/V2.2 gates; require human review |

## Trigger records and safety
For every run store timestamp, trigger, prior/new input versions, source IDs, rule/config version, output report and reviewer. If live data/integration is not configured, daily monitoring is a checklist or user-supplied snapshot, not a claim of automatic continuous monitoring. Never fabricate price/financial data. No trigger can place or execute an order.

No automatic trade execution is performed by this workflow.
