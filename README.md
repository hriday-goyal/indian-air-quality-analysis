# 🇮🇳 Indian Air Quality Analysis

A data-driven analysis of air pollution patterns across Indian urban locations using public real-time air-quality data from the Central Pollution Control Board (CPCB).

## 🎯 Research Question

How do air-pollution patterns vary across Indian urban locations, and which pollutants show the strongest statistical relationships with fine particulate pollution (PM2.5)?

## 📊 Dataset

The project uses real-time air-quality snapshot data published by the Central Pollution Control Board (CPCB) through the Government of India's Open Government Data (OGD) platform.

The dataset contains measurements for:

- PM2.5
- PM10
- NO2
- SO2
- CO
- OZONE
- NH3

The raw dataset covers 498 monitoring stations across 31 states and 263 cities.

The data was reshaped into a station-level format and cleaned before analysis.

## 🔬 Analysis Performed

### 1. Data Profiling & Cleaning
- Inspected dataset structure and data types
- Reshaped pollutant measurements into a station-level table
- Handled missing values
- Processed timestamp information
- Generated summary statistics and distribution checks

### 2. Pollutant Analysis
- Calculated pollutant summary statistics
- Examined Pearson correlations between pollutants
- Analyzed the PM2.5/PM10 ratio
- Identified cities and stations with higher average PM2.5 concentrations

### 3. Regional Statistical Analysis
- Compared PM2.5 concentrations across the selected regions represented in the dataset
- Performed One-Way ANOVA
- Performed the Kruskal-Wallis test

Both statistical tests indicated statistically significant differences in PM2.5 concentrations across the tested regions.

### 4. Machine Learning

A Random Forest Regressor was developed to predict PM2.5 using:

- CO
- NH3
- NO2
- OZONE
- PM10
- SO2

Model configuration:

- 100 decision trees
- 80/20 train-test split
- Random state: 42

Model performance on the test set:

- **RMSE:** 26.81 µg/m³
- **R²:** 0.3761

Feature importance from the model:

| Feature | Importance |
|---|---:|
| PM10 | 59.36% |
| CO | 11.08% |
| SO2 | 9.00% |
| NO2 | 7.95% |
| OZONE | 7.84% |
| NH3 | 4.77% |

Feature importance indicates how much the model relied on each feature for prediction; it does not imply a causal relationship between pollutants.

## 📈 Key Findings

- PM2.5 showed its strongest observed linear correlations with NO2 and CO, both with correlation coefficients of approximately **0.21**.
- OZONE showed a weak observed linear correlation with PM2.5 (**r ≈ 0.05**).
- The average observed PM2.5/PM10 ratio in the analyzed data was approximately **72.6%**.
- Several stations and cities in northern India recorded relatively high average PM2.5 concentrations.
- Statistical testing found significant differences in PM2.5 concentrations across the selected regions.
- In the Random Forest model, PM10 was the most important predictor of PM2.5.

## 🛠️ Technologies Used

- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **SciPy**
- **Scikit-Learn**
- **Google Colab / Jupyter Notebook**
- **Git & GitHub**

## 📁 Project Structure

```text
indian-air-quality-analysis/
├── data/
│   └── cpcb_realtime_aqi_clean.csv
├── notebooks/
│   └── 01_air_quality_analysis.ipynb
├── README.md
└── requirements.txt
