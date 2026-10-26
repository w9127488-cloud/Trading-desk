# Signal Desk

Live signals for XAU/USD, EUR/USD, GBP/USD and BTC/USD with a TradingView chart.
The server pulls prices (Yahoo Finance), computes ATR/RSI/MACD/EMA/levels, checks DXY, US10Y,
Nasdaq, Fear & Greed and the economic calendar, then scores each setup and sizes the trade.

## Run locally
    npm install
    npm start        # http://localhost:3000

## Deploy (always on)
Render, Railway or Fly.io: connect the folder or repo, build `npm install`, start `npm start`.
Use a paid or always-on instance so it does not sleep.

## Edit
- Contract sizes per lot: top of server.js (ASSETS). Match your broker's Specification.
- Stop = 1.5 x ATR(14) on H1, targets 1:2 and 1:3, threshold 58%: in analyse().

Data is unofficial and may lag or fail. Verify the price in MT5 before trading.
Confidence is a rules-based score, not a probability. Test on demo first.
