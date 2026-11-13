# Generalisation, Memorisation & Double Descent — 2026-11-13

This reading pair follows the current study of bias, variance, overfitting, and Random Forest regularisation. The first paper challenges simple explanations of why large networks generalise; the second shows that test error can behave non-monotonically as model size, training time, or dataset size changes.

Both papers are **peer-reviewed conference papers**. Their arXiv links are preprint records; the venue labels below refer to the published conference versions.

---

## 1. Understanding Deep Learning Requires Rethinking Generalization

- **Authors:** Chiyuan Zhang, Samy Bengio, Moritz Hardt, Benjamin Recht, Oriol Vinyals
- **Publication:** International Conference on Learning Representations (ICLR), 2017
- **Status:** Peer-reviewed conference paper. The arXiv preprint was first submitted on 10 November 2016 and revised on 26 February 2017.
- **Canonical preprint:** https://arxiv.org/abs/1611.03530
- **Publication record:** https://research.google/pubs/understanding-deep-learning-requires-rethinking-generalization/

### Research question

Why can highly overparameterised neural networks generalise well, even though they have enough capacity to fit arbitrary labels on a finite training set?

### Main contribution

The paper shows that the ability to fit the training data—including random labels—is not, by itself, a good explanation of why a neural network generalises on real data. It challenges explanations based only on parameter count or conventional explicit regularisation and motivates closer study of the inductive biases introduced by architecture, data, and optimisation.

### Method

- Train modern convolutional networks on image-classification datasets under several controlled changes: true labels, randomly assigned labels, and inputs whose structure is disrupted or replaced with random noise.
- Compare how readily the networks fit these datasets, and examine whether explicit regularisation prevents that fitting in the tested settings.
- Provide a theoretical construction showing that a simple two-layer neural network can have perfect finite-sample expressivity once its parameter count exceeds the number of data points.

### Key evidence

- The tested networks can fit randomly assigned training labels, even when the original image structure is destroyed.
- This memorisation ability is not qualitatively eliminated by the explicit regularisation methods examined.
- The theoretical construction reinforces that finite-sample fitting capacity alone cannot explain the small train–test gap often observed on real tasks.

### Limitations and cautions

- The experiments focus on particular image-classification architectures, datasets, and training procedures; they do not establish that every neural network behaves identically.
- Showing that a network *can* memorise random labels does not explain why it often learns useful structure from real labels.
- The paper is a challenge to simple capacity-based explanations, not a complete theory of generalisation or evidence that regularisation is useless.

### Why it matters for the Intelligence Lab path

This is a foundational bridge from the classical bias–variance picture to modern deep learning. It helps separate **capacity to memorise** from **the solution actually found by training**. For the fraud-classification work, it is a reminder that a training–validation gap is useful evidence, but parameter count or model complexity alone does not fully explain generalisation.

### Reading questions

1. What exactly do the random-label experiments establish—and what do they leave unexplained?
2. Why is the ability to fit random labels compatible with good generalisation on real labels?
3. Which parts of the learning process (architecture, data structure, initialisation, optimiser, or training duration) would you investigate to explain the gap?

---

## 2. Deep Double Descent: Where Bigger Models and More Data Hurt

- **Authors:** Preetum Nakkiran, Gal Kaplun, Yamini Bansal, Tristan Yang, Boaz Barak, Ilya Sutskever
- **Publication:** International Conference on Learning Representations (ICLR), 2020
- **Status:** Peer-reviewed conference paper. The arXiv preprint was first submitted on 4 December 2019.
- **Canonical preprint:** https://arxiv.org/abs/1912.02292
- **Conference page:** https://iclr.cc/virtual_2020/poster_B1g5sA4twr.html

### Research question

Does test error always rise once a model becomes complex enough to fit its training data, or can generalisation improve again beyond that point?

### Main contribution

The authors provide broad empirical evidence for **double descent**: test error can decrease, rise around the point where training error approaches zero (the interpolation threshold), and then decrease again as effective model complexity grows further. They study this pattern across model size, training time, and training-set size.

They introduce **effective model complexity (EMC)**: informally, the maximum number of samples on which a particular training procedure can achieve near-zero training error. EMC depends not just on architecture, but also on the data distribution and training procedure.

### Method

- Vary the width of CNNs and ResNets, and the embedding dimension of encoder–decoder Transformers.
- Measure test performance as training progresses, including changes across epochs.
- Vary training-set size and label noise.
- Compare settings using SGD and Adam, with and without data augmentation, across image classification and machine-translation tasks.

### Key evidence

- Model-wise double descent appears in experiments involving CNNs, ResNets, and Transformers, including CIFAR-10, CIFAR-100, and IWSLT'14 translation.
- Epoch-wise double descent appears in some fixed-model training runs: test error first falls, rises near the interpolation region, and later falls again.
- The authors find settings in which adding training examples shifts the critical region and can temporarily worsen test performance for particular model sizes. This is a conditional result, not a claim that more data is generally harmful.
- The effect is often stronger with label noise, although the paper also reports some peaks without added label noise.

### Limitations and cautions

- The proposed generalised EMC account is partly a hypothesis: the paper uses a heuristic tolerance for “near-zero” training error and does not fully formalise what counts as sufficiently under- or over-parameterised.
- The authors state that the mechanisms behind double descent in deep neural networks are not fully understood.
- Results depend on the dataset, architecture, optimiser, regularisation, and training regime. Double descent is not a universal curve that every model must display.
- The paper's large-scale image and translation experiments should not be assumed to transfer directly to a small tabular fraud dataset or a Random Forest.

### Why it matters for the Intelligence Lab path

This paper adds an important qualification to the simple “more complexity means more variance” story. It shows why model selection should be empirical and why training time, data size, and optimisation can change effective complexity. It is a useful next step after learning max_depth, min_samples_leaf, and validation-based tuning: regularisation is a tool to test, not a guarantee that every move toward a simpler model improves test performance.

### Reading questions

1. What is the interpolation threshold, and why can test error peak near it?
2. How does effective model complexity differ from simply counting a model's parameters?
3. Which experiment would you run to check whether a double-descent pattern exists in a small tabular dataset—and what controls would you need before trusting the result?

---

## Suggested reading order

1. **Zhang et al.** — focus on the random-label experiments and the distinction between memorisation capacity and generalisation.
2. **Nakkiran et al.** — focus on the model-wise and epoch-wise curves, then read the EMC definition and discussion of open questions.

## Connection to the current study

When comparing training and validation PR-AUC, keep using the gap as a diagnostic—not as a complete explanation. Tune one factor at a time, use stratified cross-validation where appropriate, preserve an untouched test set, and report uncertainty. These papers provide conceptual context; they do not establish that double descent is occurring in the current fraud-classification experiment.

*These briefs are reading guides, not substitutes for checking the papers' figures, experimental setup, and full arguments.*
