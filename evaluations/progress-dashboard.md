# Learning Progress Dashboard

> Updated: 2026-11-04  
> Tracking rule: a topic is not marked mastered just because it was explained. Mastery requires an independent explanation, a derivation or implementation, and a fresh problem without step-by-step help.

## Current position

| Field | Current status |
|---|---|
| Learning track | Mathematical foundations → machine learning foundations |
| Current module | Baseline knowledge assessment |
| Current lesson | Session 02 — calculus, linear algebra, probability, statistics, and core ML |
| Overall status | Guided baseline completed; independent verification still in progress |
| Next checkpoint | Independent problem set across all four areas, beginning with calculus and linear algebra |

## Topic tracker

| Topic | Status | Evidence so far | Next action |
|---|---|---|---|
| Derivatives | Practised with guidance | Differentiated (x^2); evaluated derivatives at given values | Solve a fresh set independently |
| Gradients | Practised with guidance | Interpreted positive and negative gradients; connected sign to direction of change | Explain gradient geometrically and solve fresh examples |
| Gradient descent | Practised with guidance | Updated scalar and two-variable weights using a learning rate | Implement a simple optimiser from scratch |
| Partial derivatives | Practised with guidance | Calculated partial derivatives for (3x^2+2y^2) | Practise with a new multivariable function |
| Chain rule | Practised with guidance | Applied local derivatives across multi-step expressions | Derive a new composite function independently |
| Computational graphs | Introduced and practised | Traced dependency chains in two examples | Draw a graph for a small neural-network layer |
| Backpropagation | Introduced; understanding developing | Multiplied local derivatives backwards to obtain parameter gradients | Explain and calculate a fresh example independently |
| Linear algebra: vectors and matrices | Practised with guidance | Correctly answered 10 guided questions covering vector operations, dot products, dimensions, matrix multiplication, matrix-vector products, and basic geometric meaning | Complete an independent mixed problem set |
| Eigenvectors and transformations | Introduced and practised | Correctly identified that an eigenvector retains its direction under a transformation (while its magnitude may change) | Calculate eigenvalues and eigenvectors |
| Probability and statistics | Practised with guidance | Correctly answered 10 guided questions on probability, independence, conditional probability, expectation, variance, standard deviation, Bayes' rule, correlation, samples, and MSE | Practise distributions, confidence intervals, hypothesis testing, and MLE |
| Core machine learning | Practised with guidance | 10/11 guided questions correct; covered supervised learning, classification/regression, data splits, overfitting, underfitting, regularisation, bias–variance, leakage, precision/recall, and cross-validation | Complete independent scenario-based questions and implement a small evaluation workflow |
| Overfitting diagnosis and remedies | Practised independently (one checkpoint) | Correctly diagnosed a 98% train / 72% test accuracy gap as overfitting; explained fitting noise and named L2, early stopping, and L1/feature selection as remedies | Apply remedies and compare validation results in an experiment |
| Numerical gradient checking | Not started | — | Implement finite-difference checks |
| Jacobians and Hessians | Not started | — | Study after multivariable chain rule |
| Model evaluation implementation | Not started | — | Build a small classification evaluation notebook |

## Assessment snapshot — 2026-11-04

| Area | Guided result | Interpretation |
|---|---:|---|
| Linear algebra | 10/10 | Strong initial guided performance; independent transfer not yet tested |
| Probability and statistics | 10/10 | Strong initial guided performance; advanced statistical topics remain untested |
| Core machine learning | 10/11 | Good guided understanding; one bias–variance question was initially missed |
| Calculus and optimisation | Guided examples completed | Independent chain-rule and gradient checkpoint still required |

These are learning checks, not formal exam scores or proof of mastery.

## Learning observations

- Correctly distinguished high bias from high variance after feedback.
- Correctly explained why a large training–testing performance gap indicates overfitting.
- Suggested three valid overfitting remedies: L2 regularisation, early stopping, and L1 regularisation / feature selection.
- Demonstrated good guided accuracy in linear algebra and probability/statistics.
- Independent problem-solving and implementation evidence is still limited. Keep topic statuses conservative.

## Next session

1. Run a short independent calculus and chain-rule checkpoint.
2. Test linear algebra with fresh matrix and vector problems.
3. Add probability distributions and basic statistical inference.
4. Apply core ML concepts to a small end-to-end evaluation example.
5. Update statuses only when independent evidence supports the change.

## Progress history

| Date | Session | Result |
|---|---|---|
| 2026-11-03 | Session 01 — calculus, optimisation, and backpropagation foundations | Guided practice completed; independent checkpoint pending |
| 2026-11-04 | Session 02 — baseline knowledge assessment | Linear algebra 10/10 and probability/statistics 10/10 guided; core ML 10/11 guided; one independent overfitting checkpoint completed |

## Evidence policy

Use these status labels consistently:
- **Not started** — no meaningful study yet.
- **Introduced** — concept explained, but little practice.
- **Practised with guidance** — solved examples with prompts or hints.
- **Practised independently** — solved fresh problems without step-by-step help.
- **Mastered** — can explain, derive, apply, and transfer the concept to a new setting.
