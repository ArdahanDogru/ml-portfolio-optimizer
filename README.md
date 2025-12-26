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

## Installation

### Prerequisites
- Python 3.8 or higher
- pip package manager

### Setup

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/ml-portfolio-optimizer.git
cd ml-portfolio-optimizer
```

2. **Create virtual environment** (recommended)
```bash
# macOS/Linux
python3 -m venv venv
source venv/bin/activate

# Windows
python -m venv venv
venv\Scripts\activate
```

3. **Install dependencies**
```bash
pip install -r requirements.txt
```

## Usage

### Run Analysis

1. **Launch Jupyter Notebook**
```bash
jupyter notebook
```

2. **Open** `Portfolio_Analyzer.ipynb`

3. **Run all cells** (Cell → Run All)

### Expected Outputs

- Portfolio comparison table (Equal Weight, Min Variance, Max Sharpe, Risk Parity, ML-Enhanced)
- Asset correlation heatmap
- Risk-return scatter plot with annotations
- Efficient frontier (10,000 simulated portfolios)
- Growth of $1,000 investment chart
- 60-day rolling volatility
- ML model performance (ROC-AUC, confusion matrix, feature importance)

## Customization

### Change Assets
```python
tickers = ['YOUR', 'CUSTOM', 'TICKERS']
```

### Adjust Time Period
```python
start_date = '2020-01-01'
end_date = '2024-12-01'
```

### Modify Risk-Free Rate
```python
RISK_FREE_RATE = 0.045  # 4.5% annual
```

### ML Model Parameters
```python
xgb_model = XGBClassifier(
    n_estimators=100,
    max_depth=5,
    learning_rate=0.1
)
```

## Project Structure
```
ml-portfolio-optimizer/
│
├── Portfolio_Analyzer.ipynb    # Main analysis notebook
├── README.md                    # This file
├── requirements.txt             # Python dependencies
└── .gitignore                   # Git ignore file
```

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

## Troubleshooting

**Error: "No module named 'yfinance'"**
```bash
pip install -r requirements.txt
```

**Error: "Failed to download data"**
- Check internet connection
- Verify ticker symbols are valid
- Some tickers may be delisted

**Empty plots**
- Add to first cell: `%matplotlib inline`
- Restart kernel: Kernel → Restart & Run All

## Requirements
```txt
yfinance==0.2.32
pandas==2.1.3
numpy==1.26.2
matplotlib==3.8.2
seaborn==0.13.0
scipy==1.11.4
scikit-learn==1.3.2
xgboost==2.0.3
jupyter==1.0.0
```

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
[LinkedIn](https://www.linkedin.com/in/ardahandogru/) | [GitHub](https://github.com/yourusername)

---

*Built as part of a portfolio of data science projects demonstrating machine learning, optimization, and financial analytics skills.*
