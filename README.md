**📈 BAC Stock Predictive Analysis using Linear Regression**

- This project presents a comprehensive analysis and predictive modeling approach to forecasting the stock price of Bank of America (BAC) using Linear Regression. The repository covers the full data science workflow — from data acquisition to feature engineering, model building, evaluation, and diagnostic testing of regression assumptions.

** Project Overview**

- The primary objective of this project is to build an interpretable regression model to predict BAC's stock price based on historical market data. This is done using lag features, moving averages, and relevant index indicators. The model’s performance is evaluated using error metrics like Root Mean Squared Error (RMSE) and Mean Squared Error (MSE) to assess its predictive accuracy.

** Key Features**

- Data pulled using yfinance for BAC and major market indices.
- Feature engineering includes:
- Lag variables (e.g., BAC(t-1), QQQ(t-1), ^GSPC(t-1))
- Technical indicators like 5-day Moving Average
- Feature selection techniques were applied to reduce multicollinearity, improving model stability and interpretability.
- Linear Regression modeling with statsmodels.api

**Model evaluation using:**

- RMSE: 0.7358
- MSE: 0.5414

These values indicate a moderate prediction error, with the model deviating by approximately 0.73 units from actual stock prices on average.

**Regression Assumptions Checked**
- To ensure model robustness and statistical validity, all five key assumptions of linear regression were tested:

1) Linearity
- Verified through residual vs. fitted plots to confirm linear relationship between predictors and response.

2) Homoskedasticity
- Checked using residual plots to ensure constant variance across predictions.

3) Multicollinearity
- Tested using Variance Inflation Factor (VIF) from statsmodels.stats.outliers_influence to identify and remove highly correlated predictors.

4) Normality of Residuals
- Assessed using Q-Q plots and histograms of residuals to confirm approximate normal distribution.

5) Autocorrelation of Residuals
- Evaluated with the Durbin-Watson statistic to detect serial correlation in residuals.

** Tools & Libraries Used**
- numpy
- pandas
- yfinance – for pulling stock and index data
- matplotlib.pyplot & seaborn – for visualizations
- statsmodels.api – for building and interpreting the regression model
- statsmodels.stats.outliers_influence – for VIF and multicollinearity analysis

** Results & Next Steps**

- The model currently exhibits an RMSE of 0.7358, indicating a moderate average prediction error. While linear regression offers simplicity and interpretability, future enhancements could include:

- Feature selection or dimensionality reduction
- Applying regularized models like Ridge or Lasso
- Exploring nonlinear models such as Random Forest or XGBoost

** Disclaimer**

This project is for educational and illustrative purposes only and does not constitute financial advice.
