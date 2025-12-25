# Portfolio Optimizer

## Overview
A Python-based portfolio optimization tool that constructs efficient portfolios using Modern Portfolio Theory. Compares multiple optimization strategies against market benchmarks.

## Key Features
- Optimization methods (Min Variance, Max Sharpe, Risk Parity)
- Risk metrics (Sharpe, CAGR, Max Drawdown, Calmar)
- Efficient frontier visualization
- Benchmark comparison vs ETFs and ETF-based portfolios
- Backtesting on out-of-sample data

## Results Snapshot
- **Optimized portfolio**: 18.5% CAGR, -12% max drawdown
- **S&P 500**: 14.2% CAGR, -18% max drawdown
- **Improvement**: +4.3% return with 33% less drawdown

## Tech Stack
Python | Pandas | NumPy | SciPy | Matplotlib | yfinance

## How to Run
[instructions]
```

## 6) Risk Parity - Let Me Explain

**Traditional portfolios** allocate by dollar amount (e.g., 60% stocks, 40% bonds).

**Risk Parity** allocates so that each asset contributes **equally to total portfolio risk**.

**The Problem It Solves:**
In a 60/40 stocks/bonds portfolio:
- Stocks contribute ~90% of the risk (they're more volatile)
- Bonds contribute ~10% of the risk
- So you're not really diversified by risk, just by dollars

**Risk Parity Solution:**
Give each asset a weight such that:
```
Risk Contribution₁ = Risk Contribution₂ = ... = Risk Contributionₙ
