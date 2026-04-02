# Custom Readiness Score Algorithm

![Status](https://img.shields.io/badge/Status-In%20Progress-yellow)
![Python](https://img.shields.io/badge/Python-3.14-blue)
![License](https://img.shields.io/badge/License-MIT-green)

> Personalized recovery algorithm developed through analysis of 164 days of Oura Ring biometric data

---

## Project Overview

This project aims to develop a **personalized recovery scoring algorithm** by analyzing my own wearable data from an Oura Ring over 164 days (September 2025 - February 2026). 

Rather than relying solely on Oura's proprietary algorithm, I'm building a custom model that identifies **my specific recovery patterns** and optimizes prediction based on my physiological profile.

**Key Question:** *Can a personalized algorithm outperform a one-size-fits-all approach?*

---

## Objectives

- ✅ Build end-to-end data science pipeline for wearable data
- ✅ Identify key physiological factors driving my recovery
- ✅ Analyze lifestyle patterns (weekday vs weekend, sleep deficit)
- ⏳ Develop machine learning model for personalized prediction
- ⏳ Compare custom algorithm performance vs Oura's scoring

---

## Dataset

**Source:** Oura Ring Gen 4  
**Period:** September 4, 2025 → February 25, 2026  
**Duration:** 164 days (after cleaning)  

**Metrics tracked:**
- **Cardiac:** HRV (Heart Rate Variability), Resting Heart Rate, HRV/RHR Ratio
- **Sleep:** Total duration, Deep/REM/Light percentages, Sleep efficiency
- **Recovery:** Readiness Score, Sleep Score
- **Health:** Body temperature deviation
- **Temporal:** Day of week, weekend indicators

---

## 🔬 Methodology

### Phase 1: Data Cleaning ✅
- Loaded raw CSV export from Oura Cloud (166 days)
- Removed incomplete records (2 days with missing data)
- Feature engineering: created derived metrics (sleep hours, stage percentages, HRV/RHR ratio)
- Temporal features: day of week, weekend classification

### Phase 2: Exploratory Data Analysis ✅
- Statistical profiling of all metrics
- Identified best/worst recovery days
- Analyzed patterns by day of week
- Weekend vs weekday comparison

### Phase 3: Correlation Analysis ✅
- Computed correlations with Readiness Score
- Identified top recovery factors
- Created correlation heatmap (9 key metrics)
- Detected multicollinearity between variables

### Phase 4: Machine Learning ⏳
- Feature selection based on correlation analysis
- Train regression model (Linear Regression, Random Forest)
- Custom algorithm development
- Performance comparison with Oura scoring

---

## Key Findings

### 1 : Resting Heart Rate is the Primary Factor

**Correlation with Readiness: r = -0.70**

Contrary to conventional wisdom that prioritizes HRV, my data shows **Resting Heart Rate** is the strongest predictor of recovery state.

- RHR correlation: **-0.70** (strong negative)
- HRV correlation: **+0.52** (moderate positive)
- **Implication:** For me, elevated RHR is a more reliable fatigue/stress indicator than HRV alone

### 2 : Weekend Recovery Advantage

**+6.3% Readiness improvement on weekends**

- Weekend Readiness: **77.8/100** (avg)
- Weekday Readiness: **73.2/100** (avg)
- **Difference:** +4.6 points (+6.3%)

**Driven by sleep volume:**
- Weekend sleep: **8.2 hours** (avg)
- Weekday sleep: **6.8 hours** (avg)
- **Difference:** +1.4 hours (+20.6%)

**Sleep is the limiting factor during weekdays.**

### 3 : HRV and Sleep Operate Independently

**Correlation between HRV and sleep volume: r = -0.06**

- These metrics capture **different aspects** of recovery
- High HRV ≠ Good sleep (and vice versa)
- **Implication:** Multi-factor model required; single-metric approach insufficient

### 4 : Lifestyle Impact on Recovery Quality

**Thursday pattern identified:**
- Highest sleep volume (8.0h avg)
- **Lowest HRV** (56.1 ms) and **highest RHR** (58.9 bpm) of the week
- **Cause:** Wednesday evening social activities degrading sleep quality despite adequate volume

**Sleep duration ≠ Sleep quality**

### 5 : Multicollinearity Detected

- HRV and HRV/RHR ratio: **r = 0.96** (near-perfect correlation)
- **Implication:** Using both creates redundancy; select one for model optimization

---

## Visualizations

### Correlation Heatmap
*[Image placeholder - heatmap will be added]*

Key relationships between 9 primary recovery metrics, highlighting RHR's central role and HRV-sleep independence.

### Weekly Pattern Analysis
*[Image placeholder - bar chart will be added]*

Average Readiness Score by day of week, showing consistent weekend advantage and mid-week dip.

---

## 🛠️ Tech Stack

**Languages & Libraries:**
- Python 3.14
- Pandas, NumPy (data manipulation)
- Matplotlib, Seaborn (visualization)
- Scikit-learn (machine learning - in progress)

**Environment:**
- Jupyter Notebooks
- VS Code
- Git version control

---

## 📂 Project Structure
```
custom-readiness-score/
├── data/
│   ├── oura_data.csv          # Raw data from Oura
│   └── oura_clean.csv         # Cleaned dataset
├── notebooks/
│   ├── 01_data_cleaning.ipynb       ✅ Complete
│   ├── 02_exploratory_analysis.ipynb ✅ Complete
│   ├── 03_correlations.ipynb        ✅ Complete
│   ├── 04_visualizations.ipynb      ⏳ In progress
│   └── 05_modeling.ipynb            ⏳ Planned
├── src/                       # Reusable Python modules (planned)
├── results/                   # Generated visualizations (planned)
├── README.md
└── requirements.txt
```

---

## Current Status

**Completed:**
- ✅ Data cleaning pipeline (164 days processed)
- ✅ Exploratory data analysis
- ✅ Correlation analysis
- ✅ Key insights identification

**In Progress:**
- 🔄 Advanced visualizations for presentation
- 🔄 Machine learning model development

**Planned:**
- ⏳ Custom algorithm implementation
- ⏳ Performance benchmarking vs Oura
- ⏳ Modular code refactoring (src/)
- ⏳ Interactive dashboard (optional)

---

## Learnings & Skills Demonstrated

- **Data Pipeline:** End-to-end workflow from raw export to insights
- **Statistical Analysis:** Correlation studies, pattern identification
- **Domain Knowledge:** Wearable data, physiological metrics interpretation
- **Critical Thinking:** Challenging conventional wisdom (HRV primacy)
- **Scientific Method:** Hypothesis testing, empirical validation
- **Communication:** Translating technical findings into actionable insights

---

## Contact

**Timeo Heinemann** - Engineering Student at EPF  
Seeking 4-month data internship (August/September 2026)  

📫 [timeoheinemannpro@icloud.com]  
💼 [https://www.linkedin.com/in/timeo-heinemann-6229b7307/]  

---

## License

This project is for educational and portfolio purposes.  
Data: Personal health data from Oura Ring (not shared publicly for privacy).

---

*Last updated: April 2026*