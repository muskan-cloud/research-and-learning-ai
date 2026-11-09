# 12-Month Accelerated Intelligence Lab Roadmap

**Pace:** Aggressive  
**Target effort:** 30–36 focused hours per week, usually 5–6 hours on six study days, with one lighter/recovery day.  
**Start:** 2026-11-09  
**Purpose:** Build strong foundations, practical research skills, and a credible independent research portfolio in 12 months.

> This is an ambitious development plan, not a guarantee of frontier-lab readiness or employment. Move a milestone when its evidence is demonstrated, not just when its month ends. If work or health makes 30–36 hours unsustainable, reduce the weekly load rather than sacrificing sleep or consistency.

## Operating model: three parallel tracks from Month 1

Do not postpone research until the foundations are "finished". Every month includes all three tracks:

1. **Foundations and engineering:** mathematics, Python, data handling, ML, deep learning, and cloud basics.
2. **Research:** primary-paper reading, paper critique, research questions, and literature mapping.
3. **Experiments:** notebooks, reproductions, ablations, evaluations, and clear experiment records.

### Suggested weekly allocation (30–36 focused hours)

| Workstream | Hours/week | What it includes |
|---|---:|---|
| Mathematics and theory | 7–8 | Derivations, problem sets, statistics, ML theory |
| Data, Python, and cloud engineering | 5–6 | NumPy, pandas, SQL, data pipelines, Git, Linux, cloud fundamentals |
| Deep learning implementation | 5–6 | PyTorch, training loops, models, debugging |
| Research papers and synthesis | 4–5 | 1–2 papers deeply, notes, comparisons, questions |
| Experiments and research project | 7–8 | Replication, controlled experiments, ablations, evaluation |
| Review and communication | 2–3 | Journal, weekly review, short technical explanations |
| **Total** | **30–36** | |

A practical day can be split into two or three focused blocks. Take breaks between blocks and protect at least one lighter day. Do not count passive video time as equivalent to problem-solving or implementation.

## Month-by-month plan

### Month 1 — Mathematical and coding foundations

**Focus**
- Linear algebra: vectors, matrices, projections, eigenvalues/eigenvectors, PCA intuition.
- Calculus: derivatives, partial derivatives, chain rule, gradients.
- Probability and statistics: distributions, expectation, variance, conditional probability, Bayes' rule.
- Python for scientific computing: NumPy, pandas, plotting, notebooks, testing, Git.
- Data basics: tabular data, missing values, leakage, train/validation/test splits.

**Research thread:** Read foundational papers alongside the relevant concepts; practise identifying claims, assumptions, methods, and limitations.

**Deliverables**
- Implement linear regression and gradient descent from scratch.
- Implement PCA on a small dataset and inspect explained variance and loadings.
- Complete an independent mathematics checkpoint.
- Publish two paper notes and one reproducible notebook.

### Month 2 — Statistics, optimisation, and classical ML

**Focus**
- Likelihood, maximum likelihood estimation, cross-entropy.
- Optimisation: SGD, momentum, learning-rate schedules, conditioning.
- Generalisation, regularisation, bias–variance, cross-validation.
- Classification metrics, calibration, ROC/PR curves, threshold selection.
- SQL and practical data workflows; introductory cloud storage, compute, IAM, and deployment concepts.

**Deliverables**
- End-to-end classification project with leakage-safe evaluation.
- Compare at least three baselines and document error analysis.
- Explain and implement precision, recall, F1, and confusion matrices.
- Write a short report on generalisation and evaluation choices.

### Month 3 — Statistical learning theory and experimental discipline

**Focus**
- Empirical risk minimisation, model capacity, VC/PAC intuition.
- Sampling, confidence intervals, hypothesis tests, uncertainty.
- Experimental design, controls, reproducibility, seeds, data versioning.
- PyTorch tensors, autograd, datasets, dataloaders, training loops.

**Deliverables**
- Reproduce a small classical ML result.
- Build a clean experiment template with configs, metrics, and saved artefacts.
- Write a paper critique and a one-page experiment proposal.

### Month 4 — Neural networks from first principles

**Focus**
- Perceptrons, MLPs, activations, loss functions.
- Backpropagation and automatic differentiation.
- Initialisation, normalisation, regularisation, optimisation.
- Representation learning and embeddings.

**Deliverables**
- Implement a small MLP from scratch with NumPy.
- Train and evaluate an equivalent PyTorch model.
- Explain the computational graph and gradients independently.

### Month 5 — Transformers and language modelling

**Focus**
- Tokenisation, embeddings, positional information.
- Queries, keys, values, scaled dot-product attention.
- Multi-head attention, residual streams, normalisation, MLP blocks.
- Autoregressive language modelling, training objectives, evaluation.

**Deliverables**
- Implement self-attention and a minimal transformer block.
- Train a small character- or token-level language model.
- Produce a technical walkthrough with limitations.

### Month 6 — Deep learning systems and a first replication

**Focus**
- Training stability, data quality, batching, efficient experimentation.
- GPU basics, memory, profiling, mixed precision concepts.
- Experiment tracking and cloud fundamentals: compute/storage/networking/security basics.
- Reproducibility and baseline selection.

**Deliverables**
- Reproduce a modest published result or a clearly scoped component of one.
- Run at least one ablation and report uncertainty and limitations.
- Publish code, environment details, and experiment logs.

### Month 7 — Learning dynamics and generalisation

**Focus**
- Grokking, delayed generalisation, double descent.
- Loss landscapes and optimisation trajectories.
- Feature learning versus kernel-like behaviour.
- Scaling laws: empirical patterns, assumptions, and limits.

**Deliverables**
- Run a controlled learning-dynamics experiment on a small synthetic task.
- Vary at least two factors (for example, weight decay and training duration).
- Plot training and test behaviour; explain alternative interpretations.

### Month 8 — Mechanistic interpretability

**Focus**
- Features, neurons, distributed representations, superposition.
- Sparse autoencoders and feature dictionaries.
- Activation patching, causal interventions, attribution graphs.
- Interpretability evaluation and common failure modes.

**Deliverables**
- Complete a small interpretability investigation on an accessible model.
- State a falsifiable question, method, controls, and limitations.
- Write a concise research-style report.

### Month 9 — Memory and continual learning

**Focus**
- Parametric versus external memory.
- Retrieval, associative memory, memory updates and forgetting.
- Catastrophic forgetting, replay, regularisation, parameter isolation.
- Online and continual learning; test-time adaptation.

**Deliverables**
- Build a controlled continual-learning or memory benchmark.
- Compare at least two methods against a simple baseline.
- Evaluate retention, adaptation, retrieval quality, and failure cases.

### Month 10 — Research question and proposal

**Focus**
- Map a narrow literature area across primary sources.
- Identify a tractable gap; separate novelty from implementation.
- Form falsifiable hypotheses and operationalise metrics.
- Design baselines, controls, ablations, and compute budget.

**Deliverables**
- A focused literature map.
- A 2–4 page research proposal.
- A preregistered-style experiment plan with risks and fallback options.

### Month 11 — Independent research execution

**Focus**
- Run experiments systematically.
- Track failed runs, negative results, and uncertainty.
- Perform ablations and robustness checks.
- Seek external feedback and revise the design.

**Deliverables**
- A reproducible experiment package.
- Results with appropriate comparisons and uncertainty.
- A draft report with clear limitations.

### Month 12 — Research portfolio and next-stage plan

**Focus**
- Consolidate related work, methods, findings, and limitations.
- Improve code quality, documentation, and reproducibility.
- Prepare a technical presentation and research discussion.
- Identify the next 6–12 month research direction and relevant groups.

**Deliverables**
- One substantial public research project or paper-style technical report.
- Reproducible code, configurations, data notes, and experiment logs.
- A concise research portfolio and follow-up proposal.

## Monthly evidence gates

A month is complete only when its deliverables exist and can be checked. For each major topic, aim to demonstrate:

1. **Explain:** Teach the idea clearly without notes.
2. **Derive:** Work through the core mathematics where applicable.
3. **Implement:** Build a minimal working version.
4. **Evaluate:** Test it on fresh data or a new problem.
5. **Critique:** State assumptions, limitations, and what evidence would change your view.

If a gate is missed, carry the gap forward and adjust scope. Do not hide gaps by marking topics complete.

## Weekly operating loop

- **Start of week:** Choose one core concept, one paper, and one experiment objective.
- **During the week:** Alternate theory, implementation, and research reading; write down questions as they arise.
- **End of week:** Solve a fresh problem without hints, review experiment results, update the journal and dashboard, and choose the next objective.

## First 2-week sprint (starting 2026-11-09)

1. Finish the current PCA and classification-evaluation foundations.
2. Independently calculate confusion matrices, precision, recall, specificity, and F1.
3. Implement PCA on a small dataset; inspect explained variance and feature loadings.
4. Build a leakage-safe fraud-classification baseline and compare models with and without selected components.
5. Read one paper deeply and write a structured critique.
6. Record code, results, limitations, and unresolved questions in the repository.

## What success after 12 months means

Success means demonstrated ability to:
- Understand and derive core ML and deep-learning ideas.
- Build and evaluate models with sound data and experimental practices.
- Read research papers critically.
- Reproduce a scoped result and explain discrepancies.
- Form a testable research question and execute a defensible experiment.
- Communicate results with code and evidence others can inspect.

This is a strong launchpad for applying to research-oriented roles, collaborating with research teams, or continuing toward frontier AI research. It does not guarantee entry into a particular lab; research depth, project quality, collaboration, and opportunity also matter.
