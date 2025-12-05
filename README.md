# FX Next-Day Direction Classifier (GBP/USD)

A machine learning project that predicts the next-day direction (UP/DOWN) of the GBP/USD exchange rate using logistic regression and random forest models.  
The project includes data preparation, feature engineering, time-series splitting, probability outputs, ROC/AUC evaluation, backtesting, and Sharpe ratio analysis.

---

## 📌 Project Goals
- Investigate predictability of FX daily returns  
- Build ML models for directional forecasting  
- Apply feature engineering on financial time series  
- Evaluate models using real trading metrics  
- Understand challenges of FX prediction  

---

## 📁 Project Structure
ML-Classifier/
│
├── notebooks/
│ └── baseline_classifier.ipynb
├── .gitignore
└── README.md


---

## 🔧 Feature Engineering
- Daily log returns  
- Rolling volatility (5-day)  
- Momentum (3-day and 7-day percentage change)  
- Moving averages (5-day and 20-day)  
- Moving average ratio  

---

## 🤖 Models Used
- Logistic Regression  
- Random Forest Classifier  

Both models output class predictions and probabilities (via `predict_proba`).

---

## 📊 Evaluation Metrics
- **Accuracy**
- **Confusion Matrix**
- **ROC-AUC**
- **Probability Curves**
- **Backtested Strategy Returns**
- **Sharpe Ratio**

---

## 📈 Results Summary

- Logistic Regression AUC ≈ **0.517**
- Random Forest AUC ≈ **0.533**
- Sharpe Ratio (LR) ≈ **–1.07**
- Sharpe Ratio (RF) ≈ **–0.53**

These results reflect the difficulty of predicting FX daily direction due to strong market efficiency at this time horizon.

---

## 📉 Backtesting Overview
A simple long/short strategy was tested:

- Go **long** if model predicts UP  
- Go **short** if model predicts DOWN  
- Daily returns multiplied by prediction  

Both models produced negative cumulative returns, confirming that directional daily prediction is weak for FX.

---

## 🚀 Future Improvements
- Use **hourly** data instead of daily  
- Add technical indicators (RSI, MACD, Bollinger Bands)  
- Add lagged returns and volatility clustering features  
- Try advanced ML models (XGBoost, LightGBM)  
- Implement a more robust trading backtester with spreads/slippage  
- Perform walk-forward cross-validation  

---

## 🛠️ Technologies
- Python  
- Pandas, NumPy  
- Scikit-Learn  
- Matplotlib, Seaborn  
- Jupyter Notebook  

---

## ✍️ Author
**Javidan Islamzade**  
Finance Major, ADA University  
Interested in quantitative finance, ML, and algorithmic trading.
