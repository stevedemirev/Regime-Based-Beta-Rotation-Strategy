# Regime-Based-Beta-Rotation-Strategy
Repository for the RBBR strategy backtest — developed as part of the CFRM 523: Advanced Trading Systems course at the University of Washington.

## Strategy Overview
This strategy aims to dynamically allocate capital between high-beta and low-beta equities based on prevailing interest rate regimes. The core hypothesis is that:

* In low-interest rate environments, firms are more likely to pursue growth, increase leverage, and take on risk, leading to stronger performance among high-beta stocks.
* In high-interest rate environments, firms become more conservative, reduce liabilities, and prioritize stability which favors low-beta, defensive equities.

By identifying shifts between "low" and "high" interest rate regimes using a rolling median of the Federal Funds Rate, the portfolio adapts its equity exposure accordingly:

* Low-rate regimes: Allocate to 10 highest-beta S&P 500 stocks

* High-rate regimes: Allocate to 10 lowest-beta S&P 500 stocks

Portfolios are rebalanced at a fixed frequency and evaluated using total return, Sharpe ratio, and drawdown metrics relative to SPY and static beta strategies.
