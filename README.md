# **Intraday-Reversion-Momentum-Predictor **

This repository contains a **machine learning model** that implements an **intraday reversion/momentum arbitrage strategy**.  
The model identifies ultra-short-term trading opportunities on **1-minute intervals** using **statistical indicators** and **machine learning techniques** to detect price reversion and momentum bursts.

## **Key Features**
- **Intraday Arbitrage:** Detects short-lived mispricings for reversion and momentum trades.
- **Signal Generation:** Combines Bollinger Bands, Z-scores, VWAP deviations, RSI, EMA alignment, and volume spikes.
- **Machine Learning Driven:** Utilizes **XGBoost** to classify trade signals.
- **Real-Time Streaming:** Integrates with **Yahoo Finance** for live inference.
- **Feature Engineering:** Extracts and processes 1-second and 1-minute OHLCV data into predictive features.
- **Dual Model Setup:** Uses **1-minute model for intraday signals** and **1-hour model for trend confirmation**.

## **Technology Used**
### **Languages & Libraries**
- **Python**
- **NumPy & Pandas** (Data Handling & Processing)
- **Matplotlib, Seaborn & Plotly** (Visualization)
- **Scikit-learn & XGBoost** (Machine Learning)
- **ta** (Technical Analysis Indicators)

### **APIs & Tools**
- **Yahoo Finance** – For live and historical market data
- **Jupyter Notebook / VS Code** – For experimentation and model development
- **Backtrader / Custom Backtesting** – For simulation and evaluation

### **Data & Models**
- **Model #1 (1-minute):**  
  Download historical Yahoo Finance 1-minute data for AAPL (up to ~30 days) → Used for training the intraday model.
- **Model #2 (1-hour):**  
  Download historical Yahoo Finance 1-hour data for AAPL (up to ~2 years) → Used for validation and trend confirmation.
- **Strategy:**  
  Same trading strategy applies to both models, with indicator parameters tuned to the respective timeframe.

### **Live Loop**
- Updates with the latest 1-minute candle from Yahoo Finance.
- Runs **Model #1** to generate **Buy/Sell/Hold** signals.
- Optionally compares with **Model #2’s** hourly signal for trend confirmation.

## **Installation & Usage**
### **Installation**
1. **Clone the Repository**
   ```bash
   git clone https://github.com/yourusername/hft-intraday-reversion-momentum-predictor.git
   cd hft-intraday-reversion-momentum-predictor
