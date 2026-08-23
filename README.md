# 🇮🇳 Indian Air Quality Analysis

A statistical and data-driven analysis of air pollution patterns across Indian urban locations using public CPCB real-time air-quality data.

## 🎯 Research Question

How do air-pollution patterns vary across Indian urban locations, and which gaseous pollutants show the strongest statistical relationships with fine particulate pollution ($\text{PM}_{2.5}$)?

## 🔬 Key Preliminary Findings

- **High Fine Particulate Proportion:** Fine particulate matter ($\text{PM}_{2.5}$) accounts for an average of **72.6%** of overall coarse particulate matter ($\text{PM}_{10}$) nationwide. This indicates that urban pollution in India is heavily dominated by combustion sources (vehicular emissions, industrial activity, biomass burning) rather than coarse soil dust alone.
- **Pollutant Correlations:** $\text{PM}_{2.5}$ exhibits its strongest linear correlation with nitrogen dioxide ($\text{NO}_2$, $r = 0.21$) and carbon monoxide ($\text{CO}$, $r = 0.21$). Ground-level ozone ($\text{O}_3$) shows near-zero linear correlation ($r = 0.05$).
- **Geographic Hotspots:** Stations across the Indo-Gangetic Belt and National Capital Region (e.g., Faridabad, Bhagalpur, Manesar, Panipat) record the highest average concentrations of fine particulate matter.

## 📊 Data Source

This project utilizes real-time air quality snapshot data published by the Central Pollution Control Board (CPCB) via the Government of India's Open Government Data (OGD) platform, covering 498 active monitoring stations nationwide across 7 primary pollutants ($\text{PM}_{2.5}$, $\text{PM}_{10}$, $\text{NO}_2$, $\text{SO}_2$, $\text{CO}$, $\text{O}_3$, and $\text{NH}_3$).

## 🛠️ Technologies Used

- **Data Wrangling:** Python, Pandas, NumPy
- **Data Visualization:** Matplotlib, Seaborn
- **Development Environment:** Google Colab / Jupyter Notebook
- **Version Control:** Git, GitHub

## 🚧 Project Status

**Active Analysis & Modeling Phase**

- [x] Data ingestion, pivoting, and station-level schema reshaping
- [x] Summary statistics, skewness check, and error profiling
- [x] Pearson correlation matrix & $\text{PM}_{2.5}/\text{PM}_{10}$ ratio analysis
- [ ] Regional hypothesis testing (ANOVA / Kruskal-Wallis)
- [ ] Predictive regression modeling using Scikit-Learn

## 👤 Author

**Hriday Goyal**
