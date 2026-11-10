# Intelligence Lab — 90-Day Topic & Subtopic Checklist

**Sprint:** 9 November 2026 – 6 February 2027  
**Daily commitment:** 3 focused hours  
**Companion plan:** [90-Day Deep Research Curriculum](roadmap-3-month-accelerated.md)

> Tick a box only when the topic has been practised to the evidence level required—not just watched or discussed. A checked item means we have covered it in the current learning work with practical evidence; it does not automatically mean independent mastery. Unticked topics remain on the curriculum.

## Progress snapshot

- [x] Classification evaluation foundations: confusion matrix, precision, recall, F1 and class-imbalance trade-offs.
- [x] Leakage-aware train/validation/test workflow and stratified splitting.
- [x] Repeated stratified cross-validation: compared matched 8-feature and 6-feature Random Forests across 15 folds; interpreted paired differences and variability.
- [x] Logistic Regression and Random Forest applied to the fraud-classification experiment.
- [x] Threshold selection under recall and alert-volume constraints.
- [x] Feature interactions and permutation feature importance.
- [x] Complete feature-ablation experiment and controlled same-task holdout replication; original 8-feature Random Forest outperformed reduced 6-feature model on PR-AUC, precision and F1.
- [x] Complete the baseline foundations diagnostic (10/10 in linear algebra, calculus/optimisation practice, and probability/statistics; probability/statistics independence still needs verification).

## A. Mathematical foundations

### Linear algebra
- [ ] Scalars, vectors, matrices, tensors and linear transformations
- [ ] Vector spaces, span, basis, dimension, rank, null space and column space
- [ ] Dot products, norms, distances and cosine similarity
- [ ] Orthogonality, orthonormal bases, projections and least squares
- [x] Eigenvalues and eigenvectors: characteristic equations, independent calculations and verification of Av = λv; diagonalisation remains pending
- [ ] Singular value decomposition (SVD), low-rank approximation and matrix factorisation
- [ ] Positive-definite matrices and quadratic forms
- [x] PCA concepts: eigenvalues/variance, principal components, explained variance, information loss and feature loadings; implementation remains pending

### Calculus and matrix calculus
- [ ] Limits and continuity as needed for optimisation
- [x] Derivatives and partial derivatives — practised and independently demonstrated; directional derivatives remain pending
- [x] Chain rule and computational graphs — independently demonstrated
- [ ] Gradients, Jacobians and Hessians (gradient intuition/practice covered; Jacobians and Hessians remain pending)
- [ ] Taylor approximation and curvature intuition
- [ ] Gradients of common ML losses and simple matrix expressions

### Probability and statistics
- [ ] Random variables, PMF/PDF/CDF and common distributions
- [ ] Expectation, variance, covariance and correlation
- [ ] Joint, marginal and conditional probability
- [ ] Conditional independence and Bayes' theorem
- [ ] Sampling, estimators, bias and variance
- [ ] Maximum likelihood estimation (MLE) and maximum a posteriori (MAP) intuition
- [ ] Confidence intervals, hypothesis testing and p-values
- [ ] Bootstrap and uncertainty estimation

### Information theory
- [ ] Entropy and cross-entropy
- [ ] KL divergence and its interpretation
- [ ] Mutual information and conditional mutual information
- [ ] Connection between likelihood, log loss and information

## B. Machine learning and statistical learning theory

### Classical ML
- [ ] Linear regression
- [x] Logistic regression — applied in fraud-classification experiment
- [ ] k-nearest neighbours
- [ ] Decision trees
- [x] Random Forest — trained and evaluated in fraud-classification experiment
- [ ] Gradient boosting concepts
- [ ] Support vector machines and margins
- [ ] Naive Bayes
- [ ] Clustering basics where relevant
- [x] Feature engineering — engineered interaction features in fraud experiment
- [x] Preprocessing and leakage prevention — applied in split/fit/evaluation workflow

### Evaluation and reliability
- [x] Repeated stratified cross-validation and paired fold comparison — 5 folds × 3 repeats; interpreted mean, standard deviation and fold wins without claiming independence.
- [x] Train/validation/test separation and stratified splitting
- [x] Confusion matrix: TP, FP, TN and FN
- [x] Accuracy, precision, recall and F1
- [ ] Specificity and balanced accuracy — independent derivation/practice
- [x] ROC/precision–recall evaluation concepts and PR-AUC
- [x] Threshold selection under operational constraints
- [ ] Calibration, probability quality and uncertainty
- [x] Class imbalance and class weighting
- [x] Resampling/SMOTE concepts and train-only application discipline
- [ ] Error analysis and subgroup analysis
- [ ] Data shift

### Learning theory
- [ ] Empirical risk minimisation (ERM) and expected risk
- [ ] Generalisation gap and train/test performance
- [ ] Bias–variance trade-off
- [ ] Underfitting, overfitting and regularisation
- [ ] L1/L2 regularisation, early stopping and dropout
- [ ] Model capacity and inductive bias
- [ ] VC dimension intuition
- [ ] PAC learning intuition, sample complexity and generalisation bounds
- [ ] No Free Lunch intuition and limits of benchmark claims

## C. Optimisation
- [x] Objective functions, gradients and gradient-descent optimisation — practised; loss-surface analysis remains pending
- [ ] Batch gradient descent, stochastic gradient descent and mini-batches
- [ ] Momentum and Nesterov momentum
- [ ] Adagrad, RMSProp, Adam and AdamW
- [ ] Learning-rate schedules and warm-up
- [ ] Conditioning, curvature, saddle points and local minima
- [ ] Gradient clipping, exploding and vanishing gradients
- [ ] Weight decay versus L2 penalty
- [ ] Optimisation versus generalisation

## D. Deep learning and PyTorch

### Neural-network foundations
- [ ] Perceptrons and linear decision boundaries
- [ ] MLPs and layers
- [ ] Sigmoid, tanh, ReLU, GELU and softmax
- [ ] MSE, binary cross-entropy and categorical cross-entropy
- [ ] Forward pass, computational graphs and backpropagation
- [ ] Chain-rule derivation for a small network
- [ ] Xavier/Glorot and He initialisation
- [ ] Batch normalisation and LayerNorm
- [ ] Dropout, weight decay and early stopping
- [ ] Embeddings and representation learning

### PyTorch practice
- [ ] Tensors, shapes, broadcasting and device placement
- [ ] Autograd and gradient inspection
- [ ] nn.Module, parameters and state dictionaries
- [ ] Dataset, DataLoader and batching
- [ ] Training and evaluation loops
- [ ] Optimisers, schedulers and loss functions
- [ ] Checkpointing, reproducibility and debugging
- [ ] GPU memory and basic profiling

## E. Transformers and language models
- [ ] Word, subword and byte-level tokenisation
- [ ] Token embeddings and positional information
- [ ] Positional embeddings and positional encodings
- [ ] Query, key and value projections
- [ ] Scaled dot-product self-attention
- [ ] Causal masks and attention masks
- [ ] Multi-head attention
- [ ] Residual connections and residual stream
- [ ] LayerNorm and pre-norm/post-norm intuition
- [ ] MLP/feed-forward blocks and GELU
- [ ] Encoder, decoder and encoder–decoder architectures
- [ ] Autoregressive language modelling and next-token prediction
- [ ] Cross-entropy objective and perplexity
- [ ] Pretraining, supervised fine-tuning and preference-tuning concepts
- [ ] Context windows, inference and decoding strategies
- [ ] Language-model evaluation and limitations
- [ ] Scaling laws: empirical patterns, assumptions and limits

## F. Learning dynamics and generalisation research
- [ ] Training dynamics and learning curves
- [ ] Grokking and delayed generalisation
- [ ] Double descent
- [ ] Loss landscapes and optimisation trajectories
- [ ] Feature learning versus kernel-like behaviour
- [ ] Neural tangent kernel (NTK) intuition and regime limitations
- [ ] In-context learning: definitions, hypotheses and evaluation
- [ ] Scaling behaviour and scaling-law caveats
- [ ] Controlled synthetic tasks to study emergence of generalisation

## G. Mechanistic interpretability
- [ ] Neurons, features and distributed representations
- [ ] Polysemanticity and superposition
- [ ] Feature geometry and toy models of superposition
- [ ] Residual stream and information flow
- [ ] Attention heads and MLP contributions
- [ ] Induction heads and simple circuit hypotheses
- [ ] Activation and feature analysis
- [ ] Ablation and causal interventions
- [ ] Activation patching
- [ ] Sparse autoencoders (SAEs), dictionaries and feature splitting/merging caveats
- [ ] Feature attribution and attribution graphs
- [ ] Evaluating explanations, faithfulness and common failure modes
- [ ] Distinguishing correlational inspection from causal evidence

## H. Memory and continual learning
- [ ] Parametric versus non-parametric/external memory
- [ ] Associative memory and key–value retrieval
- [ ] Retrieval mechanisms and memory indexing
- [ ] Memory write, read, update, consolidation and deletion
- [ ] Short-term, working and long-term memory concepts
- [ ] Catastrophic forgetting and interference
- [ ] Experience replay and rehearsal
- [ ] Elastic Weight Consolidation (EWC) and regularisation approaches
- [ ] Parameter isolation and modular approaches
- [ ] Online learning and continual learning
- [ ] Test-time adaptation and test-time training
- [ ] Retention, forward/backward transfer, adaptation, retrieval quality and forgetting metrics

## I. Agentic intelligence and reinforcement learning

### Agents
- [ ] Agent loop: observe, reason/plan, act, evaluate and recover
- [ ] State, context, memory and tool interfaces
- [ ] Planning, search and decomposition
- [ ] Tool use and ReAct-style patterns
- [ ] Reflection/feedback loops and their limits
- [ ] Agent memory and state management
- [ ] Multi-agent systems: roles, coordination and communication
- [ ] Agent benchmarks, task success and generalisation
- [ ] Reliability, robustness, tool errors, recovery, latency and cost

### Reinforcement learning foundations
- [ ] Agent, environment, state, action and reward
- [ ] Markov decision processes
- [ ] Policies, returns and value functions
- [ ] Bellman equations and dynamic programming intuition
- [ ] Exploration versus exploitation
- [ ] Q-learning and temporal-difference learning
- [ ] Policy gradients and actor–critic intuition
- [ ] Reward design, reward hacking and specification issues
- [ ] Credit assignment and long-horizon evaluation
- [ ] Distinguishing learning from interaction from tool orchestration

## J. Data, cloud and research engineering

### Data
- [ ] SQL: filtering, joins, grouping, subqueries and window-function basics
- [ ] Data modelling and schema design
- [ ] Data quality, missingness, outliers and validation
- [ ] Dataset splits, leakage, sampling and class imbalance
- [ ] Data pipelines, lineage and dataset versioning

### Systems and cloud
- [ ] Linux shell and process/file basics
- [ ] Git branching, commits, diffs and collaboration
- [ ] Docker images, containers and reproducible environments
- [ ] Cloud storage and object stores
- [ ] Compute instances, GPUs and job execution
- [ ] Networking basics, APIs and deployment flow
- [ ] IAM, least privilege, secrets and security fundamentals
- [ ] Monitoring, logging, cost and resource management
- [ ] Distributed training concepts: data parallelism, communication overhead and checkpoints

### Research engineering
- [ ] Experiment configs and random seeds
- [ ] Metric definitions and evaluation scripts
- [ ] Experiment tracking and artifact storage
- [ ] Checkpoints and run recovery
- [ ] Unit tests and data/model sanity checks
- [ ] Benchmark design, baselines, ablations and robustness checks
- [ ] Reproducible environment and clear README/report

## 90-day milestone checklist

### Day 21 — Foundations
- [ ] Complete diagnostic and gap map
- [ ] Implement linear regression and gradient descent
- [ ] Implement PCA and interpret loadings
- [ ] Complete fraud-classification feature ablation and report
- [ ] Write one structured paper critique

### Day 42 — Deep learning and transformers
- [ ] Derive and implement a small MLP
- [ ] Build a reproducible PyTorch training loop
- [ ] Implement self-attention and a minimal transformer block
- [ ] Train/evaluate a small language model or document a compute-constrained alternative

### Day 66 — Research pillars
- [ ] Run a controlled learning-dynamics experiment
- [ ] Complete a scoped interpretability investigation
- [ ] Build a memory/continual-learning comparison
- [ ] Write paper critiques and record limitations

### Day 84 — Agents and research design
- [ ] Build and evaluate a small controlled agent
- [ ] Implement a tiny tabular RL example or document the scoped alternative
- [ ] Select a research question and write an experiment protocol

### Day 90 — Capstone
- [ ] Complete the core experiment and an ablation/robustness check
- [ ] Publish reproducible code, configs and experiment logs
- [ ] Write a research-style report with limitations
- [ ] Create the next 3–6 month research plan

## How to update this checklist

- Tick a subtopic only after meaningful practice.
- For mathematics: solve a fresh derivation/problem without step-by-step help.
- For implementation topics: build and test a minimal working version.
- For research methods: apply the method, interpret evidence and state limitations.
- If a topic is familiar from prior education/work but not yet independently checked in this sprint, leave it unticked until the diagnostic confirms it.
