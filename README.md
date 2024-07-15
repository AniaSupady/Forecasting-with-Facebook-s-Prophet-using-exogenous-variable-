# Forecasting-with-Facebook-s-Prophet-using-exogenous-variable-

---
https://github.com/AniaSupady/Forecasting-with-Facebook-s-Prophet-using-exogenous-variable-/blob/main/Facebook's_Prophet.ipynb


---


Prophet is a forecasting tool developed by Facebook designed to handle time series data that displays patterns on different time scales such as daily, weekly, monthly, etc. It is particularly useful for datasets that exhibit strong seasonal effects and has been widely adopted due to its simplicity and ability to produce high-quality forecasts.

Key Features of Prophet:
Additive Model: Prophet decomposes a time series into three main components: trend, seasonality, and holidays (if provided). It models the time series using an additive model where these components are combined linearly:
y(t)=g(t)+s(t)+h(t)+ϵt
​
g(t): Trend component representing non-periodic changes.
s(t): Seasonal component capturing periodic changes (daily, weekly, yearly).
h(t): Holiday effects representing one-off events that impact the time series.
ϵt: Error term accounting for any remaining variation.

Flexible Seasonality: Prophet can handle both yearly and weekly seasonality, and it can also accommodate daily seasonality for datasets with high-frequency data.

Holiday Effects: It allows users to include known holidays and special events that impact the time series. These events are modeled using indicator variables that mark the occurrence of holidays.

Automatic Changepoint Detection: Prophet detects changepoints or abrupt changes in the time series trend. It identifies where the time series growth rate significantly shifts, allowing the model to adapt to these changes.

Uncertainty Estimation: Prophet provides uncertainty intervals for the forecasted values. By default, it generates 80% and 95% uncertainty intervals to quantify the uncertainty associated with the predictions.

Generalized Additive Model (GAM) Framework:
Additive Components: Prophet decomposes the time series into several additive components:

Trend Component (g(t)): Represents non-periodic changes in the time series. Prophet models this as a piecewise linear or logistic function.

Seasonal Component (s(t)): Captures periodic changes, such as daily, weekly, and yearly seasonality. Prophet can flexibly model seasonality using Fourier series.

Holiday Component (h(t)): Accounts for effects of holidays and other known events that influence the time series. These are modeled as binary indicator variables.

Error Component (𝜖𝑡ϵ t ): Represents the residual or error term capturing any remaining variability not explained by the trend, seasonality, and holidays.

Changepoints: Prophet automatically detects changepoints in the trend where the growth rate significantly shifts. These changepoints allow the model to adapt to changes in the time series behavior.

Uncertainty Estimation: Prophet provides uncertainty intervals (prediction intervals) around the forecasted values, indicating the range within which future observations are expected to fall with a specified probability (e.g., 80% or 95%).

Differences from Traditional Regression:
Flexibility in Trend and Seasonality: While traditional regression models may assume a linear relationship between predictors and the target variable, Prophet's trend and seasonal components can be non-linear and are more flexible. This allows Prophet to capture complex patterns in time series data without requiring explicit feature engineering of the predictors.

Handling Seasonality: Traditional regression models often struggle with capturing seasonal patterns effectively, especially if the seasonality is complex or changes over time. Prophet's Fourier series approach for modeling seasonality allows it to handle various seasonal patterns with ease.

Automated Feature Engineering: Prophet automates the process of feature engineering to some extent by internally handling seasonality, holidays, and trend detection, reducing the need for manual feature selection and engineering.

In summary, while Prophet utilizes components that can be conceptually related to regression (such as trend, seasonality, and error terms), its approach and methodologies are designed specifically for time series forecasting rather than traditional regression analysis. It leverages a generalized additive model framework tailored to handle the characteristics and complexities often found in time series data.
