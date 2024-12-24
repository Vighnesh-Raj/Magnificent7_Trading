# Magnificent 7 Portfolio Analysis

## Overview
This project showcases two distinct trading strategies applied to the "Magnificent 7" stocks: AAPL, MSFT, TSLA, GOOGL, NVDA, META, and AMZN. Using data from Alpaca API, the project evaluates the performance of these strategies over 2024.

## Strategies

### 1. Equal-Weight Strategy
- **Description**: An equally weighted portfolio is constructed with daily rebalancing to maintain equal allocation across all seven stocks.
- **Objective**:
  - Compute cumulative returns over the sample period.
  - Visualize portfolio growth assuming an initial investment of $10,000.
- **Methodology**:
  1. Fetch daily price data using Alpaca API.
  2. Calculate daily returns and rebalance weights equally among all stocks.
  3. Compute cumulative portfolio returns.
  4. Plot portfolio growth.

### 2. Lowest Residual Return Strategy
- **Description**: Stocks are ranked daily based on their residual returns. The portfolio is allocated entirely to the stock with the lowest residual return, rebalancing at the end of each trading day.
- **Objective**:
  - Compute alpha (α) and beta (β) for each stock.
  - Evaluate the portfolio’s performance based on residual returns.
- **Methodology**:
  1. Perform regression analysis to calculate residual returns for each stock.
  2. Rank stocks by residual returns daily.
  3. Allocate the portfolio to the lowest residual return stock and rebalance daily.

## Comparative Analysis

| Metric                        | Equal-Weight Strategy            | Lowest Residual Return Strategy |
|-------------------------------|-----------------------------------|---------------------------------|
| Cumulative Return             | Moderate                         | High                            |
| Portfolio Volatility          | Low                              | High                            |
| Risk-Adjusted Performance     | Balanced                         | Potentially higher risk-adjusted returns |
| Diversification               | High (equal exposure to 7 stocks)| Low (single stock exposure)     |
| Computational Complexity      | Moderate                         | High                            |

### Key Insights
- The Equal-Weight Strategy provides stable returns with lower risk due to diversification.
- The Lowest Residual Return Strategy can yield higher returns but is more volatile and concentrated.

## Results
- Detailed visualizations of portfolio growth for both strategies.
- Performance metrics (e.g., Sharpe ratio, alpha, beta) to compare strategies.

## Setup and Usage

### Prerequisites
- Python 3.8+
- Libraries:
  - `alpaca-trade-api`
  - `pandas`
  - `numpy`
  - `matplotlib`
  - `statsmodels`

### Steps to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/Vighnesh-Raj/Magnificent7_Trading.git
   ```
2. Navigate to the project directory:
   ```bash
   cd Magnificent7_Trading
   ```
3. Install the required libraries:
   ```bash
   pip install -r requirements.txt
   ```
4. Run the Jupyter Notebook:
   ```bash
   jupyter notebook LRRmag7.ipynb
   ```

### API Configuration
Replace the placeholders in the notebook with your Alpaca API credentials:
```python
API_KEY = 'your_api_key'
SECRET_KEY = 'your_secret_key'
```

## Repository Structure
```
Magnificent7_Trading/
├── ff-monthly.csv              # Fama_French  data
├── LRRmag7.ipynb               # Jupyter notebook for analysis
├── README.md                   # Project documentation
└── requirements.txt            # Python dependencies
```

## Future Improvements
- Incorporate additional risk metrics (e.g., maximum drawdown, Sortino ratio).
- Test alternative weighting strategies (e.g., market-cap weighted).
- Automate daily data updates and strategy execution.

## Contact
For inquiries or collaboration opportunities, feel free to reach out!


