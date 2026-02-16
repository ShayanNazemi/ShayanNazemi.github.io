---
title: "Crypto Arbitrage"
subtitle: "Cross-venue arbitrage under execution uncertainty"
summary: "A microstructure-aware cross-exchange arbitrage system with depth-aware order placement, risk controls, and backtest/replay."
featured: true
order: 1
role: "Sole author"
status: "Active"
tags: ["Microstructure", "Execution", "Arbitrage", "Risk", "Backtesting"]
stack: ["Python", "WebSockets", "Order Books", "Async IO"]
links:
  - label: "Contact me"
    href: "mailto:you@email.com"
---

## Problem

Crypto markets are fragmented across venues. Cross-venue spreads can exist, but realized edge is sensitive to:
- fees and rebates
- top-of-book vs depth conditions
- fill probability and partial execution
- adverse selection and inventory risk

## Approach

- Compute executable spreads after fees.
- Model expected slippage using order book depth and target size.
- Choose price levels and sizes under margin + risk constraints.
- Enforce safeguards: position limits, max notional, and kill-switch logic.

## System design

**Components**
- Market data ingestion (multi-venue)
- Normalized order book state + snapshots
- Signal layer (executable spread + filters)
- Execution layer (price/size selection, order routing)
- Risk manager (limits, inventory skew, throttles)
- Logging + metrics

> Add an architecture diagram here (PNG/SVG) once you have it.

## Execution logic (high level)

Pseudo:
- Identify target venue(s) and side given spread.
- Determine price ladder from current book (levels N).
- Estimate fill probability and impact by level.
- Allocate size across levels subject to max order size and risk limits.

## Backtesting / evaluation

Metrics tracked:
- realized vs theoretical spread capture
- slippage and fee drag
- fill rate, partial fill rate
- drawdown, turnover, and stability across regimes

## Limitations & next steps

- Latency modeling and queue position are approximated in replay
- Improving regime detection + volatility-aware sizing
- More robust inventory skewing & unwind logic
