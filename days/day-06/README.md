# Day 6 — Linear Regression Intuition

## Date
October 13, 2026

## Topics Covered

### 1. Understanding Linear Regression
- Definition and purpose of linear regression
- Linear regression as a supervised learning algorithm
- Regression problems and continuous target values
- Features (inputs) and target (output)
- Independent and dependent variables
- Real-world applications of linear regression
- When linear regression is and is not appropriate

### 2. Intuition Behind Linear Regression
- Representing data as points on a graph
- Understanding a line of best fit
- How a line represents a relationship between input and output
- Actual values versus predicted values
- Making predictions for new input values
- Linear relationships in data
- Positive, negative, and zero slope

### 3. Linear Regression Equation
- Simple linear regression equation
- Understanding `y = mx + c`
- Prediction equation: `ŷ = b₀ + b₁x`
- Meaning of input `x`, actual target `y`, and prediction `ŷ`
- Meaning of the intercept `b₀`
- Meaning of the slope or coefficient `b₁`
- How slope and intercept affect the fitted line
- Calculating predictions using the equation
- Simple versus multiple linear regression

### 4. Features, Coefficients, and Predictions
- How a feature contributes to a prediction
- Interpreting model coefficients
- Understanding the role of the intercept
- Combining multiple features to make a prediction
- Multiple linear regression equation
- Representing features using a feature matrix
- Model parameters versus input features

### 5. How Linear Regression Fits a Line
- Why a model needs to fit a line
- Prediction errors
- Introduction to residuals
- Actual values versus predicted values
- Positive and negative residuals
- Vertical distances between observed points and the fitted line
- How different lines produce different prediction errors
- Finding a line with low prediction error

### 6. Loss Function and Best-Fit Intuition
- Purpose of a loss function
- Squared errors
- Sum of squared errors
- Mean squared error (MSE)
- Why errors are squared
- Minimizing prediction error
- How changing a line affects its loss
- Least-squares intuition
- Training error versus performance on unseen data

### 7. Assumptions Behind Linear Regression
- Linearity assumption
- Recognizing approximately linear relationships
- Observations and features
- Influence of unusual observations
- Correlation versus causation
- Limitations of a straight-line relationship
- Checking assumptions against the data

### 8. Implementation Choices
- Manual calculations versus code-based calculations
- Representing input and target values with NumPy
- One-dimensional feature arrays
- Input and target array shapes
- Calculating predictions using slope and intercept
- Choosing a small dataset for experimentation
- Plotting data points and a candidate line
- Comparing different slopes and intercepts
- Verifying calculations manually
- Understanding the role and limitations of NumPy

### 9. Common Failure Modes
- Assuming every dataset has a linear relationship
- Confusing actual and predicted values
- Misinterpreting slope and intercept
- Using incorrect feature or target shapes
- Making arithmetic errors in predictions
- Judging model quality only by its visual appearance
- Ignoring influential observations
- Assuming low training error guarantees good generalization
- Confusing correlation with causation
- Ignoring model assumptions and limitations

### 10. Importance for an ML Engineer
- Linear regression as a foundational supervised learning model
- Understanding features, coefficients, and predictions
- Building intuition for model parameters
- Understanding prediction errors
- Preparing for MSE and residuals
- Building foundations for gradient-based optimization
- Learning simple models before more complex algorithms
- Using interpretable models as baselines

## Practical Implementation

- Selected a small dataset or controlled example.
- Represented input features and target values using NumPy.
- Calculated predictions using a chosen slope and intercept.
- Plotted observed data points and a candidate line.
- Compared predictions with observed values.

## Experiment Record

- **Assumption:** The relationship being modeled can be reasonably approximated by a straight line.
- **Result:** Record the actual output or metric from the experiment.
- **Limitation:** A linear model may not capture nonlinear relationships or all patterns in the data.
- **Debugging observation:** Record an issue actually encountered and how it was checked or resolved.

## Key Takeaways

- Linear regression predicts a numerical target using a linear relationship between features and the prediction.
- The slope determines the line's direction and steepness, while the intercept determines where it crosses the vertical axis.
- Multiple features can contribute to a prediction through their coefficients.
- Residuals represent the differences between observed and predicted values.
- Least squares provides a way to choose a line by minimizing squared errors.
- Model assumptions, data quality, and unseen-data performance matter when evaluating a model.
- Understanding linear regression builds a foundation for more advanced machine learning algorithms.


