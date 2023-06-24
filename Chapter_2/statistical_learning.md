# Unit 2: Statistical Learning
## What is Statistical Learning?
### Notation

- Assume
  - $Y$ is a response variable.
  - $X=(X_1, \cdots, X_p)$ is a vector of predictors

- Consider the following model:

  $$Y = f(X) + \epsilon, $$

- where:
  - $\epsilon$ captures measurement errors and other discrepancies.
  - $f$ is an unknown function to be determined from data.

- With a good $f$ we can make predictions of $Y$ at new points $X = x$.
- Depending on the complexity of $f$, we may be able to understand how each component $X_j$ of $X$ affects $Y$.
- Is there an ideal $f(X)$?
  - An ideal $f(x) = E(Y |X = x)$ in the case of a single predictor is called the **regression function**.
  - For a vector of predictors, an ideal $f(x) = f(x_1, \cdots, x_p) = E(Y |X_1 = x_1, \cdots, X_p = x_p)$.

    


