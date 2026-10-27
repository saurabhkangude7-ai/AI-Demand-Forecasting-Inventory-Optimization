# AI Demand Forecasting & Inventory Optimization

## Project Overview

This project uses Apache Spark and Machine Learning on Databricks to forecast future product demand and help businesses make better inventory decisions.

Retail businesses often face two major problems:
- **Overstocking:** Keeping too much inventory increases storage costs and waste.
- **Understocking:** Keeping too little inventory can result in lost sales and unhappy customers.

This project analyzes historical sales data, predicts future demand, and generates inventory recommendations to help reduce these problems.

## Project Objectives

- Generate and analyze retail sales data.
- Process data using PySpark.
- Perform feature engineering using historical sales patterns.
- Train a machine learning model to predict product demand.
- Evaluate model performance using MAE and RMSE.
- Calculate safety stock, reorder points, and target inventory.
- Store results in Delta tables.
- Build a Databricks AI/BI dashboard to visualize forecasts and inventory recommendations.

## Technologies Used

- Databricks
- Apache Spark / PySpark
- Spark MLlib
- Random Forest Regression
- Delta Lake
- Python
- Databricks AI/BI Dashboards
- Git and GitHub

## Project Workflow

1. Generate historical retail sales data.
2. Clean and prepare the data using PySpark.
3. Create features such as day of week, month, weekend indicator, previous-day sales, previous-week sales, and rolling average sales.
4. Split the data chronologically into training and testing datasets.
5. Train a Random Forest Regression model.
6. Generate demand predictions.
7. Evaluate predictions using MAE and RMSE.
8. Calculate inventory recommendations.
9. Store sales history, demand predictions, and inventory recommendations in Delta tables.
10. Visualize the results in a Databricks dashboard.

## Inventory Optimization

The project calculates inventory recommendations using forecast demand and inventory planning rules.

- **Forecast Demand:** Expected future product demand.
- **Safety Stock:** Extra inventory held to help protect against demand uncertainty.
- **Reorder Point:** Inventory level at which replenishment should be considered.
- **Target Inventory:** Suggested inventory level to support expected demand.

The exact formulas and assumptions depend on the implementation in the notebook.

## Data Storage

The project uses the following Delta tables:

- `workspace.ai_demand_forecasting.sales_history`
- `workspace.ai_demand_forecasting.demand_predictions`
- `workspace.ai_demand_forecasting.inventory_recommendations`

These tables support analysis and dashboard visualizations.

## Model Evaluation

The model is evaluated using:

- **MAE (Mean Absolute Error):** Measures the average absolute difference between actual