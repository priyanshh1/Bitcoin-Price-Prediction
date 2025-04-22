# Bitcoin Price Prediction using Machine Learning

This project uses machine learning models to predict Bitcoin price trends based on historical OHLC data. The goal is to classify whether buying Bitcoin on a given day will result in a profit the next day.

## 📌 Dataset
- **Source**: Bitcoin OHLC data (17 July 2014 – 29 Dec 2022)
- Features: Open, High, Low, Close, Volume, Date

## ⚙️ Technologies
- Python, Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn, XGBoost

## 🔍 Feature Engineering
- Derived features: `open-close`, `low-high`, `is_quarter_end`, `year`, `month`, `day`
- Target variable: Binary label based on next-day price change

## 📊 Modeling
Trained and evaluated:
- Logistic Regression
- SVM (Polynomial Kernel)
- XGBoost Classifier

**Metric**: ROC-AUC Score

| Model               | Train AUC | Validation AUC |
|--------------------|-----------|----------------|
| Logistic Regression| 0.527     | 0.519          |
| SVM (Poly)         | 0.483     | 0.528          |
| XGBoost            | 0.923     | 0.462          |

## 📈 Conclusion
Models performed close to random guessing. XGBoost overfitted. Additional features or external signals may improve performance.
