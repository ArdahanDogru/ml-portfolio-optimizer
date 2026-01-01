# ML Portfolio Optimizer

Portfolio optimization combining Modern Portfolio Theory with machine learning for data-driven investment analysis.

## Overview

Python-based system that uses ensemble machine learning (XGBoost, Random Forest) alongside traditional optimization methods to construct efficient portfolios. Analyzes multi-asset portfolios across sectors with comprehensive risk-return metrics.

## Key Features

**Traditional Optimization:**
- Multiple strategies: Minimum Variance, Maximum Sharpe Ratio, Risk Parity
- Efficient frontier visualization (10,000 Monte Carlo simulations)
- Benchmark comparison vs S&P 500 (SPY)

**Machine Learning Component:**
- XGBoost & Random Forest models for asset selection (0.63 ROC-AUC)
- Feature engineering: momentum, volatility, RSI, market correlation
- Time-based train-test split with proper backtesting
- Feature importance analysis

**Risk Analytics:**
- Sharpe ratio (risk-adjusted returns)
- Rolling volatility analysis
- Growth of $1,000 simulations
- Correlation heatmaps

## Results

**Portfolio Performance (Test Period):**
- **Min Variance:** 23% volatility reduction vs equal-weighting
- **Max Sharpe:** Optimal risk-return tradeoff
- **ML-Enhanced:** 0.63 ROC-AUC predicting outperformance

**Analysis Coverage:**
- 15+ assets across 5 sectors (Tech, Finance, Retail, Healthcare, Energy)
- 500+ trading days of historical data
- Multiple time horizons (5-day, 20-day, 60-day features)

## Tech Stack

**Core:** Python | Pandas | NumPy | SciPy  
**ML:** XGBoost | Scikit-learn | Random Forest  
**Visualization:** Matplotlib | Seaborn  
**Data:** yfinance API


### Expected Outputs

- Portfolio comparison table (Equal Weight, Min Variance, Max Sharpe, Risk Parity, ML-Enhanced)
- Asset correlation heatmap
- Risk-return scatter plot with annotations
- Efficient frontier (10,000 simulated portfolios)
- Growth of $1,000 investment chart
- 60-day rolling volatility
- ML model performance (ROC-AUC, confusion matrix, feature importance)

## Methodology

### Traditional Optimization
1. **Modern Portfolio Theory (MPT)** - Markowitz mean-variance optimization
2. **Constraint optimization** - SciPy minimize with bounds and constraints
3. **Risk metrics** - Sharpe ratio, volatility, correlation analysis

### Machine Learning Pipeline
1. **Feature Engineering** - Create predictive features from price/return data
2. **Target Definition** - Binary classification (outperform SPY in next 20 days?)
3. **Train-Test Split** - Time-based split (prevents data leakage)
4. **Model Training** - Compare Logistic Regression, Random Forest, XGBoost
5. **Evaluation** - ROC-AUC, confusion matrix, feature importance
6. **Portfolio Construction** - Weight assets by prediction confidence


## Future Enhancements

- [ ] Additional ML models (LightGBM, CatBoost)
- [ ] More technical indicators (MACD, Bollinger Bands)
- [ ] Transaction cost modeling
- [ ] Regime detection (bull/bear markets)
- [ ] Real-time data integration
- [ ] Interactive Plotly dashboards

## Author

**Yusuf Ardahan Dogru**  
Data Science Graduate Student | University of Texas at Dallas  
[LinkedIn](https://www.linkedin.com/in/ardahandogru/) | [GitHub](https://github.com/ArdahanDogru)

---

*Built as part of a portfolio of data science projects demonstrating machine learning, optimization, and financial analytics skills.*
