# Business-Analytics---Sales-Forecasting-and-Inventory-Optimization-for-a-Retail-Store-using-TSA
Retail Sales Forecasting &amp; Inventory Optimization using Prophet, ARIMA, and ML models. Includes data cleaning, EDA, association rules, demand forecasting (2025–2027), safety-stock calculation, reorder point estimation, and category-wise insights.
📊 Retail Sales Forecasting & Inventory Optimization
Business Analytics Project

This project performs end-to-end retail sales forecasting and inventory optimization using a large U.S. retail dataset. It includes exploratory data analysis, time-series modeling, forecasting (2025–2027), safety stock estimation, reorder point calculation, and category-wise insights using ML & statistical techniques.

🚀 Project Objectives
Analyze historical U.S. retail sales across multiple business categories
Identify seasonality, trends, and correlations through EDA
Perform feature engineering (lag features, scaling, date-time extraction)
Build forecasting models: Prophet, ARIMA, Random Forest
Evaluate models using MAE, RMSE, MAPE
Generate 2025–2027 sales forecasts per category
Compute Safety Stock and Reorder Point
Extract Association Rules
Provide inventory optimization recommendations

📁 Dataset Overview
The dataset includes monthly U.S. retail sales (1992–2024) across categories:
Automotive & Fuel
Food & Beverages
Clothing & Footwear
Electronics
Home & Furniture
Health & Wellness
General Merchandise
Sports & Leisure
Books & Entertainment
Jewelry
Other

Key columns include:
business_category, sales, estimate_type, month_year, year, month, quarter, safety_stock, sales_scaled, etc.

🧹 Preprocessing & Feature Engineering
Handled missing values and converted dates to time-indexed format
Extracted year, month, quarter
Created lag-1 sales feature
Generated scaled sales feature
Aggregated monthly series per category

📈 Exploratory Data Analysis
Visualizations include:
Sales distribution histogram
Monthly trends and seasonal patterns
Lag-1 scatter plot
Correlation bar chart
SHAP feature-importance visualization
Category-wise historical vs forecast plots

Insights:
Strong month-to-month correlation in sales
Increasing long-term retail demand over years
Seasonal peaks in Nov–Dec for most categories
Past sales are the most influential predictor

🔮 Forecasting Models
Implemented and compared:
✔ Facebook Prophet
Best performance across categories
Captures seasonality & holiday-driven spikes
Lowest MAE, RMSE, MAPE
✔ ARIMA
Strong baseline model
Performs well for stable series
Weaker on multi-seasonal patterns
✔ Random Forest Regressor
Works with lagged & engineered features
Lower performance than time-series models
Useful for comparison

📊 Model Evaluation
Metrics computed for 2023–2024 (test period):
MAE — Mean Absolute Error
RMSE — Root Mean Squared Error
MAPE — Mean Absolute Percentage Error

Outcome:
👉 Prophet consistently outperformed ARIMA and Random Forest in accuracy.
📦 Inventory Optimization
For each category (2025–2027):
Forecast monthly sales (yhat)
Compute uncertainty range (yhat_lower & yhat_upper)
Calculate:
Demand During Lead Time
Safety Stock (using σ & service level)
Reorder Point
Delivered as a multi-sheet Excel file with:
Category-wise forecasts
TOTAL company-wide forecast
Combined dataset
Summary statistics

🔍 Association Rule Mining
Implemented Apriori rules to find patterns between:
Business categories
Months & quarters
Estimate types

Example:
“If month = December → Sales spike in Clothing & Footwear & Electronics.”
🛒 Inventory Recommendations
Increase stock of Clothing, Electronics, and General Merchandise during Q4
Maintain higher safety stock in Food & Beverages year-round
Reduce inventory for declining low-selling categories
Use upper forecast bounds (yhat_upper) for high-demand months

🧪 Tech Stack
Python
Pandas, NumPy
Matplotlib, Seaborn
Prophet
Statsmodels (ARIMA / Exponential Smoothing)
Scikit-learn
SHAP

MLxtend (Association Rules)

📄 Results Delivered
Forecasts for 2025–2027 per category
Safety Stock & Reorder Points
11 category-level visualizations
Evaluation tables

SHAP interpretability plots

Clean final Excel output

Optimized recommendations for decision-making
