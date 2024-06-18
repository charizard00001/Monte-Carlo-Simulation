# Monte Carlo Simulation for Portfolio Optimization

## Overview
In today's volatile financial markets, optimizing an investment portfolio is essential to achieve the desired balance between risk and return. Monte Carlo simulations offer a powerful tool to assess different asset allocation strategies and their potential outcomes under uncertain market conditions.

## Objective
The objective of this project is to develop a Monte Carlo simulation model for portfolio optimization. Participants will be required to construct and analyze portfolios composed of various asset classes (e.g., stocks, bonds, and alternative investments) to maximize expected returns while managing risk.

## Model
### Data Collection & Pre-Processing
- Collected data from Kaggle about asset prices and used CSV files for analysis. Alternatively, you can use `yfinance` to get access to real-time stock prices within a fixed time frame (between start & end date).
- Focused on analyzing the 'Adjusted Close' prices of the stocks to account for factors affecting stock prices after market closure.

### Visualization
- Plotted a heatmap of Covariance and Correlation to understand relationships between stocks and to aid in portfolio diversification.
- Created scatter plot matrices using Seaborn’s `pairplot()` function to visualize pairwise relationships and patterns between daily returns of different companies.

### Log Returns vs Simple Returns
- Preferred log returns over simple returns for their time-additive property and normal Gaussian distribution characteristics.
- Demonstrated normality assumptions and deviations using histograms and statistical tests.

### Simple Moving Average (SMA)
- Incorporated moving averages to eliminate fluctuations and reduce variations in the data, using 10, 20, and 30-day periods.
- Observed smoother lines with longer periods, indicating reduced sensitivity to short-term fluctuations.

### Calculating Returns and Distribution
- Calculated daily returns for each company and visualized the distribution using histograms, showing approximate normal distribution characteristics.

### Random Shares, Combinations, and Max Sharpe Ratio
- Developed functions `randomPortfolio()`, `IncomePortfolio(Rand)`, and `RiskPortfolio(Rand)` to generate random portfolios and calculate income and risk metrics.
- Evaluated 10,000 portfolio combinations to identify the optimal portfolio with the highest Sharpe ratio, providing a visual representation of the risk-income relationship.

### Future Price Predictions using Monte Carlo Simulation
- Implemented a function `monte_carlo` using arithmetic Brownian motion to simulate future stock prices.
- Conducted Monte Carlo analysis on Twitter’s stock through 1,000 simulations, visualizing potential future price ranges with histograms and statistical annotations.

## Further Recommendations
- Incorporate measures of normality like Q-Q plots, Box Plots, and the Kolmogorov-Smirnov Test for better data analysis.
- Use Exponential Moving Average (EMA) for more responsive price tracking.
- Experiment with different moving average periods to observe their effects on smoothening.
- Explore other Risk-Return measures such as the Sortino Ratio, M2 Ratio, and Calmar Ratio.
- Use Geometric Brownian Motion (GBM) instead of Arithmetic Brownian Motion (ABM) for generating random paths in Monte Carlo simulations.
- Analyze the impact of changing risk factors on the optimal portfolio.
