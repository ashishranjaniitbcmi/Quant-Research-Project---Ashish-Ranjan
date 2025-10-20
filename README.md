# Quantitative Research Project – Volatility Pairs Trading: Bank Nifty & Nifty

This repository contains a **quantitative research project** exploring volatility pairs trading using Bank Nifty and Nifty implied volatilities. The project investigates how the volatility spread between these indices fluctuates and reverts to the mean, allowing for trading opportunities.

## Project Overview

We implemented and analyzed two trading strategies:

1. **Dynamic Z-Score Strategy (Base Model)**  
   - Uses rolling statistics of the volatility spread to detect deviations from the mean.  
   - Positions are dynamically scaled based on recent spread volatility.  
   - Generates frequent trades and provides moderate risk-adjusted returns.

2. **Kalman Residual Strategy (Improved Model)**  
   - Uses a Kalman filter to estimate a dynamic hedge ratio between Bank Nifty and Nifty.  
   - Trades are based on residuals and adaptive thresholds.  
   - Fewer trades but higher win rate and significantly improved risk-adjusted performance.

## Dataset

- Minute-level implied volatility (IV) data for Bank Nifty and Nifty.  
- Includes **Time to Expiry (TTE)** for options.  
- Covers standard Indian market hours: **09:15 – 15:30**.  
- Missing values have been appropriately handled.

## Key Features

- Profit/loss calculations consider both spread magnitude and time to expiry.  
- Performance evaluation using **absolute returns, Sharpe ratio, max drawdown, win rate, and trade count**.  
- Visualization of cumulative PnL for both strategies.  
- Well-structured, commented Python notebooks suitable for replication and further research.

## Repository Structure
- `Quant_project-report.pdf` - Report of implementations of models
- `README.md` – Project description and instructions.
- `ZScore_Strategy.ipynb` – Implementation of the dynamic Z-Score strategy.  
- `Kalman_Strategy.ipynb` – Implementation of the Kalman residual strategy.  
- `data.parquet` – Input dataset (minute-level IVs).  

## Author

**Ashish Ranjan**  
Email: 25n0086@iitb.ac.in
