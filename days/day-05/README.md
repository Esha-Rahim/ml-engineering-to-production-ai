#Day 5 --- Dot Product and Matrix Multiplication

## Date

October 12, 2026

## Official roadmap topic

**Dot product and matrix multiplication**

## 1. Dot Product

The **dot product** of two vectors of the same length is the sum of the
products of their corresponding elements. Its result is a single number
(a scalar).

For vectors (`\mathbf{a}`{=tex}=\[a_1,`\ldots`{=tex},a_n\]) and
(`\mathbf{b}`{=tex}=\[b_1,`\ldots`{=tex},b_n\]):

\[
`\mathbf{a}`{=tex}`\cdot`{=tex}`\mathbf{b}`{=tex}=`\sum`{=tex}\_{i=1}\^{n}a_i
b_i \]

**Example**

\[
\[2,3,4\]`\cdot[5,6,7]`{=tex}=(2`\times5`{=tex})+(3`\times6`{=tex})+(4`\times7`{=tex})=56
\]

The vectors must have the same number of elements.

### NumPy implementation

``` python
import numpy as np

a = np.array([2, 3, 4])
b = np.array([5, 6, 7])

print(np.dot(a, b))  # 56
print(a @ b)         # 56
```

For one-dimensional vectors of equal length, `np.dot(a, b)` and `a @ b`
both calculate the dot product.

## 2. Matrix Multiplication

**Matrix multiplication** combines each row of the first matrix with
each column of the second matrix. Each output element is a dot product
of one row and one column.

### Shape compatibility

If the first matrix has shape `(m, n)` and the second has shape
`(n, p)`, multiplication is valid and the output shape is `(m, p)`:

\[ (m`\times `{=tex}n)(n`\times `{=tex}p)=(m`\times `{=tex}p) \]

The inner dimensions must match.

**Example**

\[ A=
```{=tex}
\begin{bmatrix}1&2\\3&4\end{bmatrix}
```
,`\quad`{=tex} B=
```{=tex}
\begin{bmatrix}5&6\\7&8\end{bmatrix}
```
\]

\[ AB=
```{=tex}
\begin{bmatrix}
1(5)+2(7)&1(6)+2(8)\\
3(5)+4(7)&3(6)+4(8)
\end{bmatrix}
```
=
```{=tex}
\begin{bmatrix}19&22\\43&50\end{bmatrix}
```
\]

Matrix multiplication is generally not commutative: `A @ B` does not
generally equal `B @ A`.

### NumPy implementation

``` python
import numpy as np

A = np.array([[1, 2],
              [3, 4]])

B = np.array([[5, 6],
              [7, 8]])

result = A @ B

print(result)
# [[19 22]
#  [43 50]]

print(result.shape)  # (2, 2)
```

`np.matmul(A, B)` is another option for matrix multiplication.

## 3. Element-wise Multiplication vs. Matrix Multiplication

For NumPy arrays:

-   `A * B` multiplies matching elements position by position.
-   `A @ B` performs matrix multiplication using row-by-column dot
    products.

These are different operations and generally give different results.

## 4. Relationship Between Dot Product and Matrix Multiplication

-   A dot product of two one-dimensional vectors returns a scalar.
-   Matrix multiplication uses dot products between rows of the first
    matrix and columns of the second.
-   A row vector of shape `(1, n)` multiplied by a column vector of
    shape `(n, 1)` produces a `(1, 1)` matrix containing the dot-product
    value.

## 5. Why These Operations Matter in Machine Learning

### Weighted sums

A model may calculate a score using feature values (x_i) and weights
(w_i):

\[ `\hat{y}`{=tex}=`\sum`{=tex}\_{i=1}\^{n}x_iw_i+b \]

The sum is a dot product; the bias (b) is added afterward.

### Multiple samples and neural networks

If rows of a feature matrix `X` represent samples and columns represent
features, multiplying `X` by a compatible weight vector calculates a
weighted score for each sample. Neural-network layers also use matrix
multiplication to combine inputs with learned weights. Understanding
shapes helps prevent bugs.

## 6. Assumptions and Implementation Choices

-   Dot-product vectors must have equal lengths.
-   Matrix multiplication requires the first matrix's column count to
    equal the second matrix's row count.
-   Inspect array shapes before multiplying.
-   Use `np.dot()` or `@` for vector dot products.
-   Use `@` or `np.matmul()` for matrix multiplication.
-   Do not use `*` when you intend matrix multiplication.
-   Verify a small result manually before trusting the implementation.

## 7. Common Errors and Failure Modes

1.  **Incompatible dimensions:** the inner dimensions do not match.
2.  **Confusing `*` and `@`:** element-wise multiplication is not matrix
    multiplication.
3.  **Misreading shapes:** `(3, 2)` means three rows and two columns.
4.  **Using the wrong order:** `A @ B` and `B @ A` are not generally
    equivalent.
5.  **Expecting the wrong output shape:** `(m, n) @ (n, p)` returns
    `(m, p)`.
6.  **Skipping verification:** a small manual calculation can reveal
    incorrect assumptions or code.

## 8. Controlled NumPy Experiment

Run the code and check that the results match the expected values.

``` python
import numpy as np

# Dot product
a = np.array([2, 3, 4])
b = np.array([5, 6, 7])
dot_result = a @ b
assert dot_result == 56

# Matrix multiplication
A = np.array([[1, 2],
              [3, 4]])
B = np.array([[5, 6],
              [7, 8]])

matrix_result = A @ B
expected = np.array([[19, 22],
                     [43, 50]])

assert np.array_equal(matrix_result, expected)
assert matrix_result.shape == (2, 2)

print("Dot product:", dot_result)
print("Matrix multiplication:\\n", matrix_result)
print("Output shape:", matrix_result.shape)
```

### Experiment record --- complete after running

-   **Assumption:** The vectors have equal length and the matrices have
    compatible shapes.
-   **Result:** Record the actual output and whether the assertions
    passed.
-   **Limitation:** These small examples do not measure performance on
    large arrays.
-   **Debugging observation:** Record a shape check or error you
    actually investigated. If none occurred, write "None encountered."

## 9. Key Takeaways

-   The dot product multiplies corresponding vector elements and sums
    the products.
-   Matrix multiplication computes output elements using row-by-column
    dot products.
-   `(m, n) @ (n, p)` produces an output with shape `(m, p)`.
-   NumPy `*` is element-wise multiplication; `@` is matrix
    multiplication.
-   These operations underpin weighted sums, linear models, and
    neural-network layers.
-   Shape checks and small manual calculations are useful debugging
    habits.

## 10. Closed-Book Self-Check

-   [ ] Define a dot product and explain why its result is one number.
-   [ ] Calculate `[1, 2, 3] · [4, 5, 6]`.
-   [ ] When can two matrices be multiplied?
-   [ ] What is the output shape of `(4, 3) @ (3, 2)`?
-   [ ] Explain the difference between `A * B` and `A @ B`.
-   [ ] Why are dot products useful for model predictions?
-   [ ] Name one common shape-related failure mode.
-   [ ] Record anything you still cannot explain clearly.

## 11. Day 5 Roadmap Deliverables

-   [ ] Complete the learning and run the NumPy experiment.
-   [ ] Add this learning log and implementation to the relevant
    repository.
-   [ ] Write a short reflection based on what you actually learned.
-   [ ] Set branch and commit conventions.
-   [ ] Enable a simple repository hygiene checklist.
-   [ ] Draft a concise LinkedIn About section focused on software
    engineering and ML learning in progress.
-   [ ] Complete the closed-book self-check.

**Suggested commit message**

``` text
Add Day 5 dot product and matrix multiplication notes
```

## Resources Specified by the Roadmap

-   [3Blue1Brown --- Essence of Linear
    Algebra](https://www.youtube.com/playlist?list=PLZHQObOWTQDPD3MizzM2xVFitgF8hE_ab)
-   [NumPy --- Absolute
    Beginners](https://numpy.org/doc/stable/user/absolute_beginners/)
-   [NumPy ---
    Quickstart](https://numpy.org/doc/stable/user/quickstart.html)
-   [CampusX --- 100 Days of Machine
    Learning](https://learnwith.campusx.in/s/preview/courses/100-Days-of-Machine-Learning-YouTube-1763210027804-6918732bee601b12112865e6)

**Note:** The official roadmap title is *Dot product and matrix
multiplication*. These notes expand that topic for study; they are not a
verbatim numbered subtopic list from the roadmap PDF.
