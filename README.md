# Diamond Price Prediction: Regression Modeling Project

This project explores the relationship between diamond prices and their physical characteristics to build an accurate and interpretable predictive model. Using a dataset of **1,000 observations** , I applied advanced regression techniques, including **log-log transformations** and **stepwise AIC selection** , to explain approximately **98.4% of price variation**.

## Key Findings

* **Primary Predictor**: **Carat** is the most powerful indicator of price [cite: 544][cite_start], initially explaining 85% of variance in a simple model[cite: 609].
* [cite_start]**Quality Factors**: Categorical variables—**Cut, Color, and Clarity**—significantly improve model performance [cite: 975][cite_start], reflecting that diamond quality plays a major role in real-world pricing[cite: 977].
* [cite_start]**Model Accuracy**: The final model achieved an **Adjusted $R^2$ of 0.9838** [cite: 1080][cite_start], with a low Residual Standard Error (RSE) of 0.1289 on the log scale[cite: 1078, 1108].

## 🛠️ Statistical Workflow

### 1. Exploratory Data Analysis (EDA)
* [cite_start]**Skewness Detection**: Identified strong right-skewness in both `price` and `carat`[cite: 1356].
* [cite_start]**Correlation Analysis**: Discovered high correlations among size-related variables like `x`, `y`, and `z`[cite: 1358].

### 2. Model Transformation & Improvement
* [cite_start]**Log-Log Transformation**: Applied a log transformation to both the response (`price`) and the predictor (`carat`) to address violations of **normality** and **homoscedasticity**[cite: 1362, 1363].
* [cite_start]**Linearization**: The transformation stabilized variance [cite: 932][cite_start], reduced the influence of outliers [cite: 932][cite_start], and improved the overall validity of regression assumptions[cite: 943].

### 3. Feature Selection & Diagnostics
* [cite_start]**Stepwise AIC Selection**: Used the `stepAIC` process to identify the most efficient predictor set, leading to the removal of non-significant variables like `table` and `y`[cite: 1231, 1239].
* [cite_start]**VIF Analysis**: Conducted **Variance Inflation Factor (VIF)** tests to detect and remove redundant variables (`x`, `z`) that were causing severe multicollinearity[cite: 1368, 1370].
* **Final Model Formula**:
    [cite_start]$$\log(\text{price}) \sim \log(\text{carat}) + \text{cut} + \text{color} + \text{clarity} + \text{depth}$$ [cite: 1371]

## 💻 Tech Stack
* **Language**: R
* [cite_start]**Libraries**: `tidyverse`, `GGally`, `MASS`, `car`, `knitr`, `patchwork` [cite: 53, 291, 1114, 1241, 1318, 293]
* [cite_start]**Techniques**: Multiple Linear Regression, Log Transformation, AIC Stepwise Selection, VIF Diagnostics, Confidence & Prediction Intervals [cite: 1362, 1367, 1368, 1373]

## 📈 Prediction Example
[cite_start]For a diamond with **0.3 carat**, **Very Good cut**, **E color**, **SI1 clarity**, and **63.2 depth**[cite: 1374]:
* [cite_start]**95% Confidence Interval (Mean Price)**: \$506 – \$541[cite: 1375].
* [cite_start]**95% Prediction Interval (Individual Price)**: \$403 – \$671[cite: 1376].

---
[cite_start]*This analysis was completed as part of the Pstat 126 final project (December 2025).* [cite: 49, 50]

This repository contains the final project report for a statistics/data analysis project. 
All analysis, methodology, results, and conclusions are documented in the PDF.
