# Malaysia Stock AI

AI Investment Research Database for Malaysian stocks.

## Goal
Build a scalable research system that can support thousands of Bursa Malaysia companies while keeping company research, financial data, valuation, risk, moat analysis and content assets structured and reusable.

## Core principles
- One company = one canonical research record
- Separate raw sources from normalized research
- Separate facts, analysis, inference and forecasts
- Quarterly updates should preserve historical data
- Content assets should link back to underlying research
- Automation should operate on predictable schemas

## Planned structure
- companies/ — company master records
- financials/ — normalized quarterly/annual financial data
- research/ — investment research
- valuation/ — valuation models and scenarios
- risks/ — legal, balance-sheet and business risks
- moat/ — AI Moat / competitive advantage assessments
- sources/ — source metadata and references
- content/ — Xiaohongshu/TikTok/other content assets
- templates/ — reusable research templates
- automation/ — workflows and agents
- indexes/ — searchable company and sector indexes

## Scale target
Designed from the beginning for 1,000+ companies and long-term historical data.
