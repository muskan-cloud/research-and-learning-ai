# 24-Month Research Curriculum — Slower Reference Path

> **Reference document only.** The active plan is the [90-day deep research curriculum](roadmap-3-month-accelerated.md), designed around 3 focused hours per day. Use that document for current scheduling, detailed topics and evidence gates.


The roadmap is a scaffold, not a rigid deadline. Move faster or slower based on demonstrated understanding. Do not advance merely because a calendar period has ended.

## Phase 1 — Mathematical foundations (Months 1–3)

**Goal:** Build the mathematical language needed to understand machine learning papers and derive core algorithms.

- Linear algebra: vectors, matrices, bases, rank, projections, eigenvalues, singular value decomposition.
- Calculus: derivatives, partial derivatives, chain rule, gradients, Jacobians, Hessians.
- Probability: random variables, distributions, expectation, variance, conditional probability, Bayes' rule.
- Optimisation: objective functions, gradients, gradient descent, constrained optimisation.
- Information theory: entropy, cross-entropy, KL divergence, mutual information.

**Exit evidence:** Explain and implement linear regression with gradient descent; derive gradients for simple functions; interpret matrix transformations and probability distributions.

## Phase 2 — Machine-learning theory (Months 4–6)

**Goal:** Understand why learning algorithms work and when they fail.

- Linear and logistic regression; likelihood and maximum likelihood estimation.
- Empirical risk minimisation and regularisation.
- Bias-variance trade-off and model selection.
- Generalisation, overfitting, train/validation/test discipline.
- SGD, momentum, adaptive optimisers.
- Statistical learning theory: capacity, VC dimension, PAC-style intuition.
- Calibration, uncertainty, and evaluation.

**Exit evidence:** Implement and compare baseline models; explain generalisation gaps; design a sound evaluation protocol.

## Phase 3 — Deep learning and transformers (Months 7–9)

**Goal:** Understand modern neural networks from computation to training.

- Perceptrons and multilayer networks.
- Backpropagation and automatic differentiation.
- Initialisation, normalisation, regularisation, and optimisation.
- Embeddings and representation learning.
- Attention and self-attention.
- Transformer blocks, positional information, residual streams.
- Language-model objectives and pretraining.

**Exit evidence:** Implement a small neural network and a minimal transformer; explain the forward and backward passes.

## Phase 4 — Learning dynamics and emergence (Months 10–12)

**Goal:** Study unexpected behaviours and changes in learning regimes.

- Loss landscapes and optimisation trajectories.
- Grokking and delayed generalisation.
- Neural scaling laws and their limits.
- Double descent and interpolation.
- Feature learning versus kernel-like regimes.
- In-context learning and induction-like behaviour.
- Hypothesis formation and controlled replication.

**Exit evidence:** Reproduce a small learning-dynamics experiment and report controls, metrics, and limitations.

## Phase 5 — Mechanistic interpretability (Months 13–15)

**Goal:** Develop tools for investigating what neural networks compute internally.

- Neurons, features, and distributed representations.
- Superposition and polysemanticity.
- Sparse autoencoders and feature dictionaries.
- Activation patching and causal interventions.
- Attention and MLP circuits.
- Interpretability metrics and failure modes.

**Exit evidence:** Complete a small interpretability investigation with a falsifiable question and causal tests.

## Phase 6 — Memory and continual learning (Months 16–18)

**Goal:** Understand how systems retain, retrieve, and update knowledge.

- Parametric and external memory.
- Retrieval and associative memory.
- Catastrophic forgetting.
- Replay, regularisation, and parameter-isolation methods.
- Continual and online learning.
- Long-context systems and memory architectures.
- Evaluation of memory quality, retrieval, and updating.

**Exit evidence:** Compare at least two continual-learning or memory strategies on a controlled task.

## Phase 7 — Independent research (Months 19–21)

**Goal:** Move from reading papers to producing a defensible research result.

- Map a focused literature area.
- Identify an unresolved, appropriately scoped question.
- Form a falsifiable hypothesis.
- Design baselines, controls, and ablations.
- Predefine metrics and analysis.
- Track uncertainty, negative results, and reproducibility.
- Seek feedback and revise.

**Exit evidence:** A research proposal and a reproducible experiment with a clear limitations section.

## Phase 8 — Research portfolio (Months 22–24)

**Goal:** Communicate and extend independent work.

- Consolidate results and related work.
- Write a technical report or paper-style manuscript.
- Publish code, configurations, and experiment records.
- Prepare a research presentation.
- Identify follow-up questions and collaborators.
- Prepare applications or outreach to relevant research groups.

**Exit evidence:** A public-facing, reproducible research project and a clear next research direction.

## Weekly operating loop

1. Learn one concept.
2. Derive or explain it without notes.
3. Implement or test it.
4. Read a relevant primary source.
5. Record confusion and unresolved questions.
6. Review progress and update the next week's plan.

## Progress policy

A topic is complete only when there is evidence: a derivation, implementation, explanation, problem set, or experiment. A checked box alone is not proof of mastery.
