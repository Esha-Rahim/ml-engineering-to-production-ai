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

## Practical Implementation

- [ ] Create or select a small dataset with actual and predicted values.
- [ ] Calculate residuals manually and with NumPy.
- [ ] Calculate squared errors and SSE.
- [ ] Calculate MSE.
- [ ] Verify NumPy calculations against manual results.
- [ ] Compare two sets of predictions.
- [ ] Inspect or plot residuals for patterns.

## Experiment Record

- **Assumption:** Actual and predicted values correspond to the same observations.
- **Result:** Record the actual calculated SSE/MSE and the comparison result.
- **Limitation:** MSE is sensitive to large errors and depends on the target's scale.
- **Debugging observation:** Record an issue you actually encountered and how you checked or resolved it.

## Key Takeaways

- A residual is the actual value minus the predicted value.
- Squared errors prevent positive and negative residuals from cancelling.
- SSE is the sum of squared errors.
- MSE is the average of squared errors.
- Large errors have a stronger influence on MSE.
- Lower MSE on one dataset does not guarantee better performance on unseen data.
- Residual analysis can reveal patterns that a single metric may hide.

## Self-Check

- [ ] Explain residuals without notes.
- [ ] Calculate residuals for a set of predictions.
- [ ] Explain the difference between residuals, squared errors, SSE, and MSE.
- [ ] Calculate MSE manually and with NumPy.
- [ ] Explain why errors are squared.
- [ ] Explain why MSE is sensitive to large errors.
- [ ] Explain why training MSE does not guarantee good test performance.
- [ ] Identify one failure mode or trade-off.
- [ ] Record anything that remains unclear.

## Resources

- [3Blue1Brown — Essence of Linear Algebra](https://www.youtube.com/playlist?list=PLZHQObOWTQDPD3MizzM2xVFitgF8hE_ab)
- [NumPy — Absolute Beginners](https://numpy.org/doc/stable/user/absolute_beginners/)
- [NumPy — Quickstart](https://numpy.org/doc/stable/user/quickstart.html)
- [CampusX — 100 Days of Machine Learning](https://learnwith.campusx.in/s/preview/courses/100-Days-of-Machine-Learning-YouTube-1763210027804-6918732bee601b12112865e6)

## GitHub Deliverable

- [ ] Add the completed learning log and implementation.
- [ ] Write a short reflection based on the work actually completed.
- [ ] Commit changes with a descriptive message.
- [ ] Update the README, tests, or experiment log if the work changes the public interface or results.

**Suggested commit message:**

`Add Day 7 MSE and residuals notes`

## Profile Evidence

No public LinkedIn post required. Save one genuine evidence item, such as an MSE result, residual plot, debugging note, or lesson learned, for future profile updates.
