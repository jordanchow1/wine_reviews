# Wine Reviews
## Overview
Conducted exploratory data analysis (EDA) of price, country of origin, rating. Preprocessed wine reviews by tokenizing strings into
words and converting them into dummy variables. Trained price prediction models using Linear Regression, Polynomial Regression,
and Random Forest, along with country of classification of country of origin using Random Forest, Logistic Regression, and K-Means Clustering. 
Model Performance was measured with Mean Squared Error (MSE), F1 score, residual plots, and system runtime. K-fold Cross Validation
was used for all models.

### Prerequisites
- Python 3, Git Large File Storage (LFS), Pandas, Numpy, Matplotlib, Seaborn, Scikit-learn.

## Data
- Wine Reviews on Kaggle: https://www.kaggle.com/zynicide/wine-reviews
- From the sample of 119955, stratified sampling was used to subsample 500 and 5000 data points for model training to account for differing label proportions.

## EDA Findings
- Moderate positive correlation between Prices and Ratings with a Pearson's Coefficient of 0.416.
- Prices follow a Poisson distribution with most values ranging between 0 and 50 (Linear regression might not be ideal)
- Pinot Noir is the most reviewed variety, followed by Chardonnay, Cabernet Sauvignon, and Red Blend.

## Regression Findings
- Prices are nonlinear where when using linear regression prices on the higher end tend to vary more. Polynomial regression with 2 degrees was used to counter the issue.

![residual plot linear](https://github.com/jordanchow1/wine_reviews/blob/master/snapshots/residual_plot_linear.png)

## Model Performance - Price Prediction
### Random Forest
- MSE: 2257.94
- Runtime: 6.296 sec
### Linear Regression
- MSE: 2703.435
- Runtime: 0.1965 sec
### Polynomial Regression
- MSE: 2181.255
- Runtime: 146.910 sec

## Model Performance - Country Classification
### Random Forest
- F1 score: 0.973
- Runtime: 269.55 sec

### Logistic Regression
- F1 score: 0.988
- Runtime: 30.44 sec

### K-Means Clustering
- F1 score: 0.165
- Runtime: 202.10 sec

## Snapshots
### Residual Plots - Price Prediction
![](https://github.com/jordanchow1/wine_reviews/blob/master/snapshots/residual_plot_rf.png)
![](https://github.com/jordanchow1/wine_reviews/blob/master/snapshots/residual_plot_linear.png)
![](https://github.com/jordanchow1/wine_reviews/blob/master/snapshots/residual_plot_poly.png)

### Confusion Matrix - Country Classification
![](https://github.com/jordanchow1/wine_reviews/blob/master/snapshots/cm_rf.png)
![](https://github.com/jordanchow1/wine_reviews/blob/master/snapshots/cm_linear.png)
![](https://github.com/jordanchow1/wine_reviews/blob/master/snapshots/cm_kmeans.png)

### EDA
![](https://github.com/jordanchow1/wine_reviews/blob/master/snapshots/num_reviews.png)