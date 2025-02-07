# History

### 07/02/25
> **Primary Bias: Bullish (favoring Calls)**
> Best Call Strike: 6,100
> Best Put Strike (Hedge): 6,050
> **Trading Plan:**
> If SPX stays above 6,080, focus on calls at 6,100.
> If SPX breaks below 6,060, hedge with puts at 6,050.

### 06/02/25
> **Final Prediction: Bullish Trend**
> The market is showing strength, and call options have a better probability of success.
> If SPX remains above 6,060, expect further upside to 6,075-6,100.
> A break below 6,050 could signal a reversal, making puts a better play.

### 04/01/25
> **Market Analysis & Recommendations**  
>  
> **Expected Market Range for Next Trading Day:**  
> - Highest Expected Price: ~6,045  
> - Lowest Expected Price: ~5,950  
> - Total Range Movement: 50.43 (high) / 44.57 (low)  
>  
> **Market Strength:**  
> - Movement Percentage: 0.84% (high) / 0.74% (low)  
> - Conclusion: Market movement is expected to be weak.  
>  
> **Best Option Strike Prices:**  
> - Recommended OTM Call Option Strike: 6,020  
> - Recommended OTM Put Option Strike: 5,970  




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

## How to predict?
- **Input**
> 1.  Current SPX Price
> 2.  Current Date Trade
> 3.  Options Data (Volume, Open Int, Delta, ProbITM, Bid, Ask and Strike Price)  Bot call and PUT giong nhu cai hinh capture
- **Promt**
> Evaluate options flow for next day trading.  
> Predict marketing Total Range movement highest and low
> Is this movement consider strong, mid, or weak? 
> What is marketing trending?
> Recommend Best OTM call option strike price from current price should I enter
> Recommend Best OTM put option strike price from current price should I enter
> what is predicted trend call or put
> Give me specific trade setup based on risk-reward?

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

