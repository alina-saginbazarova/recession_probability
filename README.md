# Prediction of the Probability of the Recession in the U.S. Based on the Yield Curve Using the Logistic Regression

This is the project aimed at replicating the Federal Reserve Bank's predictions of the probability of recession in the U.S. in the next twelve months. 
* Website: https://www.newyorkfed.org/research/capital_markets/ycfaq#/interactive

The Federal Reserve Bank uses the slope of the Treasury yield curve ("term spread") to predict the probability of the recession in the U.S. in the next twelve months.

Key model assumptions:
* Treasury term spread is the only predictor of the probability of the recession
* Treasury term spread is defined as the difference between the 10 year bond and 3 month bill rates
* The recession probabilities are predicted for the next 12 months
* I used the logistic regression to predict the probability of recession, whereas the Fed does not disclose the type of the model it chose 
* In line with the Fed, the parameters were trained using the data from January 1959 to December 2009
* The recession probabilities were predicted using the data through July 31, 2024

Model results:
* The Fed's estimated parameters are α= -0.5333, β= -0.6330.
* My estimated parameters using the logistic regression are α= -0.8913, β= -1.1542.

Observations and interpretation of the results: 
* The residual plot shows a clear U and inverted-U pattern, suggesting non-linear relationship between the fitted values and residuals. This might indicate that the simple logistic regression model is not adequately capturing the true relationship between the probabiilty of recession and the term spread. The model might be missing important interaction terms or higher-order terms or predictors need to be transformed.

Improvement suggestions:
* Check if transforming predictors or adding interaction terms improves the model
* Use Generalized Additive Models that model non-linear relationships using smooth functions
* Validate the model using k-fold cross validation
* Use Gamma distribution
