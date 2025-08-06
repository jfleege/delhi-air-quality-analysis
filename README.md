# Delhi Air Quality Analysis

A comprehensive data analysis and machine learning investigation of **air pollution in New Delhi**, focused on both **exploratory data analysis (EDA)** and **predictive modeling** of the **Air Quality Index (AQI)**.

This project is split into two parts:

1. **EDA and Hypothesis Testing** — Investigates whether **carbon monoxide (CO)** levels differ between weekdays and weekends using statistical testing and visual analysis.  
2. **AQI Prediction via Multiple Linear Regression** — Builds a model to determine which pollutants most significantly impact Delhi's AQI and predicts AQI levels from observed pollutant data.

---

## Tools & Technologies

This project was developed in **Python** using:

- `pandas` for data wrangling  
- `matplotlib` & `seaborn` for visualization  
- `scipy.stats` for hypothesis testing  
- `sklearn` & `statsmodels` for regression modeling  
- Jupyter Notebook for interactive analysis  

---

## Dataset

The dataset was sourced from Kaggle:

**Delhi Air Quality Dataset**  
https://www.kaggle.com/datasets/kunshbhatia/delhi-air-quality-dataset

- Time span: **2021 to 2025**  
- Variables include: `PM2.5`, `PM10`, `CO`, `NO₂`, `SO₂`, `O₃`, `AQI`, date/time stamps, and more.

---

## Part 1: Hypothesis Testing (CO Levels)

### Research Question

> Do weekdays (Monday–Friday) produce more CO emissions on average than weekends (Saturday–Sunday) in Delhi?

### Methodology/Process

- Cleaned and grouped data into "Weekday" and "Weekend"  
- Calculated descriptive statistics  
- Visualized CO distributions and summary statistics  
- Performed a **Welch’s t-test** to compare means  

### Findings

| Group     | Mean CO (mg/m³) | Std Dev | Variance |
|-----------|------------------|---------|----------|
| Weekday   | 1.028            | 0.618   | 0.382    |
| Weekend   | 1.019            | 0.584   | 0.341    |

- **p-value**: 0.793 → **Not significant**  
> **Interpretation**: There is no statistically significant difference in CO levels between weekdays and weekends.

---

## Part 2: AQI Prediction with Linear Regression

### Research Question

> Among the measured pollutants (PM2.5, PM10, NO₂, SO₂, CO), which ones most strongly predict Delhi’s AQI?

### Methodology/Process

- Performed correlation analysis to select strongest features  
- Built and evaluated a **Multiple Linear Regression** model:
  - Selected `PM2.5`, `PM10`, and `CO` as predictors  
- Used both `scikit-learn` and `statsmodels` for model fitting and statistical interpretation  
- Evaluated model with R², residuals, and prediction plots  

### Key Results

- **R² = 0.855**: Model explains 85.5% of AQI variation  
- All predictors were statistically significant (p < 0.001)  
- **PM10** had the highest impact, followed by **PM2.5** and **CO**  
- Residuals suggest additional variables (NO₂, O₃, time features) could further improve accuracy  

---

## Main Takeaways

- AQI in Delhi is **rarely “Good”** by EPA standards — fewer than 50 clean-air days in 5 years  
- **PM10, PM2.5, and CO** are the dominant drivers of AQI  
- The model performs well in predicting AQI and can be extended for future use cases  

---

## Part 3: ML Extension: Modeling Delhi’s AQI with Regression

In this part of the project, we build a **multiple linear regression model** to predict Delhi’s AQI using pollutant measures. Key highlights:

- Explored strongest predictors: **PM2.5, PM10, CO**, then extended model with **NO₂**
- Best model (with NO₂) explains **85.7%** of AQI variance
- All predictors maintain high statistical significance and improve interpretability
- Model refinement and performance comparison are detailed in the notebook `delhi-aqi-ml-model.ipynb`
