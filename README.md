# Wine-Quality-Prediction
## Problem: Predict the quality of wine
Type of Machine Learning used —
### Supervised Learning:
As the name suggests, Supervised Learning needs a human to “supervise” and tell the computer what it should be trained to predict for, or give it the right answer. We feed the computer with training data containing various features, and we also tell it the right answer.

To give an analogy, imagine the computer to be a kid who’s a blank slate. He knows nothing.

Now, how do you teach him the difference between a dog and a cat? It’s quite intuitive — you take him out for a walk, and when you see a cat, you point it out and say, “This is a Cat.” As you keep walking you might see a dog, so you again point it out and say “This is a Dog.” Over time, as you keep showing lots of dogs and cats, the kid will learn to differentiate between the two.

Of course, you can always show him lots of pics of dogs and cats instead of going out for a walk. Instagram to the rescue! :P

With respect to our wine data-set, our machine learning model will learn to co-relate between the quality of the wines, versus the rest of the attributes. In other words, it’ll learn to identify patterns between the features and the targets (quality).

### Multiple Linear Regression:
An extension of simple linear regression
In simple linear regression there is a one-to-one relationship between the input variable and the output variable. But in multiple linear regression, as the name implies there is a many-to-one relationship, instead of just using one input variable, you use several.

#### New considerations
Adding more input variables does not mean the regression will be better, or offer better predictions. Multiple and simple linear regression have different use cases, one is not superior. In some cases adding more input variables can make things worse, this is referred to as over-fitting.

#### Multicollinearity
When you add more input variables it creates relationships among them. So not only are the input variables potentially related to the output variable, they are also potentially related to each other, this is referred to as multicollinearity. The optimal scenario is for all of the input variables to be correlated with the output variable, but not with each other.

#### The model
The model for multiple linear regression is as you would expect, very similar to the one for simple linear regression. It goes as follows:
 #### f(X) = a + (B1 * X1) + (B2 * X2) … + (Bp * Xp).
Where X is the input variables and Xp is a specific input variable, Bp is the coefficient (slope) of the input variable Xp and a is the intercept. Let’s test this out with an example!

#### Preparation before doing multiple regression
  1.Collect a list of potential input variables and a potential output variable.
  2.Collect data on the variables.
  3.Check the correlation between each input variable and the output variable.
  4.Check the correlation among the input variables.
  5.Use the non-redundant input variables in the analysis to find the best fitting model.
### Backward Elimination:
  1.Select significance level
  2.Fit our model with all possible independent variables.
  3.Consider variable with highest p-value.
  4.If p-value is greater than significance level, remove variable
  5.Again fit the model without removed variable.
  Images after every Elimination is provided,named:OLS_1,OLS_2,..
### Plot: True Quality vs Predicted Quality

### R-squared
Linear regression calculates an equation that minimizes the distance between the fitted line and all of the data points. Technically, ordinary least squares (OLS) regression minimizes the sum of the squared residuals.
In general, a model fits the data well if the differences between the observed values and the model's predicted values are small and unbiased

R-squared is a statistical measure of how close the data are to the fitted regression line. It is also known as the coefficient of determination, or the coefficient of multiple determination for multiple regression.
The definition of R-squared is fairly straight-forward; it is the percentage of the response variable variation that is explained by a linear model. Or:

#### R-squared = Explained variation / Total variation

R-squared is always between 0 and 100% or 0 and 1:

0% or  indicates that the model explains none of the variability of the response data around its mean.
100% or 1 indicates that the model explains all the variability of the response data around its mean.
In general, the higher the R-squared, the better the model fits your data. 

### Conclusion
We predicted the quality of wine using Backward Elimination Multiple Linear Regression Model.
 R-square: 0.282
 Adj. R-square: 0.281
