# Trader Performance vs Market Sentiment  
Primetrade.ai – Round 0 Assignment  

---

## 1. Methodology

This analysis examines how Bitcoin market sentiment (Fear vs Greed) impacts trader behavior and performance on Hyperliquid.

### Data Preparation
- Cleaned and standardized column names.
- Converted `timestamp ist` to datetime format (day-first format).
- Aligned both datasets at a **daily level** using the `date` field.
- Merged trader activity with sentiment classification.
- Checked for missing values and duplicates.

### Feature Engineering
Daily metrics were computed at the **account-date level**:

- **Daily PnL** → Sum of `closed pnl`
- **Trade Count** → Number of trades per day
- **Average Position Size** → Mean of `size usd`
- **Win Rate** → Percentage of profitable trades
- **Long Ratio** → Proportion of long (buy) trades
- **PnL Volatility Proxy** → Standard deviation of daily PnL

Trader segmentation was performed based on:
- Trade frequency (High vs Low)
- Performance consistency (Consistent vs Inconsistent traders)

  ## How to Run

1. Download the notebook (.ipynb file)
2. Install required libraries:
   - pandas
   - numpy
   - matplotlib
   - seaborn
3. Upload datasets
4. Run all cells


---

## 2️. Key Findings

### 🔹 1. Performance Varies Across Sentiment Regimes

- Fear periods show higher PnL volatility.
- Greed periods show increased trade frequency.
- Win rate shifts indicate sentiment-driven behavior changes.

This suggests that trader performance is meaningfully influenced by market psychology.

---

### 🔹 2. Risk-Taking Increases During Greed

During Greed days:
- Traders execute more trades.
- Position sizes tend to increase.
- Long bias becomes stronger.

This reflects risk-on behavior driven by optimism and momentum expectations.

---

### 🔹 3. Inconsistent Traders Are More Vulnerable During Fear

- Traders with historically high PnL variability experience larger drawdowns during Fear periods.
- Consistent traders demonstrate more stable performance across regimes.

This indicates emotional amplification effects during negative sentiment phases.

---

## 3️. Strategy Recommendations

###  Strategy 1 — Defensive Risk Adjustment During Fear

- Reduce trade frequency for high-frequency traders.
- Limit position size expansion.
- Allocate more capital to consistent traders.

**Rationale:** Fear increases volatility and emotional trading risk.

---

###  Strategy 2 — Controlled Aggression During Greed

- Allow moderate exposure increase.
- Cap trade frequency to prevent overtrading.
- Monitor leverage expansion closely.

**Rationale:** Greed encourages overconfidence, which can reduce risk-adjusted performance.

---

###  Strategy 3 — Sentiment-Adaptive Risk Framework

Incorporate sentiment classification as a dynamic signal:

- Lower exposure during Fear regimes.
- Gradually scale during sustained Greed periods.
- Adjust stop-loss sensitivity based on volatility conditions.

---

## 4️. Conclusion

Market sentiment materially influences trader behavior and performance.

Integrating sentiment into risk management and capital allocation decisions can improve risk-adjusted returns and reduce drawdown exposure. Segment-based adaptation (frequency and consistency) provides a structured approach to smarter trading strategy design.

---
## How to Run

1. Download the notebook (.ipynb file)
2. Install required libraries:
   - pandas
   - numpy
   - matplotlib
   - seaborn
3. Upload datasets
4. Run all cells
