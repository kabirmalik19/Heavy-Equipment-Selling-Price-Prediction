# Heavy-Equipment-Selling-Price-Prediction

## Project Overview
This repository contains a machine learning workflow designed to predict the selling price of heavy equipment. By accurately forecasting secondary market values, this project supports data-driven purchasing and sales strategies. The architecture relies on an ensemble regression approach to navigate the high dimensionality and non-linear relationships inherent in industrial machinery data.

## Data Pipeline & Modeling
The project utilizes a comprehensive Python pipeline to clean the data, extract features, and train the predictive models.

Exploratory Data Analysis (EDA): Identifies historical pricing trends, feature distributions, and missing data points across various equipment categories.

Feature Engineering: Applies log-transformations to target variables and heavily skewed features to stabilize variance and improve model convergence.

Gradient Boosting: Deploys XGBoost and LightGBM to capture complex, non-linear interactions within the dataset.

Model Ensembling: Combines the predictive power of both gradient boosting models using a Scikit-Learn VotingRegressor to mitigate individual model biases and prevent overfitting.

## Evaluation & Results
The primary evaluation metric for this task is the Root Mean Squared Logarithmic Error (RMSLE). This metric is highly effective for pricing models because it penalizes relative differences rather than absolute scale, preventing expensive machinery from dominating the error calculation.
<img width="469" height="92" alt="Screenshot 2026-09-20 131348" src="https://github.com/user-attachments/assets/d40d05bc-f7e4-4163-9b10-4ba89df28314" />


Ensemble Performance: The final VotingRegressor pipeline achieved an RMSLE score of 0.19, indicating strong predictive accuracy across varying price brackets.

