# Analysing customer churn with R

We analyse customer churn data to find the factors leading to churn.

The analysis is divided into three parts.
1. [EDA](#part-1:-eda)
2. [Modelling with tidymodels](#part-2:-modelling)
3. [H2O AutoML and Gain Lift charts](#part-3:-h2o-and-gain-lift-charts)

## Part 1: EDA

For EDA we use the following packages -
1. ggplot
2. DataExplorer
3. funModeling
4. cowplot
5. corrr

These plots are produced with ggplot and cowplot.
<img src="https://github.com/Arun-Vasist/customer-churn/blob/master/grid1.png" width="600" height="600" />
<img src="https://github.com/Arun-Vasist/customer-churn/blob/master/grid2.png" width="600" height="600" />


### Next we perform correlation analysis -
<img src="https://github.com/Arun-Vasist/customer-churn/blob/master/corr_plot.png" width="600" height="600" />


### Factors with which churn increases -
* Month to month contract
* No online security
* Fiber optic internet users
* No tech support
* Electronic check payment method
* No online backup
***
### Factors with which churn decreases -
* High tenure
* Two year contract
* No internet service


## Part 2: Modelling

#### In part 2 we will train machine learning models to see what factors are leading to Churn.
#### We use tidymodels packages like parsnip, recipes, tune, dials, yardstick to create models.

<img src="https://github.com/tidymodels/tidymodels/blob/master/tidymodels_hex.png" width="200" height="200" />

### Accuracy vs Interpretability Tradeoff

#### Linear models are more interpretable but usually are not very accurate.
#### We will examine both linear model and a more complex model like xgboost in Part 2.

These are the coefficients obtained from logistic regression -

<img src="https://github.com/Arun-Vasist/customer-churn/blob/master/coef_plot.png" width="600" height="600" />

This are the feature importances from xgboost -

<img src="https://github.com/Arun-Vasist/customer-churn/blob/master/feature_importances.png" width="600" height="600" />

## Part 3: H2O and Gain Lift charts

<img src="https://github.com/Arun-Vasist/customer-churn/blob/master/h2o_logo.png" width="200" height="200" />

#### In part 3 we will use H2O AutoML to get a better model than xgboost model from part 2 with minimal effort.
#### Then we create Gain Lift charts to show executives how much better off we are due to the model.

With AutoML we get a logloss of 0.45 which is much better than what the 2.11 we got with xgboost in part 2.

Gain chart -

<img src="https://github.com/Arun-Vasist/customer-churn/blob/master/gain_chart.png" width="600" height="600" />

Lift chart -

<img src="https://github.com/Arun-Vasist/customer-churn/blob/master/lift_chart.png" width="600" height="600" />




