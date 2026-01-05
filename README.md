# MacroVolatilityOverlay

This project is a Python backtest for a macro volatility overlay strategy across KC, SPX, and EUR/USD, including realistic execution delay and slippage.

## Strategy Overview

- Objective: Harvest volatility risk premia and tail convexity in macro instruments.
- Trade Type: Iron Condors and ATM straddles.
- Time Horizon: 30-day options.
- Position Sizing: €150k notional per product.
- Execution Model: Includes realistic broker execution delay. The bid/ask slippage (0.1%).

## Usage

Please use the following python scripts for best free usage of the data sets you will need. Quandl (https://data.nasdaq.com/?utm_source) and specific Brokerage Exchange data will have paywalls.'

import yfinance as yf
kc = yf.download("KC=F", start="2023-01-01", end="2025-09-01") kc[['Close']].to_csv("data/kc.csv", index_label='date')
spx = yf.download("^GSPC", start="2023-01-01", end="2025-09-01") spx[['Close']].to_csv("data/spx.csv", index_label='date')
eurusd = yf.download("EURUSD=X", start="2023-01-01", end="2025-09-01") eurusd[['Close']].to_csv("data/eurusd.csv", index_label='date')
