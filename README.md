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

### Prerequisites
- Python 3.8 or higher
- pip package manager

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/portfolio-optimizer.git
cd portfolio-optimizer
```

2. **Create a virtual environment (recommended)**
```bash
# On macOS/Linux
python3 -m venv venv
source venv/bin/activate

# On Windows
python -m venv venv
venv\Scripts\activate
```

3. **Install required packages**
```bash
pip install -r requirements.txt
```

### Running the Analysis

1. **Launch Jupyter Notebook**
```bash
jupyter notebook
```

2. **Open `Portfolio_Analyzer.ipynb`**

3. **Run all cells** (Cell → Run All, or press Shift+Enter through each cell)

### Expected Output
- Portfolio metrics comparison table
- Correlation heatmap
- Risk-return scatter plot
- Efficient frontier visualization
- Growth of $1,000 chart
- Rolling volatility analysis

### Customization

**To analyze different stocks/ETFs:**
Edit the `tickers` list in the "Get tickers" cell:
```python
tickers = ['YOUR', 'CUSTOM', 'TICKERS', 'HERE']
```

**To change the time period:**
Edit the date range in the "Get Data" cell:
```python
start_date = '2020-01-01'
end_date = '2024-12-01'
```

**To adjust risk-free rate:**
Edit the constant at the top:
```python
RISK_FREE_RATE = 0.045  # 4.5% annual rate
```

### Troubleshooting

**Error: "No module named 'yfinance'"**
- Make sure you activated your virtual environment
- Run: `pip install -r requirements.txt`

**Error: "Failed to download data"**
- Check your internet connection
- Verify ticker symbols are correct
- Some tickers may be delisted or have limited data

**Empty plots showing up**
- Run: `%matplotlib inline` at the top of the notebook
- Restart kernel and run all cells

### Requirements.txt

Create a file named `requirements.txt` with:
```
yfinance==0.2.32
pandas==2.1.3
numpy==1.26.2
matplotlib==3.8.2
seaborn==0.13.0
scipy==1.11.4
jupyter==1.0.0
```

### Optional: Run from Command Line

Convert notebook to Python script:
```bash
jupyter nbconvert --to script Portfolio_Analyzer.ipynb
python Portfolio_Analyzer.py
```

