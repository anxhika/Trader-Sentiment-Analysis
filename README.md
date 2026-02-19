# Trader-Sentiment-Analysis
## 📌 Objective

Analyze how Bitcoin market sentiment (Fear & Greed Index) relates to trader behavior and performance on Hyperliquid. The goal is to identify behavioral patterns and propose actionable trading strategies.

---

## 📊 Datasets

1. **Bitcoin Market Sentiment Dataset**
   - Columns: timestamp, value, classification, date
   - Daily sentiment regime (Fear, Greed, Extreme Fear, Extreme Greed, Neutral)

2. **Historical Trader Data (Hyperliquid)**
   - Account-level trade records
   - Includes timestamp, closed PnL, position size, and trade activity

Both datasets were aligned at daily granularity.

---

## 🛠 Methodology

### 1. Data Cleaning & Preparation
- Removed duplicates and checked missing values
- Converted timestamps to datetime format
- Extracted daily date
- Merged trader data with sentiment data

### 2. Feature Engineering
- Daily PnL per trader
- Win rate (percentage of profitable trades)
- Trade frequency per account
- Average position size
- Next-day profitability label (for predictive modeling)

### 3. Exploratory Analysis
- Compared average PnL across sentiment regimes
- Analyzed win rate differences
- Evaluated behavioral shifts in trade frequency and size

### 4. Trader Segmentation
- Frequent vs Infrequent trader segmentation
- KMeans clustering to identify behavioral archetypes

### 5. Predictive Modeling (Bonus)
- Random Forest classifier
- Target: Next-day profitability bucket
- Accuracy: ~66%

---

## 🔎 Key Insights

- Extreme Greed shows highest average PnL.
- Extreme Fear increases volatility and reduces win rate.
- Infrequent traders outperform during strong Greed regimes.
- Trader behavior changes significantly across sentiment states.

---

## 🎯 Strategy Recommendations

### 1. Sentiment-Based Risk Adjustment
- Reduce leverage and position size during Extreme Fear.
- Apply strict stop-loss during Greed regimes.

### 2. Segment-Specific Optimization
- Frequent traders should reduce activity during Fear.
- Increase participation during Greed trends.
- Infrequent traders should focus on high-conviction trades.

---

## 📈 Output Charts & Tables

The notebook includes:

- Boxplot: PnL distribution across sentiment regimes
- Average PnL by sentiment table
- Win rate comparison by sentiment
- Trade frequency segmentation analysis
- KMeans cluster summary table
- Confusion matrix & classification report for predictive model

---

## 🚀 Setup Instructions

### 1️⃣ Clone Repository

```bash
git clone https://github.com/YOUR_USERNAME/Trader-Sentiment-Analysis.git
cd Trader-Sentiment-Analysis
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
jupyter notebook
Trader_Analysis.ipynb

