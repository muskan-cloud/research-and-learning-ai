# Session 03 — Independent Linear Algebra, PCA, and Classification Metrics

**Date:** 2026-11-09  
**Track:** Mathematical foundations → machine learning foundations  
**Format:** Independent problem solving, guided conceptual learning, and applied reasoning

## 1. Independent calculus checkpoint

The learner worked through fresh problems involving composite functions, chain rule, gradients, and gradient descent.

### Problem A

For \(a=3w+1\), \(L=a^2\), at \(w=2\):

- \(a=7\)
- \(L=49\)
- \(dL/da=14\)
- \(da/dw=3\)
- \(dL/dw=42\)

All answers were correct.

### Problem B

For \(a=w^2+2\), \(L=(a-5)^2\), at \(w=3\):

- Correctly calculated \(a=11\).
- Initially calculated the forward loss incorrectly as 4; the correct loss is 36.
- Correctly calculated \(dL/da=12\), \(da/dw=6\), and \(dL/dw=72\).
- Correctly applied a learning rate of 0.1 to obtain \(w_{new}= -4.2\).

This shows correct derivative-chain reasoning, with a forward-pass arithmetic error.

### Problem C

For \(L=(w-4)^2\) at \(w=2\), the learner initially selected the wrong gradient direction. After feedback, correctly solved a related fresh check with \(L=(w-5)^2\) at \(w=8\): positive gradient, decrease the parameter to reduce loss, move left.

### Problem D

For \(L(x,y)=x^2+2y^2\), at \((x,y)=(3,2)\), learning rate 0.1:

- Gradients: \((6,8)\)
- Updated parameters: \((2.4,1.2)\)
- New loss: \(8.64\)

All correct.

**Assessment:** Promising independent calculus evidence across several fresh problems. Do not mark calculus mastered yet; continue testing forward-pass accuracy and independent gradient-direction reasoning.

## 2. Eigenvalues and eigenvectors — independent exercise

Given:

\[
A=\begin{bmatrix}4&1\\2&3\end{bmatrix}
\]

The learner independently completed the full calculation.

### Characteristic equation

\[
A-\lambda I=
\begin{bmatrix}4-\lambda&1\\2&3-\lambda\end{bmatrix}
\]

\[
\det(A-\lambda I)=(4-\lambda)(3-\lambda)-2
\]

\[
\lambda^2-7\lambda+10=0
\]

\[
(\lambda-5)(\lambda-2)=0
\]

Eigenvalues:

\[
\boxed{\lambda_1=5,\quad \lambda_2=2}
\]

### Corresponding eigenvectors

For \(\lambda=5\):

\[
(A-5I)v=0 \Rightarrow -x+y=0
\]

One valid eigenvector:

\[
v_1=\begin{bmatrix}1\\1\end{bmatrix}
\]

For \(\lambda=2\):

\[
(A-2I)v=0 \Rightarrow 2x+y=0
\]

One valid eigenvector:

\[
v_2=\begin{bmatrix}1\\-2\end{bmatrix}
\]

The learner also verified the eigenvalue relationship:

\[
Av_1=5v_1,\qquad Av_2=2v_2
\]

**Assessment:** Correct independent solution of one complete 2×2 eigenvalue/eigenvector problem, including verification. This is strong evidence of independent practice, not yet broad mastery across different matrix types.

## 3. PCA and explained variance

Topics discussed:

- PCA creates new directions as linear combinations of original numerical features.
- Eigenvectors of a covariance matrix give principal-component directions.
- Eigenvalues indicate the variance captured along those directions.
- A larger eigenvalue corresponds to a principal component explaining more variance.
- Explained-variance ratio is the component eigenvalue divided by the sum of all eigenvalues.
- Retaining fewer components reduces dimensionality but discards some variation.

### Guided example

Given eigenvalues 90 and 10:

\[
\frac{90}{90+10}\times100=90\%
\]

The learner correctly identified that the eigenvector corresponding to eigenvalue 90 represents the first, more variance-explaining principal component.

### Important conceptual distinction

High variance does not necessarily mean high predictive value. PCA is unsupervised and prioritises variance, not a target label. A low-variance direction may still carry useful information for a supervised task, such as fraud detection.

### Fraud-detection illustration

A hypothetical transaction dataset was used to distinguish original features from principal components.

Original features included transaction amount, transaction hour, transaction frequency, average amount, distance from usual location, failed attempts, account age, merchant risk, payment method, and device change.

The learner understood that principal components are combinations of original features, not simply renamed raw columns. Feature loadings can help interpret which original features contribute to a component.

**Caveat:** Example component labels and variance percentages were illustrative only, not computed from a real dataset.

## 4. Classification evaluation and threshold trade-offs

Topics discussed:

- Recall: proportion of actual positive cases correctly detected.
- Precision: proportion of predicted positive cases that are truly positive.
- False positives: legitimate transactions incorrectly flagged as fraud.
- False negatives: fraudulent transactions incorrectly missed.
- Raising the classification threshold generally increases precision and decreases recall, though actual changes depend on the model and data.

### Guided scenario

A hypothetical model had 95% recall and 40% precision.

The learner correctly explained:

- 95% recall means the model detects 95% of actual fraudulent transactions.
- 40% precision means only 40% of transactions flagged as fraud are actually fraudulent.
- The remaining 60% of flagged transactions are false positives.

A correction was made: false positives are not necessarily random noise; they are legitimate transactions incorrectly classified as fraud.

### Threshold scenario

The learner correctly reasoned that increasing the threshold makes the model stricter:

- Fewer transactions are flagged.
- Precision generally increases.
- Recall generally decreases.
- Some genuine fraud cases may be missed.

### Ablation study

The learner was introduced to comparing a model with PC1 + PC2 + PC3 against one with only PC1 + PC2 to test whether PC3 contributes useful predictive information.

**Assessment:** Good guided conceptual reasoning. A fresh independent confusion-matrix calculation and a practical evaluation exercise are still needed.

## 5. Strengths observed

- Reconstructed a complete eigenvalue/eigenvector solution independently.
- Correctly distinguished the zero-vector equation used to solve for eigenvectors from the original relationship \(Av=\lambda v\).
- Connected PCA variance to dimensionality reduction and information loss.
- Recognised that low-variance features may still contain predictive signal.
- Correctly interpreted precision, recall, false positives, and threshold changes.
- Asked useful clarification questions when the covariance matrix or data assumptions were missing.

## 6. Gaps and next steps

1. Solve additional eigenvalue/eigenvector problems with different matrices and verify results.
2. Build a small PCA example in Python using a real numerical dataset.
3. Inspect explained-variance ratios and feature loadings.
4. Compare classification models with and without selected principal components.
5. Calculate a confusion matrix, precision, recall, specificity, and F1 independently.
6. Explore threshold selection using validation data and the costs of false positives and false negatives.
7. Implement an ablation study and record results.

## Assessment note

This session combined independent calculations with guided conceptual questions. Keep the distinction visible: the eigenvalue/eigenvector exercise is independent evidence; the PCA and classification topics are primarily guided understanding and require independent application.
