# Day 8 — Linear Regression from Scratch: Math to Code Verification

## Date
October 15, 2026

## Topics Covered

### 1. Linear Regression Foundations
- Linear regression and its purpose
- Simple vs. multiple linear regression
- Features, targets, weights, and bias
- Prediction equation
- Actual values vs. predicted values

### 2. Mathematical Formulation
- Feature vectors and feature matrices
- Target and parameter vectors
- Scalar and vectorized prediction equations
- Matrix-vector multiplication
- Expected matrix and tensor shapes

### 3. Loss Function and Objective
- Prediction errors and residuals
- Squared errors and SSE
- Mean Squared Error (MSE)
- Mathematical formulation of MSE
- Objective of minimizing prediction error
- Prediction vs. model fitting

### 4. Derivation Before Coding
- Deriving the prediction equation
- Deriving residual and MSE calculations
- Translating mathematical expressions into computational steps
- Identifying input and output shapes
- Checking mathematical consistency

### 5. NumPy Implementation
- Creating a small dataset
- Defining features, targets, weights, and bias
- Vectorized predictions
- Matrix multiplication
- Residual and MSE calculations
- Avoiding high-level ML shortcuts
- Manual calculation and numerical verification

### 6. Shape Verification
- Feature matrix and weight vector shapes
- Prediction and target vector shapes
- Matrix multiplication compatibility
- Residual and loss calculation shapes
- Broadcasting and dimension errors
- Verifying shapes at each step

### 7. PyTorch and Autograd
- PyTorch tensors and NumPy conversion
- Reproducing predictions and MSE
- Automatic differentiation
- Gradient tracking and gradient calculation
- Interpreting gradients
- Comparing NumPy and PyTorch results

### 8. Automated Numerical Testing
- Writing tests with `pytest`
- Testing predictions, residuals, and MSE
- Comparing NumPy and PyTorch outputs
- Using `numpy.allclose`
- Numerical tolerances and floating-point precision
- Detecting incorrect implementations

### 9. Gradient Verification
- Numerical gradients
- Finite-difference checks
- Comparing numerical gradients with autograd
- Step size and tolerance selection
- Investigating gradient-check failures

### 10. ML Interpretation and Failure Modes
- Interpreting predictions, parameters, and MSE
- Mathematical correctness vs. model quality
- Shape and broadcasting errors
- Incorrect loss calculations
- NumPy and PyTorch mismatches
- Inappropriate tolerances
- Floating-point precision limitations
- Importance of math-to-code verification

## Practical Implementation

- [ ] Complete the mathematical derivation.
- [ ] Document expected matrix and tensor shapes.
- [ ] Implement linear regression calculations using vectorized NumPy.
- [ ] Reproduce the calculations using PyTorch/autograd.
- [ ] Verify numerical agreement between implementations.
- [ ] Add automated tests using `pytest`.
- [ ] Add `allclose` or finite-difference checks with an explained tolerance.
- [ ] Record the ML interpretation and a limitation or failure mode.

## Verification Record

- **NumPy result:** Record the actual prediction and MSE results.
- **PyTorch result:** Record the corresponding results.
- **Numerical agreement:** Record the comparison outcome and tolerance.
- **Automated tests:** Record the actual test results.
- **Gradient verification:** Record the result if performed.
- **Failure mode or limitation:** Record one observed or investigated issue.

## Key Takeaways

- Mathematical derivations should guide implementation.
- Expected shapes should be defined before coding.
- Vectorized NumPy operations provide a transparent implementation.
- PyTorch/autograd provides an independent computational comparison.
- Automated tests help detect mathematical and numerical errors.
- Passing numerical tests verifies specific calculations, not overall model quality.

## Self-Check

- [ ] Explain the prediction equation without notes.
- [ ] Derive the MSE calculation.
- [ ] State the expected shape of every major array or tensor.
- [ ] Explain the NumPy implementation.
- [ ] Explain how PyTorch/autograd was used for verification.
- [ ] Explain the selected numerical tolerance.
- [ ] Identify one failure mode or trade-off.
- [ ] Record anything that remains unclear.

## Resources

- [3Blue1Brown — Essence of Linear Algebra](https://www.youtube.com/playlist?list=PLZHQObOWTQDPD3MizzM2xVFitgF8hE_ab)
- [NumPy — Absolute Beginners](https://numpy.org/doc/stable/user/absolute_beginners/)
- [NumPy — Quickstart](https://numpy.org/doc/stable/user/quickstart.html)
- [CampusX — 100 Days of Machine Learning](https://learnwith.campusx.in/s/preview/courses/100-Days-of-Machine-Learning-YouTube-1763210027804-6918732bee601b12112865e6)

## GitHub Deliverable

- [ ] Add the derivation, implementation, tests, and verification results.
- [ ] Update the README or experiment log where necessary.
- [ ] Commit the completed work with a descriptive message.

**Suggested commit message:**

`Add Day 8 linear regression math-to-code verification`

## Profile Evidence

No public LinkedIn post required today. Save one genuine evidence item, such as a numerical comparison, test result, derivation, diagram, or debugging lesson, for future profile updates.
