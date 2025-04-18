# 🌍 Life Expectancy & Air Health Data Analysis

## 📌 Overview

This project analyzes global **Life Expectancy** data alongside **Health Expenditure (% of GDP)** with the goal of uncovering how factors like **education**, **health spending**, and **disease prevalence** influence public health outcomes.

The main focus is to answer the research question:

> _What is the relationship between average years of schooling and life expectancy, and how does education influence other health outcomes such as infant mortality, under-five mortality, and disease prevalence?_

---

## 📂 Dataset Overview

We used two datasets:

### 1. `Life Expectancy Data.csv` (Kaggle)
- 22 features across 2,938 records
- Covers global statistics from 2000 to 2015
- Key attributes:
  - `Life expectancy`, `Status`, `Schooling`
  - `HIV/AIDS`, `Hepatitis B`, `Infant deaths`
  - `GDP`, `BMI`, `Population`, `Polio`, etc.

### 2. `Health_Expenditure.csv` (World Bank API)
- Country: **Israel**
- 16 records from 2000 to 2015
- Tracks `Health_Expenditure_%_GDP`

---

## 🧠 Key Insights

- 📚 **Education Matters**  
  Higher schooling years are strongly correlated with higher life expectancy (`r = 0.66`), and negatively correlated with infant mortality and disease prevalence.

- 👶 **Infant Mortality Drops With Education**  
  Schooling is negatively correlated with both `Infant Deaths` and `Under-Five Mortality` (around `r = -0.56`), confirming its importance in child health outcomes.

- 🧬 **Disease Prevalence and Education**  
  Diseases like `HIV/AIDS` and `Hepatitis B` decrease with higher education levels due to increased awareness and preventative care.

- 💰 **Health Spending Correlates with Longevity**  
  Countries with higher **health expenditure (% of GDP)** tend to report higher life expectancy — though education appears to enhance the impact of spending.

---

## 🧹 Data Cleaning & Preprocessing

- ✔️ Removed columns with excessive nulls
- ✔️ Renamed columns and standardized formatting
- ✔️ Converted dtypes (e.g., `float16` / `int16`) to optimize memory usage
- ✔️ Handled outliers using Z-score method
- ✔️ Merged external API data using the `Year` column

---

## 📊 Visualizations

- 📈 **Histograms & Scatter Plots** – Showed distributions and correlations between health indicators
- 📉 **Heatmaps** – Displayed relationships between variables like `Schooling`, `Life Expectancy`, and `HIV/AIDS`
- 📊 **Bar Plots** – Compared known vs. unknown value counts in key columns

---

## ⚙️ Tools & Techniques

- **Language:** Python 🐍  
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn  
- **Data Cleaning:** Missing values, data types, column renaming, outlier replacement  
- **Visualization:** Histograms, bar charts, heatmaps, and scatter plots  
- **Statistical Insight:** Descriptive statistics and Pearson correlation analysis
