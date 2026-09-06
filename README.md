# 🇮🇳 Indian Air Quality Analysis

A statistical and machine-learning analysis of air pollution patterns across Indian urban monitoring locations using public CPCB real-time air-quality data.

## 🎯 Research Questions

This project investigates:

- How do pollutant concentrations vary across Indian urban monitoring locations?
- What statistical relationships exist between fine particulate matter (PM₂.₅) and other pollutants?
- Which pollutants are most strongly associated with PM₂.₅?
- Can pollutant measurements be used to model PM₂.₅ concentration?

## 📊 Dataset

The analysis uses real-time air-quality snapshot data published by the Central Pollution Control Board (CPCB) through the Government of India's Open Government Data (OGD) platform.

The dataset contains measurements from:

- **498 monitoring stations**
- **263 cities**
- **31 states**
- **7 pollutants:** PM₂.₅, PM₁₀, NO₂, SO₂, CO, O₃, and NH₃

The raw station-level observations were cleaned, reshaped, and aggregated for statistical analysis and machine-learning experiments.

## 🔬 Analysis Performed

### Data Preparation
- Data ingestion and inspection
- Missing-value and error profiling
- Timestamp handling
- Station-level reshaping
- Pollutant-wise descriptive statistics
- Distribution and skewness analysis

### Statistical Analysis
- Pearson correlation analysis
- PM₂.₅ / PM₁₀ ratio analysis
- Pollutant relationship analysis
- Regional comparison
- ANOVA testing
- Kruskal-Wallis testing

### Machine Learning

A **Random Forest Regressor** was used to model PM₂.₅ concentration from available pollutant measurements.

**Model evaluation:**

| Metric | Result |
|---|---:|
| RMSE | 26.81 µg/m³ |
| R² | 0.3761 |

The model achieved an R² of approximately 0.38, indicating that the selected features explain a meaningful but limited portion of the variation in PM₂.₅ concentration.

### Feature Importance

PM₁₀ was the most influential feature in the Random Forest model, accounting for approximately **59.36%** of the model's feature-importance score.

Feature importance indicates the contribution of a feature to the model's predictive decisions; it should not be interpreted as a causal relationship.

## 📌 Preliminary Findings

- PM₂.₅ showed its strongest linear correlations with **NO₂ (r = 0.21)** and **CO (r = 0.21)** among the analyzed pollutants.
- O₃ showed a comparatively weak linear correlation with PM₂.₅ (**r = 0.05**).
- Several monitoring locations in the Indo-Gangetic region and National Capital Region showed high average PM₂.₅ concentrations.
- The average PM₂.₅ / PM₁₀ ratio in the analyzed data was approximately **72.6%**.

These findings describe statistical associations in the analyzed dataset and should not be interpreted as proof of specific pollution sources or causal mechanisms.

## 🗂️ Project Structure

```text
indian-air-quality-analysis/
├── README.md
├── requirements.txt
├── cpcb_realtime_aqi_clean.csv
└── notebooks/
    └── 01_data_profiling.ipynb
