# Retail-Demand-Forecaster
An automated Machine Learning forecasting tool built for FMCG Demand Planners
# 🛒 Retail Demand Forecaster (Prophet + Python)

This tool was designed for **Demand Planners** to bridge the gap between static ERP data and actionable 52-week ML forecasts. It specifically solves the "New Product Ramp-Up" and "Missing Promo Tactic" hurdles in retail planning.

### ✨ Key Features:
- **Dynamic Lifecycle Detection:** Automatically adjusts trending logic for New vs. Mature products.
- **Smart Tactic Imputation:** Guesses future promotional visibility based on planned discount depth (e.g., triggers 'Catalogue' flags for >30% discounts).
- **Store-Count Scaling:** Adjusts baseline volume based on supermarket ranging expansion/contraction.
- **Batch Processing:** Forecasts an entire vendor portfolio in one automated run.

### 🛠️ How to Use:
1. Download the `GitHub_Sample_Retail_Data.csv` file from this repo.
2. Open the `.ipynb` notebook in Google Colab.
3. Click "Run All", upload the sample CSV when prompted, and the tool will automatically output a master CSV with 52 weeks of forecasting!

*Note: This is a personal project. All data provided in the sample CSV is randomly generated dummy data for demonstration purposes.*
