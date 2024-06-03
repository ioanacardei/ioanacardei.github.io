---
layout: page
title:  S&P 500 predictions in R
description: Linear regresstion for stock index returns from 1990-2010 using R
img: assets/img/sp_500.jpg
importance: 2
category: work
giscus_comments: false
---

S&P 500 stock index from 1990 – 2010 
<br>
<br>
My project is using R to analyze Weekly data frame in ISLR package. This data frame contains 9 features for 1089 weeks of stock index returns from 1990 to 2010. Analysis was performed using tidyverse and glmnet packages.
<br>
<br>
First, I fit a ridge-penalized linear regression model and a lasso-penalized linear regression model to predict the percentage return today from the percentage return for the five previous weeks.
<br>
I considered 100 tuning parameter (λ) values evenly spaced between 0.001 and 1000 on a base-10 logarithmic scale and plotted the coefficients as a function of log(λ)
<br>
<br>
Code below: 
<br>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/r_1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<br>
Plots
<br>
<br>
Ridge-penalized model
<br>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/r_2.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<br>
Lasso-penalized model
<br>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/r_3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<br>
Next I performed 10-fold cross-validation for a ridge-penalized and for a lasso-penalized linear regression model to predict the percentage return today from the percentage return for the five previous weeks. For each model, I use the fit with the λ value that has the smallest cross-validation error rate in order to predict classes for the training data, then printed a confusion matrix and an estimate of classification training accuracy to the console.
<br>
<br>
Code/Results
<br>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/r_4.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<br>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/r_5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<br>

Explanation
<br>
<br>
In this project, I utilized ridge and lasso-penalized linear regression models to analyze weekly data of the S&P 500 stock index returns from 1990 to 2010. The goal was to predict the percentage return today based on the percentage returns for the five previous weeks.
<br>
<br>
Model Training and Evaluation
<br>
<br>
I began by fitting ridge and lasso-penalized linear regression models to the data. To determine the optimal regularization parameter (λ), I considered a range of 100 tuning parameter values evenly spaced between 0.001 and 1000 on a base-10 logarithmic scale. The coefficients were plotted as a function of log(λ) to understand the effect of regularization on feature selection.
<br>
The ridge-penalized model revealed the following coefficients for the features:
<br>
<br>
- Intercept: 0.22613475
<br>
- Lag1: -0.02110663
<br>
- Lag2: 0.03112942
<br>
- Lag3: -0.00860878
<br>
- Lag4: -0.01146716
<br>
- Lag5: -0.00719927
<br>
<br>
The model achieved an accuracy of approximately 55.56% on the training data. True "Up" predictions accounted for 99% of the actual "Up" movements, while true "Down" predictions accounted for 1.2% of the actual "Down" movements.
<br>
<br>
 
The lasso-penalized model resulted in the following coefficients for the features:
<br>
<br>
- Intercept: 0.22041644
<br>
- Lag1: -0.01562924
<br>
- Lag2: 0.03671116
<br>
- Lag3: Not significant
<br>
- Lag4: Not significant
<br>
- Lag5: Not significant
<br>
<br>
Despite some coefficients being set to zero, the model achieved a similar accuracy of approximately 55.46% on the training data. True "Up" predictions represented 98.6% of the actual "Up" movements, while true "Down" predictions represented 1.4% of the actual "Down" movements.
<br>
<br>
Both ridge and lasso-penalized linear regression models demonstrated comparable performance in predicting S&P 500 stock index returns based on past data. While the lasso model provided a more parsimonious solution by setting some coefficients to zero, both models achieved similar accuracy rates. These findings suggest that either model could be used effectively for predicting stock market movements based on historical data within the given timeframe.
<br>
<br>
The analysis provides valuable insights into the application of penalized regression techniques in financial forecasting, offering a robust framework for future research and decision-making in investment strategies. Further exploration could involve refining the model parameters, incorporating additional features, or extending the analysis to different time periods or financial markets.

