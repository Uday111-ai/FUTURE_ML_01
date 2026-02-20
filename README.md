# 📊 Sales & Demand Forecasting using Machine Learning

## 🚀 Project Overview

This project builds a **Sales Forecasting System** using historical Superstore sales data.  
The objective is to predict future monthly sales and generate actionable business insights for inventory and financial planning.

The model captures:
- Seasonality
- Trend patterns
- Short-term momentum
- Long-term sales behavior

---

## 🎯 Business Objective

The forecasting system helps businesses:

- Plan inventory in advance
- Prepare for seasonal demand spikes
- Optimize staffing
- Reduce overstocking and stockouts
- Improve cash flow management

---

## 📂 Dataset

**Superstore Sales Dataset**

Contains:
- Order Date
- Sales
- Category
- Region
- Quantity
- Discount
- Profit

Date Range: 2014–2017  
Country column dropped (constant value)

---

## 🧹 Data Preparation

1. Converted `Order Date` to datetime format.
2. Removed unnecessary columns.
3. Aggregated daily sales into **monthly sales** to reduce noise.
4. Sorted dataset chronologically.

---

## ⚙ Feature Engineering

### Time-Based Features
- Year
- Month
- Quarter

### Lag Features
- Lag 1 month
- Lag 2 months
- Lag 3 months
- Lag 6 months
- Lag 12 months

### Rolling Features
- 3-month rolling average
- 6-month rolling average

These features allow the model to understand:
- Recent trends
- Seasonal cycles
- Sales momentum

---

## 🧠 Model Used

**Random Forest Regressor**

Why Random Forest?
- Handles non-linear relationships
- Works well with lag-based features
- Robust to outliers
- Good performance on structured data

Time-based train-test split used:
- Training: 2014–2016
- Testing: 2017

---

## 📈 Model Performance

| Metric | Value |
|--------|--------|
| R² Score | ~0.64 |
| MAE | ~13,000–16,000 |
| RMSE | ~15,000–20,000 |

### Interpretation

- Model explains **64% of sales variation**
- Forecast error is within acceptable retail forecasting range (15–25%)
- Model captures seasonal spikes effectively

---

## 🔮 6-Month Future Forecast

Recursive forecasting was implemented to predict the next 6 months.

The forecast suggests:

- Q4 months show peak sales
- Q1 months show seasonal dip
- Sales trend gradually increases before festive season

---

## 📊 Key Insights

1. **October–December generate highest sales**
   - Business should increase inventory before Q4.

2. **January–February show lower demand**
   - Reduce bulk procurement.

3. **Recent 3–6 month trend strongly influences future sales**
   - Monitor rolling averages for early demand signals.

---

## 💡 Business Recommendations

| Period | Strategy |
|--------|----------|
| Q1 | Control inventory, avoid overstock |
| Q2 | Maintain stable procurement |
| Q3 | Prepare for seasonal growth |
| Q4 | Increase stock & staffing |

---

## 🏁 Conclusion

The forecasting model provides reliable monthly sales predictions and supports strategic decision-making.

It transforms historical sales data into:
- Predictive insights
- Risk-aware planning
- Data-driven inventory optimization

---

## 🛠 Tech Stack

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib

---

## 📌 Future Improvements

- Implement XGBoost for performance comparison
- Add SARIMA model for classical time-series comparison
- Deploy as dashboard (Power BI / Streamlit)
- Add confidence interval bands
