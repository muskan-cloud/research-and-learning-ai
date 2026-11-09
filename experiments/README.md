# Experiments

This directory contains reproducible practical experiments, their notebooks, configurations, and result notes.

## Experiments

- [Fraud classification](fraud-classification/README.md) — class imbalance, scaling, SMOTE, class weighting, threshold tuning, and planned model comparisons.

## Experiment record standard

Every experiment should be understandable and reproducible by someone who did not run it.

- **Question / hypothesis**
- **Motivation and related work**
- **Model and architecture**
- **Dataset and provenance**
- **Preprocessing**
- **Baselines**
- **Variables and controls**
- **Metrics**
- **Compute and environment**
- **Random seeds**
- **Procedure**
- **Results**
- **Ablations**
- **Negative results**
- **Interpretation**
- **Alternative explanations**
- **Limitations**
- **Next experiment**

## Standards

- Keep training, validation, and test data separate.
- Record configurations and dependency versions.
- Fix and report random seeds where possible.
- Compare against meaningful baselines.
- Do not omit failed runs that affect interpretation.
- Distinguish exploratory analysis from confirmatory tests.
- Never claim causation without a design that supports it.
