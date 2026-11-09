# Session 04 — Imbalanced Fraud Classification and Threshold Trade-offs

**Date:** 2026-11-09  
**Track:** Machine learning foundations → applied experimentation  
**Format:** Guided notebook implementation, metric interpretation, and model-selection reasoning

## 1. Practical work completed

Continued the synthetic fraud-classification experiment. The dataset contains 10,000 rows, 8 features, and a highly imbalanced target (9,895 legitimate; 105 fraud). A stratified split produced 8,000 training rows and 2,000 test rows; the test set contains 21 fraud cases.

Implemented and compared:
- Baseline Logistic Regression.
- SMOTE + Logistic Regression, with scaling and resampling restricted to training data.
- Class-weighted Logistic Regression.
- Validation-based threshold tuning for the class-weighted model.

## 2. Results observed

| Model / method | Test precision | Test recall | False positives | False negatives | Fraud alerts |
|---|---:|---:|---:|---:|---:|
| Baseline Logistic Regression | 100.00% | 4.76% | 0 | 20 | 1 |
| SMOTE + Logistic Regression | 3.61% | 85.71% | 481 | 3 | 499 |
| Class-weighted Logistic Regression (0.50) | 3.73% | 90.48% | 491 | 2 | 510 |
| Class-weighted, threshold 0.80 | 5.61% | 28.57% | 101 | 15 | 107 |

The class-weighted default confusion matrix was [[1488, 491], [2, 19]]. The validation threshold table showed no tested threshold meeting both constraints (recall >= 90%, alerts <= 100). Threshold 0.80 was selected as a best-effort diagnostic choice: validation produced 89 alerts at 29.41% recall. On the untouched test set it produced 107 alerts at 28.57% recall, so neither business constraint was met.

## 3. What the learner demonstrated

- Correctly predicted the direction of threshold changes: increasing the threshold generally reduces false positives and recall, while increasing false negatives.
- Correctly explained that a basic Logistic Regression model has a linear decision boundary and can struggle with nonlinear patterns and interactions unless features are engineered.
- Identified that an explicit interaction feature can help Logistic Regression represent a combined effect.
- Understood that Random Forest can model nonlinear relationships and interactions through tree splits.
- Correctly interpreted the trade-off in the observed threshold results: lower alert volume came at the cost of missing more fraud.

These were guided explanations and should be recorded as practised with guidance, not independent mastery.

## 4. Important interpretation and limitations

- No tested threshold met both operational constraints.
- Threshold tuning cannot create better ranking/separation if fraud and legitimate score distributions overlap.
- The test set contains only 21 fraud cases, so recall changes in increments of about 4.76 percentage points.
- The alert cap is an exercise constraint on this 2,000-row synthetic test set; it is not a real daily production volume.
- Results on synthetic data do not establish real-world fraud performance.
- Do not use the test set to tune another threshold. Use validation data for model and threshold selection, then evaluate the chosen approach once on the held-out test set.

## 5. Next experiment

Compare a Random Forest model against Logistic Regression with explicitly engineered interaction features. Keep the validation/test discipline consistent, compare precision-recall behaviour and operational constraints, and record negative results as carefully as positive ones.
