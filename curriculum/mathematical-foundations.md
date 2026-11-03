# Mathematical Foundations

## Learning objective

Develop enough mathematical fluency to read machine-learning research, understand derivations, and implement algorithms without treating equations as black boxes.

## 1. Linear algebra

### Topics
- Scalars, vectors, matrices, tensors, and notation.
- Vector spaces, span, basis, dimension, and rank.
- Matrix multiplication as composition of linear maps.
- Linear transformations, projections, and orthogonality.
- Norms, inner products, and distances.
- Eigenvalues and eigenvectors.
- Singular value decomposition and low-rank approximation.

### Practical work
- Implement vector and matrix operations with NumPy.
- Visualise 2D linear transformations.
- Demonstrate projection and least-squares solutions.
- Explore PCA on a small dataset.

### Mastery questions
- What does a matrix do to a vector geometrically?
- Why does rank matter?
- When is a matrix invertible?
- What do eigenvectors reveal about a transformation?
- Why is SVD useful for compression and representation?

## 2. Calculus

### Topics
- Functions, limits, and continuity.
- Derivatives and the chain rule.
- Partial derivatives and gradients.
- Jacobians and Hessians.
- Multivariable chain rule.
- Taylor approximations.
- Computational graphs.

### Practical work
- Derive gradients for scalar functions.
- Implement numerical finite-difference gradient checks.
- Compare analytical and numerical gradients.
- Visualise gradients on simple loss surfaces.

### Mastery questions
- What does a gradient represent?
- Why does the chain rule enable backpropagation?
- What information does a Hessian contain?
- When can numerical gradients be misleading?

## 3. Probability and statistics

### Topics
- Sample spaces, events, and conditional probability.
- Random variables and common distributions.
- Expectation, variance, covariance, and correlation.
- Bayes' theorem.
- Joint, marginal, and conditional distributions.
- Maximum likelihood estimation.
- Sampling, confidence intervals, and hypothesis testing.
- Bayesian reasoning and uncertainty.

### Practical work
- Simulate distributions and sampling.
- Verify the law of large numbers empirically.
- Fit a simple probability model.
- Compare likelihood-based parameter estimates.

### Mastery questions
- What is the difference between probability and likelihood?
- How does conditioning change a distribution?
- What does variance measure?
- What assumptions underlie a confidence interval?

## 4. Optimisation

### Topics
- Objective and loss functions.
- Gradient descent and stochastic gradient descent.
- Learning rates and convergence intuition.
- Momentum and adaptive optimisers.
- Convexity and local minima.
- Constraints and regularisation.

### Practical work
- Implement gradient descent from scratch.
- Compare learning rates.
- Plot optimisation trajectories.
- Investigate ill-conditioned objectives.

## 5. Information theory

### Topics
- Entropy and cross-entropy.
- KL divergence.
- Mutual information.
- Conditional entropy.
- Coding intuition and information bottlenecks.

### Practical work
- Calculate entropy for discrete distributions.
- Compare cross-entropy and KL divergence.
- Explore how information measures change with model predictions.

## Completion standard

For each major topic, save:
1. A concise explanation in your own words.
2. At least one derivation.
3. A worked problem or implementation.
4. A note on common misconceptions.
5. One open question connecting the mathematics to learning systems.
