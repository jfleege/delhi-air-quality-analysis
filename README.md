# Delhi Air Quality Analysis

A data analysis (EDA) of air pollution in **New Delhi**, focused specifically on **carbon monoxide (CO)** levels. This project investigates whether **CO emissions differ between weekdays and weekends**, using data from 2021–2025. It includes hypothesis testing, descriptive statistics, and visualizations to ultimately collect information and make a decision on the null hypothesis.

This project was developed in **Python** using:
- `pandas` for data wrangling
- `matplotlib` and `seaborn` for visualization
- `scipy.stats` for hypothesis testing
- Jupyter Notebook for analysis and documentation

---

## About the Dataset

The dataset used for this project is publicly available on Kaggle:

**Delhi Air Quality Dataset**  
https://www.kaggle.com/datasets/kunshbhatia/delhi-air-quality-dataset

---

## Objective of the Project

To determine whether **weekday activities** in New Delhi lead to **higher carbon monoxide (CO)** levels on average than weekends.

---

## Research Question

> Do weekdays (Monday–Friday) produce more CO emissions on average than weekends (Saturday–Sunday) in Delhi?

---

## Hypothesis Testing

- **Null Hypothesis (H₀)**: There is no difference in mean CO emissions between weekdays and weekends.

---

## Methodology

1. **Load and clean the dataset**
2. **Group days into "Weekday" and "Weekend"**
3. **Compute descriptive statistics** (mean, standard deviation, variance)
4. **Visualize data** using KDE plots and bar graphs
5. **Conduct a Welch's t-test** to compare the two groups

---

## Key Findings

| Group     | Mean CO (mg/m³) | Std Dev | Variance |
|-----------|------------------|---------|----------|
| Weekday   | 1.028            | 0.618   | 0.382    |
| Weekend   | 1.019            | 0.584   | 0.341    |

- **p-value** from t-test: **0.793**
- Since **p > 0.05**, we **fail to reject the null hypothesis**.

> Interpretation: There is no statistically significant difference in CO emissions between weekdays and weekends in this dataset.

---

## Graphs and Visuals

- Distribution plots comparing weekday vs weekend CO levels  
- Summary bar charts of CO means and variances  
- Summary tables for statistical findings  

---

## Future Directions

- Further extend analysis to other pollutants: PM2.5, NO₂, etc.
- Add time-series trends (e.g., monthly/seasonal AQI)
- Add contextual research on Delhi air quality policies or events
- Potentially deploy as an interactive Shiny or Dash app

---

## Files in this Repository

| File                        | Description                               |
|----------------------------|-------------------------------------------|
| `new-delhi-air-project.ipynb` | Main Jupyter Notebook with full analysis |
| `final_dataset.csv`         | Cleaned dataset used in the project       |
| `new-delhi-air-project.html` | HTML-exported notebook for easy viewing  |

---
