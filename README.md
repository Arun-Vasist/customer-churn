# Analysing customer churn with R

We analyse customer churn data to find the factors leading to churn.

The analysis is divided into three parts.
1. EDA
2. Modelling with tidymodels
3. H2O AutoML

## Part 1: EDA

For EDA we use the following packages -
1. ggplot
2. DataExplorer
3. funModeling
4. cowplot
5. corrr

These plots are produced with ggplot and cowplot.
![Grid 1](https://github.com/Arun-Vasist/customer-churn/blob/master/grid1.png)
![Grid 2](https://github.com/Arun-Vasist/customer-churn/blob/master/grid2.png)

## Part 2: Modelling

#### In part 2 we will train machine learning models to see what factors are leading to Churn.
#### We use tidymodels packages like parsnip, recipes, tune, dials, yardstick to create models.

### Accuracy vs Interpretability Tradeoff

#### Linear models are more interpretable but usually are not very accurate.
#### We will examine both linear model and a more complex model like xgboost in Part 2.

These are the coefficients obtained from logistic regression -

![Coef plot](https://github.com/Arun-Vasist/customer-churn/blob/master/coef_plot.png)

This are the feature importances from xgboost -

![Feature Importances](https://github.com/Arun-Vasist/customer-churn/blob/master/coef_plot.png)

### Next we perform correlation analysis -
![Corr plot](https://github.com/Arun-Vasist/customer-churn/blob/master/corr_plot.png)


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







