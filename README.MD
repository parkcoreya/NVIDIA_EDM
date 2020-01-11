# Empirical Dynamic Modeling for predicting NVIDIA stock price

## Abstract
Conventional data analysis relies on statistical models for forecasting and to deduce variable relationships. Statistical models contain underlying assumptions and hypothesis about the data, for example, statistical independence is often presumed between variables, which can lead to erroneous statistical estimates such as inflated correlation coefficients between variables. Empirical dynamic modeling (EDM) is a data-driven, non-parametric framework for modeling nonlinear dynamic systems with minimal assumptions. This notebook presents an implementation of EDM (Simplex Projection using Nearest Neighbor Forecasting) to predict movements of NVIDIA stock price (NVDA).

Convergent Cross Mapping (CCM) is used to evaluate if outside variables are affecting the price of NVDA, and if adding them as features to the Simplex Projection will increase predicability of the model. Correlation is often insufficient as two variables can be highly correlated, but have no causal effect. CCM is an exploration of the cause and effect of two variables. It is done by looking at the predictability of one variable when the other variable is presumed to be the source of the dynamics.

The price of Bitcoin (BTC), supplier company stock price, and fed interest rates were examined to see if a causal relationship existed with NVDA price. No features were discovered that added power to the model. Despite this, a model using Simplex Projection of time-delay embedded NVDA price correctly predicted day to day directional movements of NVDA.

Next steps for this work are to identify external features that add power to the model. Since the stock market is largely affected by consumer perception/psychology, a useful feature to add to the model could be an aggregated metric of public perception of a stock based on social media feedback and news outlet articles.

The [pyEDM library](https://github.com/SugiharaLab/pyEDM) used for this implementation was developed by the [UCSD Sugihara Lab](https://deepeco.ucsd.edu/). Installation instructions can be found [here](https://github.com/SugiharaLab/pyEDM/blob/master/README.md).