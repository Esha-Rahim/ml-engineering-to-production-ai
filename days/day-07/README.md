# Day 7 — MSE and Residuals

## Date
October 14, 2026

## Topics Covered

### 1. Prediction Errors
- Actual values vs. predicted values
- Definition and calculation of prediction error
- Positive and negative prediction errors
- Error magnitude and its interpretation
- Importance of prediction errors in regression

### 2. Residuals
- Definition of a residual
- Residual formula: actual value minus predicted value
- Positive, negative, and zero residuals
- Residual magnitude
- Calculating residuals manually and with NumPy
- Residuals as vertical distances from a fitted regression line
- Residuals across multiple observations

### 3. Residuals and the Regression Line
- Observed data points vs. predicted points
- Relationship between a fitted line and residuals
- How different fitted lines produce different residuals
- Perfect predictions and zero residuals
- Comparing residuals from candidate regression lines
- Introduction to residual plots
- Identifying potential problems through residual patterns

### 4. Squared Errors
- Definition and formula for squared error
- Squaring residuals
- Calculating squared errors
- Why positive and negative errors become non-negative
- Greater penalty for larger errors
- Residuals vs. squared errors
- Sensitivity to large errors and outliers

### 5. Sum of Squared Errors (SSE)
- Definition and formula for SSE
- Adding squared residuals
- Manual SSE calculation
- Interpreting SSE values
- Comparing SSE between models
- Effect of sample size on SSE
- Limitations of SSE when comparing datasets of different sizes

### 6. Mean Squared Error (MSE)
- Definition and purpose of MSE
- MSE formula:

  `MSE = (1/n) × Σ(yᵢ − ŷᵢ)²`

- Meaning of actual values, predictions, and number of observations
- Step-by-step MSE calculation
- Relationship between residuals, squared errors, SSE, and MSE
- MSE as the average squared prediction error
- Interpreting lower MSE on the same evaluation dataset
- MSE units and target scale
- MSE vs. average absolute error
- MSE vs. root mean squared error (RMSE)

### 7. Why Errors Are Squared and Averaged
- Cancellation of positive and negative residuals
- Why squaring prevents signed errors from cancelling
- Greater influence of large errors
- Why MSE averages errors
- Comparing datasets with different sample sizes
- Trade-offs of using squared errors
- MSE as a regression loss function

### 8. Comparing Models
- Comparing prediction errors and residuals
- Calculating MSE for different prediction sets
- Comparing models on the same dataset
- Training error vs. test error
- Why low training MSE does not guarantee good generalization
- Overfitting and unseen-data performance
- Using residual patterns alongside MSE

### 9. Residual Patterns and Limitations
- Randomly scattered residuals
- Patterns that may suggest nonlinear relationships
- Changes in residual spread
- Unusual observations and large residuals
- Individual errors vs. systematic patterns
- Limitations of residual analysis
- Why low MSE can hide important errors
- Importance of domain context

### 10. Assumptions and Implementation Choices
- Matching actual and predicted observations
- Compatible array shapes
- Matching numbers of actual and predicted values
- Choosing an appropriate error metric
- Calculating residuals with NumPy
- Calculating squared errors, SSE, and MSE with NumPy
- Verifying results with manual calculations
- Mathematical definitions vs. code implementation

### 11. Common Failure Modes
- Reversing the residual formula
- Confusing residuals with squared errors
- Forgetting to square residuals
- Forgetting to divide SSE by the number of observations
- Using incorrect observation counts
- Comparing MSE across different datasets without context
- Mismatched array shapes
- Assuming lower training MSE proves a better model
- Ignoring outliers and large errors
- Misinterpreting MSE units
- Relying on MSE without residual analysis or test evaluation
- Failing to verify calculations

### 12. Importance for an ML Engineer
- Measuring regression prediction errors
- Diagnosing model errors
- Comparing regression models
- Understanding loss functions
- Foundations for later optimization topics
- Understanding evaluation metric trade-offs
- Using error analysis to guide model improvements
- Verifying model outputs and numerical calculations

## Key Takeaways

- A residual is the actual value minus the predicted value.
- Squared errors prevent positive and negative residuals from cancelling.
- SSE is the sum of squared errors.
- MSE is the average of squared errors.
- Large errors have a stronger influence on MSE.
- Lower MSE on one dataset does not guarantee better performance on unseen data.
- Residual analysis can reveal patterns that a single metric may hide.


