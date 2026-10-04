# Portfolio Schema V2.0

## Purpose
Define the minimum structured record required for portfolio-level analysis.

## Position fields
- ticker
- company_name
- market
- sector
- shares
- average_cost
- current_price
- market_value
- portfolio_weight
- thesis_status
- investment_horizon
- last_review_date

## Research-linked fields
- fundamental_score
- moat_score
- valuation_score
- decision_score
- risk_level
- catalyst_status
- fair_value_base
- margin_of_safety
- evidence_status

## Data rules
- Never invent missing values; use N/A.
- Separate FACT, ANALYSIS, INFERENCE and FORECAST.
- Every decision-critical field must have a source or be explicitly marked unavailable.
- Current price and market value must be timestamped.
