# 🚀 Universal Retail Demand Forecasting Engine  
### AI-Powered SKU-Level Forecasting for FMCG Retail Systems

A production-style forecasting engine designed for large-scale retail and FMCG demand prediction, combining time-series modeling, price elasticity estimation, and rule-based retail intelligence.

This project demonstrates how forecasting systems can be enhanced beyond standard statistical models by integrating economic behavior, data quality correction, and product lifecycle awareness.

---

# 📌 Key Capabilities

## 🧠 Product Lifecycle-Aware Forecasting

Automatically adapts forecasting logic based on data maturity.

- New products (limited history)
  - Uses stable baseline forecasting
  - Avoids overfitting and unstable seasonality

- Mature products (sufficient history)
  - Activates full seasonal + elasticity modeling
  - Learns stable demand patterns from historical behaviour

---

## 📊 Hybrid Forecasting Architecture

A multi-layer forecasting system combining:

- Facebook Prophet time-series model
- Custom retail seasonality engine
- Price elasticity adjustment layer
- Business-driven regressors (promotions, distribution coverage)

---

## 💰 Dynamic Price Elasticity Modeling

Implements SKU-level demand sensitivity estimation using log-log regression.

- Computes elasticity dynamically per product
- Validation safeguards:
  - Filters invalid positive elasticity
  - Caps extreme values
- Falls back to FMCG benchmark elasticity when data is unstable

---

## 📅 Custom Seasonality Engine

Learns weekly demand structure independent of Prophet.

- Builds demand index by week (1–53)
- Normalises demand to remove price distortion effects
- Applies smoothing controls:
  - 3-week moving average
  - 5-week moving average
  - Weighted seasonality blending

---

## 🧹 Data Quality & Cleaning Framework

Robust preprocessing layer for real-world retail datasets.

- Handles missing and zero values across:
  - Price
  - Store distribution
  - Promotional coverage

- Applies forward/backward filling for pricing continuity
- Stabilises store count using recent averages

---

## 🚨 Retail Anomaly Detection System

Custom outlier handling logic for demand spikes.

- Detects abnormal demand:
  - Greater than 2.5× median demand
  - Not promotion-driven

- Corrects anomalies using stable baseline values

---

## 🔌 Multi-Regressor Forecasting Model

Supports real-world demand drivers:

- Discount intensity
- Store distribution coverage
- Promotional store activity
- Custom seasonal index

All regressors are validated before model training.

---

## ⚖️ Economic Price Adjustment Layer

Post-forecast correction to ensure realism.

- Compares historical vs future pricing
- Applies elasticity-based demand adjustments
- Ensures forecasts reflect real-world price sensitivity

---

## 🔁 Scalable Batch Forecasting System

Designed for large SKU portfolios.

- Processes multiple products in a single run
- Builds independent models per SKU
- Outputs consolidated forecast dataset

---

## 📈 Business-Focused Visualization Layer

Each SKU includes:

- Historical demand vs forecast trend
- Price overlay (dual-axis visualization)
- Clear separation of training vs forecast periods

---

# 🏗️ System Architecture

```text
Raw Retail Data  
    ↓  
Data Cleaning & Imputation Layer  
    ↓  
Anomaly Detection & Correction  
    ↓  
Elasticity Estimation Engine  
    ↓  
Seasonality Learning Module  
    ↓  
Time-Series Forecasting Model (Prophet)  
    ↓  
Economic Adjustment Layer  
    ↓  
Final Forecast Output
```

---

# 📦 Tech Stack

- Python  
- Pandas  
- NumPy  
- Facebook Prophet  
- Matplotlib  
- Google Colab / Jupyter  
- IPyWidgets  

---

# ⚙️ Configuration Options

## Seasonality Smoothing Method

- None  
- 3-week moving average  
- 5-week moving average  

---

## Seasonality Weight (0–1)

Controls the influence of seasonal patterns in the final forecast.

---

## Default Elasticity

Used for products with limited or unstable historical data.

---

## Elasticity Cap

Prevents extreme or unrealistic demand sensitivity effects.

---

# 🎯 Project Highlights

This system addresses key limitations in traditional forecasting models:

- Price-driven demand distortion  
- Promotion-induced volatility  
- Product lifecycle variation  
- Real-world data quality issues  

### Core approach:

Econometric modeling + Time-series forecasting + Retail domain intelligence

---

# 🚀 Output

The system generates:

- SKU-level demand forecasts  
- Clean structured CSV output  
- Visual analytics (historical trend, forecast, and price overlay)  

---

# 📁 Use Cases

- Retail demand planning  
- Inventory optimisation  
- Promotion forecasting  
- Supply chain planning  
- Pricing strategy analysis  

---

# 🧪 Future Enhancements

- Deep learning forecasting models (LSTM / TFT)  
- Forecast uncertainty intervals  
- Streamlit interactive dashboard  
- External feature integration (weather, holidays, events)  
- API deployment for real-time forecasting  

---

# 👤 Author

Independent project exploring AI-driven forecasting systems for retail and supply chain analytics, with a focus on combining statistical modeling, economic behavior, and operational intelligence.
