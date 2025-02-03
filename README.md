# SPX Options Trading Strategy

## Overview
This strategy leverages **AI predictions**, the **Martingale method**, and **Iron Condor** to trade SPX options efficiently. By analyzing market trends, the AI predicts potential movements, allowing for strategic entries and exits to maximize profitability while managing risk.

## Strategy Components
### 1. **AI Market Prediction**
- AI analyzes market trends and volatility to predict direction.
- Predictions are generated daily at **12:55 PM (before market close)**.
- Based on the forecast, options positions are structured accordingly.

### 2. **Martingale Method**
- If the initial trade results in a loss, the position size is doubled to recover losses in subsequent trades.
- Risk is managed by setting a **50% stop-loss** at each step.
- Implementation:
  - **Day 1:** Buy 1 CALL & 1 PUT ($1,000 each, total $2,000). If loss = **-$1,000**.
  - **Day 2:** Double to 2 CALLs & 2 PUTs ($4,000 total). If loss = **-$2,000**.
  - **Day 3:** Double again to 4 CALLs & 4 PUTs ($8,000 total). If loss = **-$4,000**.
  - If market moves strongly, potential profit is **100%+**.

### 3. **Iron Condor for Stability**
- Used when AI predicts a **sideways market**.
- Sell an Iron Condor with short strikes near expected price range.
- Generates **premium income** while limiting risk.
- Profits from low volatility conditions.

## Trade Execution
- **Entry:** 12:57 PM (before market close)
- **Exit:** Before 7:30 AM (market open next day)
- **Option Expiration:** Next day
- **Price Limit:** ≤ $10 per contract
- **Minimum Capital Required:** $14K+

## Risk Management
- **Stop-loss:** 50% per trade
- **Diversification:** Mix of directional trades (Martingale) and neutral trades (Iron Condor)
- **AI Adjustment:** AI adapts predictions based on new data

## Expected Outcomes
### **Best-Case Scenario (Strong Market Movement)**
- At least **100% profit** on directional trades.
- Iron Condor expires worthless, keeping premium.

### **Worst-Case Scenario (Sideways Market)**
- Directional trades incur losses up to $4,000.
- Iron Condor limits further risk and provides hedge.

### Prompt

![Alt text](https://github.com/dearvn/stock-prediction/raw/main/tos.png?raw=true "Price TOS")

```bash
Evaluate options flow for next day trading.  
Predict marketing Total Range movement highest and low and Is this movement consider strong, mid, or weak?
Recommend Best OTM call option strike price from current price should I enter
Recommend Best OTM put option strike price from current price should I enter
```

![Alt text](https://github.com/dearvn/stock-prediction/raw/main/chart-tdv.png?raw=true "Chart TDV")

```bash
Evaluate Future Marketing flow for next day trading.  
Predict marketing Total Range movement highest and low and Is this movement consider strong, mid, or weak?
```

## Conclusion
This strategy combines AI-powered predictions, Martingale scaling, and Iron Condor hedging to optimize SPX options trading. It balances risk and reward while taking advantage of market trends and volatility conditions.

