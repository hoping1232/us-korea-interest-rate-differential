# U.S.–Korea Interest Rate Differential and KRW/USD Exchange Rate

## 📌 Project Overview

This project examines whether differences between U.S. and South Korean policy interest rates are associated with movements in the KRW/USD exchange rate using monthly time-series data. The analysis explores both contemporaneous and lagged relationships and evaluates the explanatory power of simple linear regression models commonly used in international macroeconomics.

---

## 📊 Data Description

The dataset consists of monthly observations from January 2005 to January 2025 and includes:

- U.S. policy interest rate (Federal Funds Rate, FRED)
- South Korean policy interest rate (FRED)
- KRW/USD nominal exchange rate (FRED)

After merging the series and removing missing values, the dataset is suitable for regression-based time-series analysis.

---

## 🧪 Methodology

### 1. Interest Rate Differential

The key explanatory variable is the interest rate differential, defined as the difference between the U.S. policy rate and the South Korean policy rate:
Interest Rate Differential = r_US − r_KR

Positive values of the differential indicate periods when U.S. interest rates exceeded those of South Korea.

---

### 2. Exchange Rate Dynamics

To provide a visual overview of exchange rate behavior, the KRW/USD exchange rate is plotted over time. The series exhibits substantial volatility, particularly during periods of global financial stress, suggesting that exchange rate movements are influenced by broader macroeconomic and financial factors beyond interest rates alone.

A scatter plot of the exchange rate against the interest rate differential is also examined. The plot suggests no strong linear relationship between the two variables, with substantial dispersion across observations.

---

### 3. Baseline Regression Analysis

An ordinary least squares (OLS) regression is estimated with the KRW/USD exchange rate as the dependent variable and the interest rate differential as the explanatory variable.

The estimated coefficient on the interest rate differential is positive but not statistically significant at conventional levels. The model explains only a small fraction of the variation in the exchange rate, as indicated by the low R-squared value. This suggests that most of the variation in the KRW/USD exchange rate is driven by factors not captured in this simple model.

The Durbin–Watson statistic is well below 2, indicating strong positive serial correlation in the residuals. This implies that a simple OLS specification may be insufficient for modeling exchange rate dynamics in a time-series context.

---

### 4. Lagged Interest Rate Differential

To account for potential delayed effects, a one-period lag of the interest rate differential is constructed and used as the explanatory variable in an alternative regression specification.

The coefficient on the lagged interest rate differential remains positive but is not statistically significant, and the explanatory power of the model remains very limited. The low Durbin–Watson statistic again points to serial correlation in the residuals, reinforcing the limitations of a simple OLS approach.

---

### 5. Log Transformation and First Differences

To address potential non-stationarity in the exchange rate series, the KRW/USD exchange rate is transformed using logarithms and first differences. The log-differenced exchange rate approximates percentage changes and helps stabilize the variance of the series, making it more suitable for time-series regression analysis.

Regression results using the log-differenced exchange rate as the dependent variable show no statistically significant relationship between interest rate differentials and exchange rate changes. The model’s explanatory power remains very low.

---

## ✅ Conclusion

Overall, the results suggest that U.S.–Korea interest rate differentials alone do not provide a strong explanation for KRW/USD exchange rate movements. Across contemporaneous, lagged, and log-differenced specifications, the estimated relationships are weak and statistically insignificant.

The presence of serial correlation and low explanatory power highlights the importance of considering additional macroeconomic factors—such as global risk sentiment, capital flows, and expectations—as well as more advanced time-series models in future research.

