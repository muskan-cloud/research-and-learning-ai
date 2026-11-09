# Fraud Classification Experiment

**Date started:** 2026-11-09  
**Status:** In progress — baseline, SMOTE, class weighting, and validation-based threshold tuning completed; Random Forest is the next planned comparison.

## Research question

Can we detect rare fraudulent transactions while satisfying both operational constraints?

- Recall >= 90%.
- No more than 100 fraud alerts on the 2,000-row held-out test set.

## Notebook

- [Fraud classification pipeline](fraud-classification-pipeline.ipynb)
- [Open in Google Colab](https://colab.research.google.com/github/muskan-cloud/research-and-learning-ai/blob/main/experiments/fraud-classification/fraud-classification-pipeline.ipynb)

## Dataset and setup

- Synthetic dataset generated with scikit-learn `make_classification`.
- 10,000 rows and 8 input features.
- Class counts: 9,895 legitimate and 105 fraud.
- Stratified 80/20 train-test split.
- Training set: 8,000 rows (7,916 legitimate; 84 fraud).
- Test set: 2,000 rows (1,979 legitimate; 21 fraud).
- Random seed: 42.

This is simulated data for learning the workflow, not evidence of real-world banking performance.

## Experiments completed

| Model / method | Test recall | Test precision | False positives | Test fraud alerts |
|---|---:|---:|---:|---:|
| Baseline Logistic Regression | 4.76% | 100.00% | 0 | 1 |
| SMOTE + Logistic Regression | 85.71% | 3.61% | 481 | 499 |
| Class-weighted Logistic Regression (default 0.50) | 90.48% | 3.73% | 491 | 510 |
| Class-weighted model (threshold selected on validation: 0.80) | 28.57% | 5.61% | 101 | 107 |

**Metric note:** The class-weighted default result is from the user's executed notebook output: confusion matrix [[1488, 491], [2, 19]], so total predicted fraud alerts = 491 + 19 = 510. The threshold-tuned test result is from the user's executed output: [[1878, 101], [15, 6]], so total alerts = 107.

## Threshold tuning protocol

- A validation split was created from the original training data.
- The weighted pipeline was trained on the fit subset only.
- Thresholds from 0.05 to 0.95 were compared on validation predictions.
- Threshold 0.80 was selected as a best-effort threshold because no tested validation threshold met both operational constraints.
- It met the validation alert limit (89 alerts) but recall was only 29.41%.
- On the untouched test set, it produced 107 alerts and 28.57% recall.
- The test result is a final evaluation; do not tune the threshold again using this test set.

## Interpretation so far

- The baseline mostly predicts the majority class and misses nearly all fraud.
- SMOTE and class weighting substantially improve recall but create many false positives.
- Raising the threshold reduces alerts but also sharply reduces recall.
- No tested threshold meets both constraints.
- Threshold adjustment alone has not solved the problem. Better separation/ranking, features, or model structure may be needed.

## Next experiment

Compare:
1. Random Forest, using the same training/validation/test discipline.
2. Logistic Regression with explicitly engineered interaction features.

Use validation data for model/threshold selection. Keep the test set untouched until final comparison. Do not assume Random Forest will perform better; test the hypothesis.

## Reproducibility and limitations

- Record library versions, random seed, model settings, and data-generation settings.
- Fit preprocessing only on the relevant training partition.
- Never resample validation or test data.
- This small test set contains only 21 fraud cases, so each missed or detected case changes recall by about 4.76 percentage points.
- Alert counts are for this fixed synthetic test set, not a daily production volume.
