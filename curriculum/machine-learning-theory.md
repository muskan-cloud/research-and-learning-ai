# Machine Learning Theory

## Learning objective

Understand the principles that connect data, model capacity, optimisation, and generalisation.

## Core sequence

1. **Learning setup:** datasets, features, labels, hypotheses, objectives, and assumptions.
2. **Linear models:** linear regression, logistic regression, least squares, likelihood.
3. **Risk:** empirical risk, expected risk, loss functions, and distribution shift.
4. **Generalisation:** train-test gap, overfitting, underfitting, regularisation.
5. **Model capacity:** parameter count, VC dimension intuition, sample complexity.
6. **Optimisation:** batch and stochastic gradient descent, momentum, adaptive methods.
7. **Evaluation:** data leakage, cross-validation, calibration, uncertainty, and metrics.
8. **Robustness:** distribution shift, spurious correlations, and out-of-distribution evaluation.

## Suggested experiments

- Compare polynomial models of increasing degree.
- Plot training and validation error under different regularisation strengths.
- Compare full-batch and stochastic gradient descent.
- Test the effect of dataset size on generalisation.
- Create a controlled distribution shift and measure performance degradation.

## Required research habits

- State the data-generating assumptions.
- Separate optimisation failure from generalisation failure.
- Use appropriate baselines.
- Report uncertainty and repeated-run variation where practical.
- Avoid causal claims from purely correlational evidence.

## Exit criteria

Explain empirical versus expected risk, diagnose overfitting, implement baseline algorithms, and design a leakage-resistant evaluation.
