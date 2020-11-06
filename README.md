# E-commerce Website A/B Test Results Analysis
## Introduction
A/B tests are very commonly performed by data analysts and data scientists. This project will analyze the results of an A/B test run by an e-commerce website. The goal is to help the company understand if they should implement the new page, keep the old page, or perhaps run the experiment longer to make their decision.

## Hypothesis Testing
<img src="https://render.githubusercontent.com/render/math?math=converted\: success\: rate\: p = \frac{number\: of\: unique\: users\: who\: converted}{total\: number\: of\: unique\: users}">

H<sub>0</sub> : p<sub>new</sub> - p<sub>old</sub> &ge; 0

H<sub>1</sub>: p<sub>new</sub> - p<sub>old</sub> &lt; 0

Assume under the null hypothesis, p<sub>new</sub> and p<sub>old</sub> both have "true" success rates equal to the converted success rate regardless of page - that is p<sub>new</sub> and p<sub>old</sub> are equal to the converted rate in the dataset regardless of the page. Simulate sampling distribution of the difference in converted rate with bootstrapping 10000 times under the null hypothesis using the ‘true’ probability.

## Logistic Regression
* The result in the previous A/B test can also be acheived by performing logistic regression.
* In order to predict whether or not an individual converts, we need to have the individual factors as the predictors in the regression model. Country was chosesn to be the additional factor.
* Add interaction terms between type of page and country into the regression model to see if there significant effects on conversion.
* Add the influences associated with time on conversion.

## Summary and Conclusion
Hypothesis testing was an **aggregate** approach to understand whether or not the proportion of users that converts using old page is better than the average using new page. The results showed that there is no significantly difference in conversion rate between the two groups.

Logistic regression was an **individual** approach to understand whether or not an individual converts depends on the pages they see and which country are they from. The results showed that having country as additional factor and adding interaction terms into the logistic regression model are not useful in predicting the probability of conversion.
* The type of page does not correlate to the user conversion, which agrees with the A/B test.
* The country where the user lives is not a good predictor for user conversion.
* The interaction between type of page and country has no significant effects on conversion.
* Adding time factor provides no improvement in the model.
