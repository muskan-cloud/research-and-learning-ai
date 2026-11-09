# Intelligence Lab — 90-Day Deep Research Curriculum

**Sprint dates:** 9 November 2026 – 6 February 2027  
**Daily commitment:** 3 focused hours/day, 7 days/week = 21 hours/week, approximately 270 hours across 90 days.  
**Learning style:** Deep theory, mathematical derivations, implementation, paper reading and experiments.  
**North-star question:** How do learning systems acquire, represent, retain and use knowledge to generalise and act?

> This curriculum compresses scheduling, not the topic list. It is designed for an Applied AI Engineer with prior CS, data-science, ML and AI engineering experience. Familiar topics should be validated quickly, not retaught from zero. Three months can establish a serious foundation and produce a scoped research project; it cannot guarantee mastery of every advanced subfield or frontier-lab readiness. Protect sleep and health. If a topic needs more time, record it as a continuation rather than pretending it is mastered.

## 1. Research direction: four connected pillars

Explore all four throughout the sprint. Do not force premature specialisation.

1. **Learning and generalisation:** how models acquire structure, generalise beyond training data and adapt.
2. **Mechanistic interpretability:** what representations and computations emerge inside neural networks, and how to test explanations causally.
3. **Memory and continual learning:** how systems retain, retrieve, update and forget knowledge over time.
4. **Agentic intelligence:** how systems plan, reason, use tools, interact with environments and learn from feedback.

**Unifying research lens:** how knowledge is learned, represented, retained and used. Investigate connections experimentally rather than assuming a single explanation.

## 2. What depth means in a 270-hour sprint

Keep every requested topic in the curriculum, but be explicit about the expected depth:

- **Core competence:** derive/explain the central idea, implement a small version, and evaluate it. Prioritise linear algebra, calculus for learning, probability/statistics, optimisation, classical ML evaluation, neural-network training, backpropagation, attention, experimental design and reproducibility.
- **Research literacy:** understand assumptions, mathematical intuition, key methods and limitations; reproduce a small demonstration where feasible. Includes PAC/VC ideas, NTK intuition, scaling laws, interpretability methods, continual-learning methods and agent architectures.
- **Exploratory exposure:** understand the problem, main approaches and open questions; do not claim mastery. Includes advanced attribution graphs, multi-agent systems, distributed training and broad frontier claims.

At the end of the sprint, use evidence gates—not topic count—to decide what is mastered and what becomes the next research cycle.

## 3. Daily study structure — exactly 3 focused hours

Use this default 180-minute structure. Adjust the split for a derivation-heavy or experiment-heavy day, but keep all four modes in the week.

| Block | Time | What to do |
|---|---:|---|
| Theory and derivation | 60 min | Read a textbook/lecture note/paper section; derive equations by hand |
| Implementation and problem solving | 60 min | Code a minimal implementation, solve problems, or run a controlled experiment |
| Research reading / experiment analysis | 40 min | Read a primary paper, inspect results, compare methods or analyse outputs |
| Learning journal and recall | 20 min | Explain from memory, record questions, results, mistakes and next steps |
| **Total** | **180 min** | **3 focused hours** |

Weekly pattern:
- 4 days: core concepts, derivations and implementation.
- 2 days: research papers, experiments and deeper problem sets.
- 1 day: 3-hour consolidation day—closed-book recall, a fresh problem, experiment review and planning. It is still a focused study day, but lighter in intensity.

Take short breaks between blocks; breaks do not count as focused hours.

## 4. Full topic inventory

### A. Mathematical foundations

**Linear algebra**
- Scalars, vectors, matrices, tensors and linear transformations.
- Vector spaces, span, basis, dimension, rank, null space and column space.
- Dot products, norms, distances and cosine similarity.
- Orthogonality, orthonormal bases, projections and least squares.
- Eigenvalues, eigenvectors, diagonalisation and geometric interpretation.
- Singular value decomposition (SVD), low-rank approximation and matrix factorisation.
- Positive-definite matrices and quadratic forms.
- PCA: covariance matrix, principal directions, explained variance and loadings.

**Calculus and matrix calculus**
- Limits and continuity as needed for optimisation.
- Derivatives, partial derivatives and directional derivatives.
- Chain rule and computational graphs.
- Gradients, Jacobians and Hessians.
- Taylor approximation and curvature intuition.
- Gradients of common ML losses and simple matrix expressions.

**Probability and statistics**
- Random variables, PMF/PDF/CDF and common distributions.
- Expectation, variance, covariance and correlation.
- Joint, marginal and conditional probability.
- Conditional independence and Bayes' theorem.
- Sampling, estimators, bias and variance.
- Maximum likelihood estimation (MLE) and maximum a posteriori (MAP) intuition.
- Confidence intervals, hypothesis testing and p-values.
- Bootstrap and uncertainty estimation.

**Information theory**
- Entropy and cross-entropy.
- KL divergence and its interpretation.
- Mutual information and conditional mutual information.
- Connection between likelihood, log loss and information.

### B. Machine learning and statistical learning theory

**Classical ML**
- Linear regression and logistic regression.
- k-nearest neighbours.
- Decision trees and Random Forests.
- Gradient boosting concepts.
- Support vector machines and margins.
- Naive Bayes.
- Clustering basics where relevant.
- Feature engineering, preprocessing and leakage prevention.

**Evaluation and reliability**
- Train/validation/test separation and cross-validation.
- Confusion matrix, accuracy, precision, recall, specificity and F1.
- ROC curves, precision–recall curves and PR-AUC.
- Threshold selection under operational constraints.
- Calibration, probability quality and uncertainty.
- Class imbalance, class weighting and resampling.
- Error analysis, subgroup analysis and data shift.

**Learning theory**
- Empirical risk minimisation (ERM) and expected risk.
- Generalisation gap and train/test performance.
- Bias–variance trade-off.
- Underfitting, overfitting and regularisation.
- L1/L2 regularisation, early stopping and dropout.
- Model capacity and inductive bias.
- VC dimension intuition.
- PAC learning intuition, sample complexity and generalisation bounds.
- No Free Lunch intuition and limits of benchmark claims.

### C. Optimisation

- Objective functions, loss surfaces and gradients.
- Batch gradient descent, stochastic gradient descent and mini-batches.
- Momentum and Nesterov momentum.
- Adagrad, RMSProp, Adam and AdamW.
- Learning-rate schedules and warm-up.
- Conditioning, curvature, saddle points and local minima.
- Gradient clipping, exploding and vanishing gradients.
- Weight decay versus L2 penalty.
- Optimisation versus generalisation: why lower training loss does not guarantee better test performance.

### D. Deep learning and PyTorch

**Neural-network foundations**
- Perceptrons and linear decision boundaries.
- MLPs and layers.
- Activations: sigmoid, tanh, ReLU, GELU and softmax.
- Losses: MSE, binary cross-entropy and categorical cross-entropy.
- Forward pass, computational graphs and backpropagation.
- Chain-rule derivation for a small network.
- Initialisation: Xavier/Glorot and He.
- Batch normalisation and LayerNorm.
- Dropout, weight decay and early stopping.
- Embeddings and representation learning.

**PyTorch practice**
- Tensors, shapes, broadcasting and device placement.
- Autograd and gradient inspection.
- nn.Module, parameters and state dictionaries.
- Dataset, DataLoader and batching.
- Training and evaluation loops.
- Optimisers, schedulers and loss functions.
- Checkpointing, reproducibility and debugging.
- GPU memory and basic profiling.

### E. Transformers and language models

- Tokenisation: word, subword and byte-level intuition.
- Token embeddings and positional information.
- Positional embeddings and positional encodings.
- Query, key and value projections.
- Scaled dot-product self-attention.
- Causal masks and attention masks.
- Multi-head attention.
- Residual connections and residual stream.
- LayerNorm and pre-norm/post-norm intuition.
- MLP/feed-forward blocks and GELU.
- Encoder, decoder and encoder–decoder architectures.
- Autoregressive language modelling and next-token prediction.
- Cross-entropy objective and perplexity.
- Pretraining, supervised fine-tuning and preference-tuning concepts.
- Context windows, inference and decoding strategies.
- Language-model evaluation and limitations.
- Scaling laws: empirical patterns, assumptions and limits.

### F. Learning dynamics and generalisation research

- Training dynamics and learning curves.
- Grokking and delayed generalisation.
- Double descent.
- Loss landscapes and optimisation trajectories.
- Feature learning versus kernel-like behaviour.
- Neural tangent kernel (NTK) intuition and regime limitations.
- In-context learning: definitions, hypotheses and evaluation.
- Scaling behaviour and scaling-law caveats.
- Controlled synthetic tasks to study when and how generalisation emerges.

### G. Mechanistic interpretability

- Neurons, features and distributed representations.
- Polysemanticity and superposition.
- Feature geometry and toy models of superposition.
- Residual stream and information flow.
- Attention heads and MLP contributions.
- Induction heads and simple circuit hypotheses.
- Activation and feature analysis.
- Ablation and causal interventions.
- Activation patching.
- Sparse autoencoders (SAEs), dictionaries and feature splitting/merging caveats.
- Feature attribution and attribution graphs.
- Evaluating explanations, faithfulness and common failure modes.
- Difference between correlational inspection and causal evidence.

### H. Memory and continual learning

- Parametric versus non-parametric/external memory.
- Associative memory and key–value retrieval.
- Retrieval mechanisms and memory indexing.
- Memory write, read, update, consolidation and deletion.
- Short-term, working and long-term memory concepts.
- Catastrophic forgetting and interference.
- Experience replay and rehearsal.
- Elastic Weight Consolidation (EWC) and regularisation approaches.
- Parameter isolation and modular approaches.
- Online learning and continual learning.
- Test-time adaptation and test-time training.
- Evaluation: retention, forward/backward transfer, adaptation, retrieval quality and forgetting.

### I. Agentic intelligence and reinforcement learning

**Agents**
- Agent loop: observe, reason/plan, act, evaluate and recover.
- State, context, memory and tool interfaces.
- Planning, search and decomposition.
- Tool use and ReAct-style patterns.
- Reflection/feedback loops and their limits.
- Agent memory and state management.
- Multi-agent systems: roles, coordination and communication.
- Agent benchmarks, task success and generalisation.
- Reliability, robustness, tool errors, recovery, latency and cost.

**Reinforcement learning foundations**
- Agent, environment, state, action and reward.
- Markov decision processes.
- Policies, returns and value functions.
- Bellman equations and dynamic programming intuition.
- Exploration versus exploitation.
- Q-learning and temporal-difference learning.
- Policy gradients and actor–critic intuition.
- Reward design, reward hacking and specification issues.
- Credit assignment and long-horizon evaluation.
- Distinguish learning from interaction from merely orchestrating tools.

### J. Data, cloud and research engineering

**Data**
- SQL: filtering, joins, grouping, subqueries and window-function basics.
- Data modelling and schema design.
- Data quality, missingness, outliers and validation.
- Dataset splits, leakage, sampling and class imbalance.
- Data pipelines, lineage and dataset versioning.

**Systems and cloud**
- Linux shell and process/file basics.
- Git branching, commits, diffs and collaboration.
- Docker images, containers and reproducible environments.
- Cloud storage and object stores.
- Compute instances, GPUs and job execution.
- Networking basics, APIs and deployment flow.
- IAM, least privilege, secrets and security fundamentals.
- Monitoring, logging, cost and resource management.
- Distributed training concepts: data parallelism, communication overhead and checkpoints.

**Research engineering**
- Experiment configs and random seeds.
- Metric definitions and evaluation scripts.
- Experiment tracking and artifact storage.
- Checkpoints and run recovery.
- Unit tests and data/model sanity checks.
- Benchmark design, baselines, ablations and robustness checks.
- Reproducible environment and clear README/report.

## 5. The 13-week schedule

The weekly topic lists are detailed. Use the daily 3-hour template; do not try to watch every resource available. Each week should produce a small piece of evidence.

### Week 1 — Diagnostic and mathematical foundations I
**Topics**
- Linear algebra: vectors, matrices, transformations, span, basis, rank, norms, dot products and projections.
- Calculus: derivatives, partial derivatives, chain rule and gradients.
- Probability: random variables, distributions, expectation, variance and conditional probability.
- Python/NumPy refresh only where diagnostic results show gaps.

**Deep work**
- Derive least-squares linear regression in vector form.
- Derive gradients for a simple scalar loss.
- Implement linear regression and gradient descent from scratch.
- Solve a closed-book problem set.

**Evidence:** diagnostic record, derivations and a tested regression implementation.

### Week 2 — Mathematical foundations II, statistics and information theory
**Topics**
- Eigenvalues/eigenvectors, SVD, low-rank approximation and PCA.
- Jacobians and Hessians.
- Bayes' theorem, covariance, conditional independence and common distributions.
- Sampling, MLE/MAP, confidence intervals and hypothesis testing.
- Entropy, cross-entropy, KL divergence and mutual information.

**Deep work**
- Implement PCA; inspect explained variance and loadings.
- Derive MLE for a simple distribution and connect log likelihood to cross-entropy.
- Work through conditional-probability and information-theory problems.

**Evidence:** PCA notebook, derivation notes and independent maths checkpoint.

### Week 3 — Classical ML, evaluation and learning theory
**Topics**
- Linear/logistic regression, KNN, trees, Random Forest, boosting, SVM and Naive Bayes concepts.
- Feature engineering, preprocessing, cross-validation and leakage.
- Metrics, PR/ROC, calibration, thresholds and imbalance.
- ERM, regularisation, bias–variance, model capacity, VC/PAC intuition and sample complexity.

**Deep work**
- Finish and document the existing fraud-classification experiment, including feature ablation.
- Compare baselines and explain metric trade-offs.
- Derive regularised empirical-risk objectives and explain generalisation gaps.

**Evidence:** reproducible classification report and short learning-theory explanation.

### Week 4 — Optimisation and neural networks from first principles
**Topics**
- GD, SGD, mini-batches, momentum, Nesterov, Adagrad, RMSProp, Adam and AdamW.
- Learning-rate schedules, conditioning, curvature, saddle points and gradient pathologies.
- Perceptrons, MLPs, activations, losses and softmax.
- Backpropagation, initialisation, normalisation, dropout and weight decay.

**Deep work**
- Derive backpropagation for a tiny MLP.
- Implement a NumPy MLP and compare gradients with finite differences.
- Experiment with learning rates and optimisers.

**Evidence:** from-scratch MLP, gradient check and optimisation comparison.

### Week 5 — PyTorch and representation learning
**Topics**
- Tensors, autograd, modules, datasets, dataloaders, training loops and checkpoints.
- GPU/device basics, debugging and profiling.
- Embeddings, representation learning and feature geometry.
- SQL/data quality/dataset versioning; Linux/Git refresh.

**Deep work**
- Rebuild the MLP in PyTorch.
- Inspect gradients, activations and learned embeddings.
- Make the experiment reproducible with fixed seeds and saved configuration.

**Evidence:** documented PyTorch training pipeline and representation analysis.

### Week 6 — Transformers and language modelling I
**Topics**
- Tokenisation, embeddings, positional information.
- Q/K/V, scaled dot-product attention, causal masks and multi-head attention.
- Residual stream, LayerNorm, MLP blocks and encoder/decoder patterns.

**Deep work**
- Derive attention tensor shapes and scaled dot-product attention.
- Implement self-attention and a transformer block.
- Test causal masking and inspect attention outputs.

**Evidence:** tested minimal transformer components and a technical explanation.

### Week 7 — Language modelling II and deep-learning systems
**Topics**
- Autoregressive next-token prediction, cross-entropy and perplexity.
- Pretraining, fine-tuning, decoding and language-model evaluation.
- Scaling-law patterns and limitations.
- GPU memory, batching, profiling, checkpointing and distributed-training concepts.
- Cloud storage, compute, networking and IAM foundations.

**Deep work**
- Train a small character/token language model if compute allows.
- Compare training settings and evaluate held-out behaviour.
- Document compute, environment, checkpoints and limitations.

**Evidence:** small language-model experiment and reproducibility record.

### Week 8 — Learning dynamics and generalisation
**Topics**
- Grokking, delayed generalisation and double descent.
- Loss landscapes and optimisation trajectories.
- Feature learning versus kernel-like behaviour and NTK intuition.
- In-context learning hypotheses and scaling-law caveats.

**Deep work**
- Build a small synthetic task.
- Vary at least two factors such as weight decay, model size or training duration.
- Plot train/test behaviour and explain competing interpretations.
- Read and critique a primary paper on learning dynamics/generalisation.

**Evidence:** controlled experiment, plots and paper critique.

### Week 9 — Mechanistic interpretability
**Topics**
- Features, neurons, polysemanticity and superposition.
- Residual stream, attention heads, MLPs and induction heads.
- Feature analysis, ablation and activation patching.
- SAEs and feature dictionaries; attribution and attribution graphs.
- Faithfulness, causal evidence and interpretability failure modes.

**Deep work**
- Use an accessible small model or toy transformer.
- Form one falsifiable circuit/feature hypothesis.
- Run an activation analysis and one controlled intervention/ablation where feasible.
- Distinguish observation from causal evidence.

**Evidence:** scoped interpretability investigation with limitations.

### Week 10 — Memory and continual learning
**Topics**
- Parametric/external memory, associative memory and retrieval.
- Memory read/write/update/consolidation/forgetting.
- Catastrophic forgetting, replay, EWC and parameter isolation.
- Online learning and test-time adaptation.
- Retention, transfer, adaptation and retrieval metrics.

**Deep work**
- Build a small sequential-task or memory benchmark.
- Compare a no-memory baseline with one memory/replay method.
- Measure retention and adaptation; inspect failure cases.

**Evidence:** reproducible memory/continual-learning comparison.

### Week 11 — Agentic intelligence and reinforcement learning
**Topics**
- Agent loop, state, planning, search, tool use and ReAct-style patterns.
- Reflection, feedback, memory and recovery.
- Multi-agent coordination concepts.
- MDPs, policies, returns, value functions and Bellman equations.
- Exploration/exploitation, Q-learning, TD, policy gradients and actor–critic intuition.
- Reward design, reward hacking and credit assignment.

**Deep work**
- Build a small tool-using agent in a controlled environment.
- Compare a basic agent with a planning, memory or feedback intervention.
- Evaluate task success, tool errors, recovery, robustness and cost.
- Implement a tiny tabular RL example if time permits.

**Evidence:** agent evaluation and short RL implementation.

### Week 12 — Integrated research design and experiments
**Topics**
- Connect learning/generalisation, representations, memory and agent behaviour.
- Literature mapping, competing explanations and research gaps.
- Hypotheses, controls, baselines, metrics, ablations and robustness.
- Statistical uncertainty and reproducibility.

**Deep work**
- Select a tractable question supported by the previous weeks' evidence.
- Design a small integrated experiment. Candidate direction: how explicit memory changes an agent's retention and generalisation across a sequence of tasks.
- Define a baseline, one intervention, metrics and ablations before running.
- Run pilot experiments and revise scope.

**Evidence:** written research protocol and pilot results.

### Week 13 — Capstone, report and next research cycle
**Topics**
- Finish core experiments and at least one ablation/robustness check.
- Analyse failures, uncertainty and alternative explanations.
- Research writing, figures, methods and reproducibility.
- Next-stage literature map and research plan.

**Deep work**
- Complete the scoped experiment within available compute.
- Produce a report: question, related work, method, results, limitations and next steps.
- Clean code, configs, environment instructions and logs.
- Present findings in a short technical walkthrough.

**Evidence:** reproducible capstone repository, research-style report and 6-month continuation plan.

## 6. Parallel strands: research reading, data/cloud and communication

These run throughout the 13 weeks; they are not extra hours beyond the daily three-hour limit.

**Paper reading**
- Aim for one paper read carefully each week, not a large pile skimmed.
- For each paper: question, claim, assumptions, method, evidence, limitations, alternative explanation and one follow-up experiment.
- Prioritise papers that support the current week's concepts.

**Data/cloud/systems**
- Allocate approximately two focused blocks per week within the 3-hour schedule.
- Rotate SQL/data quality, Linux/Git/Docker, cloud storage/compute/IAM, GPU/system profiling and experiment tracking.
- Learn each concept through the active project; avoid tool collecting without a use case.

**Communication**
- Keep a dated journal entry each study day.
- At week's end, write a concise synthesis: what changed in understanding, what evidence supports it, what remains uncertain and what to do next.
- Explain one concept aloud without notes.

## 7. Candidate integrated capstone

A candidate question—not a pre-decided thesis:

**How does adding an explicit memory mechanism change an agent's ability to retain information and generalise across a sequence of tasks?**

Possible design:
- A small controlled sequence of tasks and a transparent baseline.
- Compare no-memory with one explicit memory/retrieval method.
- Measure task success, retention, adaptation, retrieval quality and generalisation.
- Ablate one memory component.
- Inspect internal representations or computations only if the chosen model/tooling permits meaningful tests.
- Avoid claiming mechanistic explanations from correlations or visualisations alone.

Keep the scope small enough for the available compute and 90-day time budget. The project may narrow after the literature review.

## 8. Evidence gates and progress labels

For each topic, record one of:
- **Not started**
- **Introduced:** can describe the problem and core vocabulary.
- **Understood:** can explain assumptions and derive/justify the central idea.
- **Implemented:** built a working minimal version.
- **Evaluated:** tested with suitable baselines and metrics.
- **Independent:** can solve a fresh problem and critique limitations without step-by-step guidance.

Do not mark a topic complete merely because a lecture or notebook was finished.

## 9. What Day 90 should mean

A successful 90 days means:
- Stronger, evidenced foundations in the mathematical and computational tools used in ML research.
- Working understanding of the full topic map, with deeper competence in selected core methods.
- Practical exposure to all four research pillars.
- At least one scoped reproduction/replication and one integrated research experiment.
- A reproducible repository, paper-style report and clear account of limitations.
- A prioritised next 3–6 month plan based on actual gaps and research evidence.

This is a serious launchpad for continued research—not mastery of every topic, a guaranteed publication or guaranteed frontier-lab employment.
