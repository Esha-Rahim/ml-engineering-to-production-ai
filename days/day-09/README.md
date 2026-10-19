# Day 9 — Linear Regression with Scikit-learn

## Date
October 19, 2026

## Topics Covered

### 1. Scikit-learn Foundations
- Purpose of Scikit-learn
- Scikit-learn vs. NumPy
- Estimators, transformers, and predictors
- The fit–predict workflow
- `LinearRegression`

### 2. Data Preparation
- Features (`X`) and target (`y`)
- Feature matrix and target vector shapes
- Samples and features
- NumPy arrays and data types
- Missing values and data inspection
- Preparing data for model training

### 3. Training a Linear Regression Model
- Creating a `LinearRegression` object
- `fit()`
- Learned coefficients (`coef_`)
- Intercept (`intercept_`)
- `n_features_in_`
- `predict()`
- Predictions for single and multiple observations

### 4. Mathematical Connection
- Linear regression equation
- Matrix-vector multiplication
- Learned parameters and predictions
- Residuals and MSE
- Comparing Scikit-learn with the NumPy implementation
- Understanding the work handled internally by Scikit-learn

### 5. Model Evaluation
- Actual vs. predicted values
- Residual calculations
- Mean Squared Error (MSE)
- `mean_squared_error`
- Training error vs. unseen-data evaluation
- Interpreting evaluation metrics
- Limitations of a single metric

### 6. Important Methods and Attributes
- `fit()`
- `predict()`
- `coef_`
- `intercept_`
- `score()`
- `n_features_in_`
- \(R^2\) score
- \(R^2\) vs. MSE
- Methods vs. learned attributes

### 7. Linear Regression Assumptions
- Linearity
- Independence of observations and errors
- Constant error variance (homoscedasticity)
- Residual normality and statistical inference
- Multicollinearity
- Effects of violated assumptions
- Statistical assumptions vs. software requirements

### 8. Implementation Choices
- Selecting features and target
- Choosing an evaluation metric
- `fit_intercept`
- `copy_X`
- `positive`
- Data representation
- Training and evaluation data separation
- Reproducibility

### 9. Common Failure Modes
- Incorrect feature shapes
- Confusing rows and columns
- Mismatched feature and target lengths
- Incorrect target values
- Incorrect prediction feature dimensions
- Misinterpreting coefficients and intercept
- Evaluating only on training data
- Confusing \(R^2\) with MSE
- Ignoring residual patterns
- Assuming Scikit-learn fixes poor-quality data
- Drawing conclusions without considering the dataset

### 10. Controlled Experiment
- Creating a small regression dataset
- Fitting a Scikit-learn model
- Generating predictions
- Calculating residuals and MSE
- Comparing against a NumPy implementation
- Checking coefficients and intercept
- Recording assumptions, results, and limitations
- Recording debugging observations
- Interpreting results in an ML context

### 11. Importance for an ML Engineer
- Using standard ML libraries
- Understanding model APIs
- Connecting mathematical foundations with implementation
- Building reliable training workflows
- Evaluating models correctly
- Debugging data and shape errors
- Producing reproducible experiments


## Key Takeaways

- Scikit-learn provides a standard workflow for fitting and using regression models.
- `fit()` learns model parameters, while `predict()` generates predictions.
- Coefficients and the intercept define the fitted linear relationship.
- MSE and \(R^2\) measure different aspects of model performance.
- Training performance alone does not establish generalization.
- Data shapes, assumptions, and evaluation choices matter.


