# Learning Progress Dashboard

> Updated: 2026-11-09  
> Tracking rule: a topic is not marked mastered just because it was explained. Mastery requires an independent explanation, a derivation or implementation, and a fresh problem without step-by-step help.

## Current position

**Active pace:** Aggressive — target 30–36 focused hours per week, with a lighter/recovery day. Follow the [12-month accelerated roadmap](../curriculum/roadmap-12-month-accelerated.md). The original 24-month curriculum remains a slower reference path.

| Field | Current status |
|---|---|
| Learning track | Mathematical foundations → machine learning foundations |
| Current module | 12-month accelerated Intelligence Lab roadmap — Month 1 foundations sprint |
| Current lesson | Session 03 — independent eigenvalue/eigenvector work, PCA, and classification evaluation |
| Overall status | Accelerated plan active; foundational assessment and independent verification in progress |
| Next checkpoint | Compare Random Forest with Logistic Regression plus engineered interaction features using validation-based model selection; continue PCA implementation and independent metric calculations |

## Topic tracker

| Topic | Status | Evidence so far | Next action |
|---|---|---|---|
| Derivatives | Practised with guidance | Differentiated (x^2); evaluated derivatives at given values | Solve a fresh set independently |
| Gradients | Practised with guidance | Interpreted positive and negative gradients; connected sign to direction of change | Explain gradient geometrically and solve fresh examples |
| Gradient descent | Practised with guidance and independent numerical updates | Correctly updated parameters in fresh scalar and two-variable problems using a learning rate | Implement a simple optimiser from scratch |
| Partial derivatives | Practised with guidance | Calculated partial derivatives for (3x^2+2y^2) | Practise with a new multivariable function |
| Chain rule | Practised independently (several checkpoints) | Correctly solved fresh chain-rule derivative chains; one forward-loss arithmetic error occurred | Continue with unfamiliar composite functions and improve forward-pass checking |
| Computational graphs | Introduced and practised | Traced dependency chains in two examples | Draw a graph for a small neural-network layer |
| Backpropagation | Introduced; understanding developing | Multiplied local derivatives backwards to obtain parameter gradients | Explain and calculate a fresh example independently |
| Linear algebra: vectors and matrices | Practised with guidance | Correctly answered 10 guided questions covering vector operations, dot products, dimensions, matrix multiplication, matrix-vector products, and basic geometric meaning | Complete an independent mixed problem set |
| Eigenvalues and eigenvectors | Practised independently (one complete 2×2 problem) | Independently found eigenvalues 5 and 2, eigenvectors [1,1] and [1,-2], and verified Av = λv for A=[[4,1],[2,3]] | Solve additional matrices and test geometric interpretation |
| Probability and statistics | Practised with guidance | Correctly answered 10 guided questions on probability, independence, conditional probability, expectation, variance, standard deviation, Bayes' rule, correlation, samples, and MSE | Practise distributions, confidence intervals, hypothesis testing, and MLE |
| Core machine learning | Practised with guidance | 10/11 guided questions correct; covered supervised learning, classification/regression, data splits, overfitting, underfitting, regularisation, bias–variance, leakage, precision/recall, and cross-validation | Complete independent scenario-based questions and implement a small evaluation workflow |
| Overfitting diagnosis and remedies | Practised independently (one checkpoint) | Correctly diagnosed a 98% train / 72% test accuracy gap as overfitting; explained fitting noise and named L2, early stopping, and L1/feature selection as remedies | Apply remedies and compare validation results in an experiment |
| Numerical gradient checking | Not started | — | Implement finite-difference checks |
| Jacobians and Hessians | Not started | — | Study after multivariable chain rule |
| PCA and dimensionality reduction | Introduced and practised with guidance | Explained eigenvalues as explained variance, eigenvectors as component directions, information loss, and why low-variance components may still predict a target | Implement PCA, inspect loadings, and compare downstream model performance |
| Classification metrics and thresholds | Practised with guidance | Interpreted baseline/SMOTE/class-weighted confusion matrices; correctly predicted that raising the threshold generally reduces FP and recall while increasing FN; interpreted validation and test threshold results | Independently calculate precision, recall, specificity, and F1 from a fresh confusion matrix; explain why test data must not be used for tuning |
| Model evaluation implementation | Practised with guidance | Built and interpreted baseline, SMOTE, class-weighted, and threshold-tuned evaluations; read confusion matrices and compared precision/recall/F1 | Independently calculate metrics from a fresh confusion matrix and build a second model comparison |

## Current practical experiment — fraud classification (2026-11-09)

The [fraud-classification experiment](../experiments/fraud-classification/README.md) now contains the notebook, result record, and next-step hypothesis.

| Approach | Test recall | Test precision | False positives | Fraud alerts |
|---|---:|---:|---:|---:|
| Baseline Logistic Regression | 4.76% | 100.00% | 0 | 1 |
| SMOTE + Logistic Regression | 85.71% | 3.61% | 481 | 499 |
| Class-weighted Logistic Regression (0.50) | 90.48% | 3.73% | 491 | 510 |
| Class-weighted, validation-selected threshold 0.80 | 28.57% | 5.61% | 101 | 107 |

**Conclusion:** No tested threshold met both the exercise constraints (recall >= 90% and <= 100 alerts on the 2,000-row test set). The test set was kept separate from threshold selection. The next experiment is Random Forest versus Logistic Regression with explicit interaction features.

## Assessment snapshot — 2026-11-09

| Area | Guided result | Interpretation |
|---|---:|---|
| Linear algebra | 10/10 | Strong initial guided performance; independent transfer not yet tested |
| Probability and statistics | 10/10 | Strong initial guided performance; advanced statistical topics remain untested |
| Core machine learning | 10/11 | Good guided understanding; one bias–variance question was initially missed |
| Calculus and optimisation | Fresh independent problems mostly correct | Correct derivative chains, gradient updates, and partial derivatives across several problems; one forward-pass arithmetic error and an initial gradient-direction misconception were corrected |

These are learning checks, not formal exam scores or proof of mastery.

## Learning observations

- Correctly distinguished high bias from high variance after feedback.
- Correctly explained why a large training–testing performance gap indicates overfitting.
- Suggested three valid overfitting remedies: L2 regularisation, early stopping, and L1 regularisation / feature selection.
- Demonstrated good guided accuracy in linear algebra and probability/statistics.
- Independent problem-solving and implementation evidence is still limited. Keep topic statuses conservative.

## Next session

1. Implement and compare Random Forest against Logistic Regression with explicit interaction features.
2. Keep model/threshold selection on validation data and preserve the held-out test set.
3. Calculate confusion-matrix metrics independently from a fresh example.
4. Implement PCA, inspect loadings, and test downstream usefulness.
5. Continue fresh independent mathematics and statistics checkpoints.

## Progress history

| Date | Session | Result |
|---|---|---|
| 2026-11-03 | Session 01 — calculus, optimisation, and backpropagation foundations | Guided practice completed; independent checkpoint pending |
| 2026-11-04 | Session 02 — baseline knowledge assessment | Linear algebra 10/10 and probability/statistics 10/10 guided; core ML 10/11 guided; one independent overfitting checkpoint completed |
| 2026-11-09 | Session 03 — independent linear algebra, PCA, and classification metrics | One complete eigenvalue/eigenvector problem solved independently; several calculus checkpoints completed; PCA and classification evaluation concepts practised with guidance |
| 2026-11-09 | Session 04 — imbalanced fraud classification and threshold trade-offs | Compared baseline, SMOTE, class weighting, and validation-based threshold tuning; correctly reasoned about nonlinear boundaries and feature interactions; all practical interpretation remains guided evidence |

## Evidence policy

Use these status labels consistently:
- **Not started** — no meaningful study yet.
- **Introduced** — concept explained, but little practice.
- **Practised with guidance** — solved examples with prompts or hints.
- **Practised independently** — solved fresh problems without step-by-step help.
- **Mastered** — can explain, derive, apply, and transfer the concept to a new setting.
