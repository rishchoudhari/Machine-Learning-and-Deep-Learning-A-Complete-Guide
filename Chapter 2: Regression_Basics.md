# Regression Basics

Supervised Learning uses known answers during training to predict a continous value or categories.

###### Regression - ######
When a function maps features (x) to a continous output (y), it is called a Regression Function.

There are two situations where Regression is used -

a) How variables are related or influenced

b) Predictions or forecaste responses

Advantage of Regression - Ease of interpretting results.

Example of Regression - Price of Car (y) determined by features Milage (x1), Year Made (x2), Model (x3), ..., (xr).

## Basic Notation ##

f(x) = y = actual output

x = input or independent variable or feature

x1, x2, x3,... = Different inputs or features

r = number of features

i = iteration

## Regression Formula ##

###### f(x) = β0 + β1 * x1 + β2 * x2 + ... + βr * xr + ε ######

β0 = intercept (value of f(x) when all x's are 0)

β1, β2, βr = Slope or Regression Coeffiecients.

ε = random error or noise (Greek Letter Epsilon)

## Estimated Regression Function ##

The real mathematical relationship between inputs and outputs is unkown. All we have is examples of inputs and their corresponding outputs, a.k.a Data.
Linear Regression uses those examples to learn a rule that -

- Approximates the real relationship
- Predicts new outputs
- captures the main patterns in the data

*This learned rule is the Estimated Function.*

## Estimated Regression Model ##
### (What is actually Computed) ###

###### ^f(x) = b0 + b1 * x1 + b2 * x2 + ... + br * xr ######

f(x) = true regression function (which is unkown)
^f(x) = estimated regression function (which is the model)

β = True regression coefficients (they describe how the world actually works)
b = estimated coefficients (they are the model's best guess of true β's)

## Residuals ##

The difference between predicted responses (^f(x)) for each observation (i=n) and the actual response (f(x)) is called the Residual.
The weight that corresponds to the smallest residual is what Regression wants to determine.

## Residual Formula ##

###### ei = f(x)i - ^f(x)i ######

Usually to get the best weight we minimize the Sum of Least Squared (SSR) for all observations. This approach is called Method of Ordinary Least Squares (OLS.)

###### SSR = Σi (f(x)i - ^f(x)i)^2 ######

## How to measure Regression Performance ##

R^2 = Performance Metric

Residual Sum of Squares (RSS) = How much variation the model did not capture

Explained Sum of Squares (ESS) = How much variation the model successfully captured

Total Sum of Squares (TSS) = RSS + ESS = How much the actual values (f(x)) varry around their mean. Total variation in data.

###### R^2 = ESS/TSS = 1 - (RSS/TSS) ######

![Least Square Picture](https://upload.wikimedia.org/wikipedia/commons/e/ed/Least_Squares.gif)
*Least Squares gif*

