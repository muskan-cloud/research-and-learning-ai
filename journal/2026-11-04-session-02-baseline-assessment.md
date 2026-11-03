# Session 02 — Baseline Knowledge Assessment

**Date:** 2026-11-04  
**Track:** Mathematical foundations and machine learning foundations  
**Format:** Guided assessment with one independent applied checkpoint

## Areas assessed

- Calculus and optimisation: derivatives, gradients, gradient descent, partial derivatives, chain rule, computational graphs, and backpropagation.
- Linear algebra: vector operations, dot products, matrix dimensions and multiplication, matrix-vector products, transformations, and the eigenvector concept.
- Probability and statistics: basic probability, independence, conditional probability, expectation, variance, standard deviation, Bayes' rule, correlation, sampling, and mean squared error.
- Core machine learning: supervised learning, classification and regression, data splits, overfitting and underfitting, L1/L2 regularisation, bias–variance, data leakage, precision/recall, and cross-validation.

## Guided assessment results

| Area | Result | Notes |
|---|---:|---|
| Linear algebra | 10/10 | Correct responses across the guided questions |
| Probability and statistics | 10/10 | Correct responses across the guided questions |
| Core machine learning | 10/11 | One initial error: high bias vs high variance; corrected after explanation |
| Calculus and optimisation | Guided examples completed | Fresh independent chain-rule checkpoint remains outstanding |

These results describe guided question accuracy. They are not formal examination scores and do not establish independent mastery.

## Independent applied checkpoint

Scenario: training accuracy 98%, testing accuracy 72%.

The learner:
- Identified overfitting.
- Explained that the model had learned training patterns too closely, including noise.
- Suggested L2 regularisation.
- Further suggested early stopping and L1 regularisation / feature selection.

This is good evidence of transferring the overfitting concept to a practical scenario. More independent problems are needed before marking broader ML topics as independently practised.

## Strengths observed

- Strong guided performance in vector/matrix operations and introductory probability/statistics.
- Correct understanding of data leakage, recall in a high-cost false-negative scenario, and K-fold cross-validation.
- Correctly distinguished L1 (can drive weights to zero) from L2 (shrinks weights).
- Corrected the bias–variance distinction after feedback.

## Gaps and next steps

1. Independently solve a new chain-rule and gradient-descent problem.
2. Calculate eigenvalues/eigenvectors rather than only identifying their meaning.
3. Study probability distributions, confidence intervals, hypothesis testing, and maximum likelihood estimation.
4. Practise bias–variance diagnosis with multiple scenarios.
5. Implement a small classification evaluation workflow, including precision, recall, F1, and cross-validation.

## Assessment principle

Keep progress labels conservative. Guided correctness is useful evidence, but independent explanation, calculation, implementation, and transfer to unfamiliar problems are required for stronger mastery claims.
