# Speed Dating Classification Model Optimizer

## Author : Eduardo Gonzalez

We recently established an innovative dating advice company with a mission to guide individuals discovering the love of their life.Building on a foundation of expertise in relationship dynamics and modern dating trends, our approach is data-driven.

We've been gathering insights from our clients' feedback post their speed dating experiences, allowing us to understand the intricate factors that influence a successful date. Using this invaluable data, our aim is to construct a predictive model that can accurately forecast the likelihood of a date reaching a successful conclusion.

With the predictions from this model, we are better positioned to offer personalized advising sessions. During these sessions, we'll go deep into the nuances of online dating profiles, understanding what truly makes a profile stand out and how to effectively communicate to resonate with potential matches.

## Data Sources

For this problem, we're using the SpeedDating data source from [Columbia University](http://www.stat.columbia.edu/~gelman/arm/examples/speed.dating/). Let's try to find what makes a couple match based on surveys taken before and after the speed dating session.

The dataset includes preferences about the person and the potential partner on the moment of the speed date.

### Questions to consider:

* What is the best model to predict in an efficient way if a couple will match or not. Logistic Regression or Decision Trees?
* What are the best hyperparameters to optimize the prediction models
* What are important factors into determining if a couple will match or not?

## Methods

First we did some data cleaning and EDA (Being careful of not making data leakage), and we got this demographics results:

![Age Distribution of our Dataset](/images/age_distribution_dataset.png)
![Gender and Race Distribution Dataset](/images/demographics_dataset.png)

After it, we run our Baseline models, for Logistic Regression and for Decision trees, compare our baseline results with the same models with adjusted Hyperparameters, and run the best performing model to improve the accuracy.

## Results

Out of the two models to compare, the best performing one was the DecisionTree. And the best Hyperparameters:

* criterion = gini
* max_depth = 4
* min_samples_leaf = 1
* min_samples_split = 2

Here we can see some plots of our best performing model.

![Decision Tree](/Images/dt_polynomial.png)
![Confusion Matrix](/Images/cm_polynomial.png)
![ROC Curve](/Images/roc_curve_polynomial.png)

We also looked at the top features based on importance and we find that one of the most important features are:

* Whether the couple liked each other or not.
* If they found each other attractive
* The amount of shared interest they have

## Recommendations

* Create workshops for grooming and style
* Classes to break the ice to avoid the effect of meeting someone else.
* Create Premium Tier to make people more likely to match

## Next Steps

* We can create subsets by race or gender so we can further analyze what are the most important factors for each sub-category at the moment of finding a partner.
* We can extract the non-important features and evaluate how our model performs.
* We can also extract from our analysis the features that are more important when matching and creating personalized recommendations
