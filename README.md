# Diamond Price Prediction: Regression Modeling Project

This project explores the relationship between diamond prices and their physical characteristics to build an accurate and interpretable predictive model. Using a dataset of **1,000 observations** , I applied advanced regression techniques, including **log-log transformations** and **stepwise AIC selection** , to explain approximately **98.4% of price variation**.

## Key Findings

* **Primary Predictor**: **Carat** is the most powerful indicator of price, initially explaining 85% of variance in a simple model.
* **Quality Factors**: Categorical variables—**Cut, Color, and Clarity**—significantly improve model performance, reflecting that diamond quality plays a major role in real-world pricing.
* **Model Accuracy**: The final model achieved an **Adjusted $R^2$ of 0.9838** , with a low Residual Standard Error (RSE) of 0.1289 on the log scale.

##  Statistical Workflow

### 1. Exploratory Data Analysis (EDA)
* **Skewness Detection**: Identified strong right-skewness in both `price` and `carat`.
* **Correlation Analysis**: Discovered high correlations among size-related variables like `x`, `y`, and `z`.

### 2. Model Transformation & Improvement
* **Log-Log Transformation**: Applied a log transformation to both the response (`price`) and the predictor (`carat`) to address violations of **normality** and **homoscedasticity**.
* **Linearization**: The transformation stabilized variance, reduced the influence of outliers, and improved the overall validity of regression assumptions.

### 3. Feature Selection & Diagnostics
* **Stepwise AIC Selection**: Used the `stepAIC` process to identify the most efficient predictor set, leading to the removal of non-significant variables like `table` and `y`.
* **VIF Analysis**: Conducted **Variance Inflation Factor (VIF)** tests to detect and remove redundant variables (`x`, `z`) that were causing severe multicollinearity.
* **Final Model Formula**:
    $$\log(\text{price}) \sim \log(\text{carat}) + \text{cut} + \text{color} + \text{clarity} + \text{depth}$$
  
## Tech Stack
* **Language**: R
* **Libraries**: `tidyverse`, `GGally`, `MASS`, `car`, `knitr`, `patchwork` 
* **Techniques**: Multiple Linear Regression, Log Transformation, AIC Stepwise Selection, VIF Diagnostics, Confidence & Prediction Intervals.

All analysis, methodology, results, and conclusions are documented in the PDF.
