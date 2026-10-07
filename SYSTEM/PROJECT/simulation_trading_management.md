# Simulation Trading Management

## Status

This is the permanent operating rule for simulated trading in the repository.

- It is a **management / operating specification**, not a new product version.
- Do not create V1, V2, V3, V2.1, V2.2 or similar versions for this simulation workflow.
- Improvements to the workflow are made in place only when there is a demonstrated problem, contradiction, or materially better rule.
- Do not create a new simulation engine, framework, or project merely because a new stock, trade, metric, or idea appears.

## Purpose

The simulation system exists to test whether the trading framework can be executed consistently and whether the resulting trades show a measurable statistical edge.

It is separate from company research:

- **SYSTEM / PROJECT** = how simulated trading is done.
- **REPORTS / COMPANY** = what was researched about a company.
- Individual simulated trade records are operational data and must not be mixed into company research reports.

## Relationship to Existing Repository Rules

This document is an orchestration layer. It does not replace the existing decision, risk, portfolio, valuation, or company-research rules.

Use the existing repository rules for their respective jobs:

- decision rules -> investment decision logic
- risk engine / position rules -> risk and position constraints
- portfolio rules -> portfolio-level allocation and concentration
- company reports -> company facts and research evidence

Simulation applies those rules to a hypothetical trade and records the outcome.

Do not duplicate the same rule in multiple files unless a cross-reference is necessary.

## Fixed Simulation Workflow

Every simulated trade follows this order:

1. **Opportunity**
2. **Entry**
3. **Stop**
4. **1R**
5. **Position Size**
6. **Target / R-R**
7. **Statistical Edge**
8. **Execution**
9. **Monitoring**
10. **Exit**
11. **Trade Journal**
12. **Aggregate Statistics**

The order is fixed to prevent hindsight bias: never see a price move first and then invent the reasons for the trade.

## Opportunity Checklist

Evaluate the five opportunity components:

- **Trend** — is the trend supportive?
- **Volume** — does volume support the move?
- **Breakout** — has a meaningful level been broken?
- **Momentum** — is price momentum supportive?
- **Catalyst** — is there a reason for the move to occur now, such as earnings, orders, policy, products, or industry events?

The framework is strongest when multiple conditions align. A single attractive chart is not sufficient by itself.

## Risk Construction

Before deciding position size, define:

- Entry
- Stop
- Per-share risk
- Maximum permitted loss / risk budget
- 1R
- Position Size

Core rule:

> Decide the maximum acceptable loss first, then derive position size.

Do not buy a quantity first and invent the stop afterwards.

If the risk budget is not supplied or cannot be justified, do not silently assume one. Mark the trade as incomplete and request the missing input.

## R/R and Target

Record:

- Entry
- Stop
- Target
- Risk per share
- Potential reward
- R/R

R/R is not a standalone buy signal. It must be considered together with the quality of the opportunity, historical win rate, average win, average loss, expectancy, and transaction costs where available.

## Statistical Validation

For the simulation ledger, maintain:

- Win Rate
- Average Win (R)
- Average Loss (R)
- Expectancy (R/trade)
- Maximum Drawdown (R)
- Maximum Consecutive Losses

Expectancy is calculated as:

> Win Rate × Average Win − Loss Rate × Average Loss

Do not declare the trading method successful from one or a few trades. Statistical conclusions require an adequate sample of completed trades.

## Trade States

Each simulated trade must have one clear state:

- **PLANNED** — setup identified but not entered
- **OPEN** — simulated position entered and being monitored
- **CLOSED-WIN** — closed with positive realized R
- **CLOSED-LOSS** — closed with negative realized R
- **CLOSED-FLAT** — closed around 0R
- **REJECTED** — setup failed the entry criteria before entry
- **CANCELLED** — planned setup invalidated before entry

Do not rewrite a rejected or cancelled setup as if it had been an actual trade.

## Minimum Trade Record

Each entered simulated trade should record, when available:

- trade date / time
- ticker / company
- entry price
- stop price
- 1R
- position size
- target price
- R/R
- Trend result
- Volume result
- Breakout result
- Momentum result
- Catalyst result
- reason for entry
- invalidation condition
- exit price
- exit date / time
- realized P/L
- realized R
- final state
- brief post-trade review

Missing information must remain explicitly marked as missing. Do not manufacture values.

## Monitoring and Exit

After entry, monitoring is based on the original trade plan.

A change in price alone does not justify rewriting the original thesis.

When the stop, target, invalidation condition, or other predefined exit condition is reached, record the event and outcome. If the plan is changed during the trade, record the change and the reason rather than silently replacing the original plan.

## Simulation Integrity Rules

1. Simulation is hypothetical. It must never be presented as an executed live order.
2. Every entry must have a timestamp or identifiable market session.
3. Entry, stop and target must be defined before judging the outcome.
4. Do not move the stop retrospectively just to improve the result.
5. Do not remove losing trades from the ledger.
6. Do not convert a missed trade into a simulated trade after the move unless it is explicitly labelled as a retrospective study.
7. Do not use future information that was unavailable at the simulated entry time.
8. Separate **FACT**, **ANALYSIS**, **INFERENCE**, and **FORECAST** when external research is used.
9. A catalyst must be evidenced where possible; price movement alone is not a catalyst.
10. One trade is one observation. Do not over-generalize from it.

## Storage Rules

### System rules

Store simulation methodology, workflow, definitions, checklists, and governance under:

SYSTEM / PROJECT

This file belongs there.

### Company research

Store company-specific research, financials, catalysts, risks, valuation, and investment reports under:

REPORTS / COMPANY

Do not place company reports inside the system-rules area.

### Operational simulation records

When simulation records are eventually persisted in the repository, keep them as operational trading data (for example under a dedicated simulation data area) rather than mixing them with company research or system rules.

The first priority is a clean ledger; do not create multiple storage formats without a demonstrated need.

## No-Version / Anti-Complexity Policy

This is the most important management rule.

### Do not create a new version because:

- another stock is added
- another trade is opened
- another metric is requested
- a new company report is created
- a normal bug or typo is fixed
- a better explanation is found
- the user asks for a different view of the same data

### A structural change is allowed only when:

1. the existing workflow cannot represent a required case,
2. the problem is demonstrated with an actual example,
3. the change has been reviewed against existing decision/risk/portfolio rules,
4. the change reduces complexity or materially improves reliability,
5. the change does not duplicate an existing rule.

Even then, update the existing specification in place. Do not create a new version number.

### No parallel systems

There must be one canonical simulation workflow.

Do not create:

- a second simulation framework
- a second trade-plan template
- a second risk formula
- a second simulation engine
- a new project for the same purpose
- duplicate rules under different filenames

If two rules overlap, consolidate them instead of adding another layer.

## Daily Operating Principle

The user should interact with the AI in the simulation chat using natural requests such as:

- “分析 XXX”
- “这只可以进吗”
- “记录 XXX 进场”
- “更新这笔模拟交易”
- “检查止损 / 目标”
- “总结目前模拟交易”
- “统计胜率、Expectancy、最大回撤”

The AI is responsible for applying the canonical workflow and maintaining consistency. The user does not need to operate GitHub or Codex for routine simulation.

GitHub is the durable backend record of the rules; the simulation chat is the primary working interface.

## Change Control

Only make a repository change when there is a concrete reason.

For every rule change, record:

- date
- what changed
- why it changed
- evidence / problem that triggered the change
- whether existing trade records are affected

Do not use version numbers. The goal is a stable system with controlled in-place maintenance, not continuous version expansion.

## Canonical Summary

> Opportunity -> Entry -> Stop -> 1R -> Position Size -> R/R -> Statistical Edge -> Execution -> Monitoring -> Exit -> Journal -> Statistics

The simulation system is complete when it can execute and record this loop consistently. More modules are not automatically better.
