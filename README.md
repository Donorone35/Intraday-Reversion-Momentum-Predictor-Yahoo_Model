# **HFT-Intraday-Reversion-Momentum-Predictor**

This repository contains a **machine learning model** that implements an **intraday reversion/momentum arbitrage strategy** for **High-Frequency Trading (HFT)**.  
The model identifies ultra-short-term trading opportunities on **1-second to 1-minute intervals** using **statistical indicators** and **machine learning techniques** to detect price reversion and momentum bursts.

## **Key Features**
- **Intraday Arbitrage:** Detects short-lived mispricings for reversion and momentum trades.
- **Signal Generation:** Combines Bollinger Bands, Z-scores, VWAP deviations, RSI, EMA alignment, and volume spikes.
- **Machine Learning Driven:** Utilizes **XGBoost** to classify trade signals.
- **Real-Time Streaming:** Integrates with **Alpaca’s WebSocket API** for live inference.
- **Feature Engineering:** Extracts and processes 1-second and 1-minute OHLCV data into predictive features.

## **Technology Used**
### **Languages & Libraries**
- **Python**
- **NumPy & Pandas** (Data Handling & Processing)
- **Matplotlib, Seaborn & Plotly** (Visualization)
- **Scikit-learn & XGBoost** (Machine Learning)
- **ta** (Technical Analysis Indicators)

### **APIs & Tools**
- **Alpaca API** – For live and historical market data
- **Jupyter Notebook / VS Code** – For experimentation and model development
- **Backtrader / Custom Backtesting** – For simulation and evaluation

## **Installation & Usage**
### **Installation**
1. **Clone the Repository**
   ```bash
   git clone https://github.com/yourusername/hft-intraday-reversion-momentum-predictor.git
   cd hft-intraday-reversion-momentum-predictor

