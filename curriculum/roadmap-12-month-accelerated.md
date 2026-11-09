# Intelligence Lab — 12-Month Accelerated Research Roadmap

**Start:** 2026-11-09  
**Target pace:** 30–36 focused hours/week when sustainable; one lighter/recovery day.  
**North-star question:** How does intelligence emerge, adapt, remember, and generalise in learning systems?

> This roadmap is designed for an Applied AI Engineer with prior computer-science, data-science, ML, and AI engineering experience—not a beginner. The first week is a fast-track diagnostic of familiar foundations, not a promise that every topic can be mastered in seven days. Pass demonstrated skills quickly; spend extra time only on gaps. Milestones are evidence-based, not calendar-based. Protect sleep and health; reduce workload rather than forcing the target hours.

## 1. Research identity: broad first, specialised later

The user has chosen to explore **all four** directions. Keep them connected throughout the year rather than treating them as isolated specialisations.

1. **Learning and generalisation:** How do models acquire useful structure, generalise beyond training data, and adapt?
2. **Mechanistic interpretability:** What representations and computations emerge inside neural networks, and how can we test causal explanations?
3. **Memory and continual learning:** How do systems retain, retrieve, update, and forget information over time?
4. **Agentic intelligence:** How do systems plan, reason, use tools, interact with environments, and learn from feedback?

**Unifying lens:** study the learning process, inspect the internal representations, test memory and adaptation, and evaluate behaviour in interactive settings. Do not assume these areas have one simple explanation; use experiments to discover where they connect and where they differ.

## 2. Three parallel workstreams

Every phase includes all three:

- **Foundations and engineering:** mathematics, statistics, Python, data, PyTorch, systems, cloud and reproducibility.
- **Research and synthesis:** primary papers, careful critique, literature maps, hypotheses and research questions.
- **Experiments:** implementations, baselines, replications, ablations, evaluation and written results.

### Suggested weekly allocation

| Workstream | Hours/week | Examples |
|---|---:|---|
| Mathematics and theory | 6–7 | Derivations, probability, optimisation, learning theory |
| Data, Python, cloud and systems | 4–5 | SQL, data pipelines, Linux, Git, cloud storage/compute/IAM |
| Deep learning implementation | 5–6 | PyTorch, models, training, debugging |
| Papers and research synthesis | 5–6 | 1–2 papers deeply, notes, comparisons |
| Experiments and project work | 8–9 | Replication, ablations, benchmarks, evaluation |
| Review and communication | 2–3 | Research journal, weekly review, technical explanations |
| **Total** | **30–36** | |

Passive video time is not equivalent to active problem-solving. Prefer building, deriving, testing and explaining.

## 3. Week 1 — accelerated foundations diagnostic (9–15 November 2026)

This week tests existing knowledge across the first five foundation areas. It is a readiness sprint, not a race to watch five courses.

| Day | Focus | Evidence |
|---|---|---|
| 1 | Linear algebra, calculus, probability, scientific Python | Solve representative problems and explain core operations |
| 2 | Statistics, classical ML, metrics and evaluation | Analyse a dataset and justify a leakage-safe evaluation |
| 3 | Optimisation, generalisation and PyTorch basics | Explain loss/gradients and build a small training loop |
| 4 | Neural networks and backpropagation | Trace gradients and train a small MLP |
| 5 | Transformers and language modelling | Explain and implement a minimal self-attention block |
| 6 | Integrated practical challenge | Complete a small end-to-end implementation and evaluation |
| 7 | Independent checkpoint and gap map | Demonstrate what is already strong and list only the gaps that need work |

**Pass rule:** for each topic, demonstrate the relevant combination of explain, derive, implement, evaluate and critique. Familiar topics can be signed off quickly. Do not claim mastery from recognition or video completion alone.

## 4. Month-by-month roadmap

### Month 1 — readiness, foundations audit and clean experimentation (9 Nov–8 Dec 2026)

**Focus**
- Complete the Week 1 diagnostic.
- Close only the gaps exposed by the assessment.
- Finish the current fraud-classification experiment, including feature ablation and a clear report.
- Implement PCA and interpret explained variance and component loadings.
- Refresh Git, testing, experiment organisation and data-leakage discipline.

**Deliverables**
- Foundation diagnostic with evidence and a targeted gap list.
- Reproducible fraud-classification notebook and concise experiment report.
- PCA implementation and interpretation.
- One structured research-paper critique.

### Month 2 — learning theory, optimisation and generalisation (9 Dec 2026–8 Jan 2027)

**Focus**
- Empirical risk minimisation, regularisation and model capacity.
- Generalisation, bias–variance, cross-validation and uncertainty.
- SGD, momentum, learning-rate schedules, conditioning and loss landscapes.
- Introductory statistical learning theory: VC/PAC intuition and limits.
- Design controlled experiments and distinguish correlation from causal evidence.

**Research connection:** why do models generalise, and what changes during training?

**Deliverables**
- Implement and compare optimisation methods on controlled tasks.
- Run a small generalisation experiment with baselines and ablations.
- Explain results, uncertainty and alternative interpretations.

### Month 3 — neural learning and representations (9 Jan–8 Feb 2027)

**Focus**
- PyTorch fluency: tensors, autograd, datasets, dataloaders and training loops.
- MLPs, backpropagation, initialisation, normalisation and regularisation.
- Embeddings and representation learning.
- Feature learning versus kernel-like behaviour at an introductory level.

**Research connection:** what representations do networks learn, and how do those representations change?

**Deliverables**
- Implement an MLP from first principles and in PyTorch.
- Compare learned representations across controlled settings.
- Produce a technical note with visualisations and limitations.

### Month 4 — transformers and language modelling (9 Feb–8 Mar 2027)

**Focus**
- Tokenisation, embeddings and positional information.
- Queries, keys, values, attention and multi-head attention.
- Residual streams, normalisation and MLP blocks.
- Autoregressive language modelling, objectives and evaluation.
- Training dynamics in small language models.

**Research connection:** how do transformer architectures learn useful internal structure?

**Deliverables**
- Implement self-attention and a minimal transformer block.
- Train a small language model.
- Document its behaviour, evaluation and failure cases.

### Month 5 — mechanistic interpretability foundations (9 Mar–8 Apr 2027)

**Focus**
- Features, neurons, superposition and distributed representations.
- Residual stream and attention/MLP contributions.
- Activation analysis and feature visualisation.
- Sparse autoencoders and feature dictionaries: motivation and caveats.
- Interpretability as a set of testable hypotheses, not attractive visualisations.

**Research connection:** what internal features and computations support model behaviour?

**Deliverables**
- Reproduce a small interpretability analysis on an accessible model.
- Form a falsifiable hypothesis about a feature or circuit.
- Write a short report that includes controls and limitations.

### Month 6 — causal and mechanistic investigations (9 Apr–8 May 2027)

**Focus**
- Activation patching and causal interventions.
- Ablation, attribution and circuit-level hypotheses.
- Feature interactions and evaluation of explanations.
- Common pitfalls: spurious explanations, dataset dependence and incomplete causal evidence.

**Deliverables**
- Run a scoped causal intervention experiment.
- Compare at least two explanations or methods.
- Publish reproducible code and a research-style report.

### Month 7 — memory and continual learning (9 May–8 Jun 2027)

**Focus**
- Parametric versus external memory.
- Retrieval, associative memory, memory updates and forgetting.
- Catastrophic forgetting, replay, regularisation and parameter isolation.
- Online learning, continual learning and test-time adaptation.
- Metrics for retention, adaptation, interference and retrieval quality.

**Research connection:** how can a model acquire new knowledge without losing useful old knowledge?

**Deliverables**
- Build a controlled continual-learning or memory benchmark.
- Compare at least two methods with a simple baseline.
- Analyse retention, adaptation and failure cases.

### Month 8 — agentic intelligence (9 Jun–8 Jul 2027)

**Focus**
- Agent loops: observe, reason, plan, act and evaluate.
- Tool use, planning, search and feedback.
- Short- and long-horizon task evaluation.
- Agent memory, state, context management and learning from interaction.
- Reliability, robustness, safety boundaries and cost/latency trade-offs.

**Research connection:** what capabilities emerge from interaction, memory and feedback—and how do we measure them?

**Deliverables**
- Build a small controlled agent environment or benchmark.
- Compare a baseline agent with a memory, planning or feedback intervention.
- Evaluate task success, generalisation, tool errors and recovery.

### Month 9 — intersections: learning × representations × memory × agency (9 Jul–8 Aug 2027)

**Focus**
- Identify connections among the four pillars using evidence from prior experiments.
- Study how representations support memory and how memory changes adaptation.
- Examine whether agent feedback improves learning or merely changes task execution.
- Design multi-factor experiments with controls and ablations.

**Deliverables**
- A small integrated benchmark or experiment.
- A comparison of at least two mechanisms or interventions.
- A shortlist of 2–3 research questions supported by literature and observed evidence.

### Month 10 — literature map and research proposal (9 Aug–8 Sep 2027)

**Focus**
- Narrow the broad interest to a tractable question.
- Map primary literature and identify competing explanations.
- Separate a genuinely open question from an implementation exercise.
- Define hypotheses, metrics, baselines, controls, compute budget and risks.

**Deliverables**
- Focused literature map across relevant pillars.
- A 2–4 page research proposal.
- A reproducible experiment plan with success criteria and fallback options.

### Month 11 — independent research execution (9 Sep–8 Oct 2027)

**Focus**
- Run the planned experiments systematically.
- Track negative results, failures, uncertainty and deviations.
- Perform ablations, robustness checks and error analysis.
- Seek informed feedback and revise the design.

**Deliverables**
- Reproducible experiment package.
- Results with meaningful baselines and limitations.
- Draft paper-style report.

### Month 12 — research portfolio and next-stage direction (9 Oct–8 Nov 2027)

**Focus**
- Consolidate the question, related work, methods, results and limitations.
- Improve code, documentation, reproducibility and communication.
- Prepare a technical presentation and research discussion.
- Choose the next 6–12 month research direction based on evidence and feedback.

**Deliverables**
- One substantial public research project or paper-style report.
- Reproducible code, configurations, data notes and experiment logs.
- Research portfolio and next-stage proposal.

## 5. Ongoing engineering foundation: data and cloud

Data and cloud are enabling skills, not a separate detour. Keep a small weekly allocation throughout the year.

- **Data:** SQL, data modelling, data quality, dataset versioning, pipelines, leakage, efficient processing and evaluation datasets.
- **Systems:** Linux, Git, Docker, testing, experiment tracking, profiling and reproducibility.
- **Cloud:** storage, compute, networking, IAM/security, deployment, monitoring and cost awareness.
- **Research infrastructure:** reproducible environments, configuration management, logging, checkpoints and artifact storage.

Increase depth when an experiment requires it. Avoid collecting cloud certifications or services without a concrete engineering use case.

## 6. Research operating system

For every paper:
1. State the research question and central claim.
2. Identify assumptions, method, data and evaluation.
3. Reconstruct the key experiment or argument.
4. Record limitations and competing explanations.
5. Write one question that could lead to a testable experiment.

For every experiment:
1. State a falsifiable hypothesis.
2. Define a baseline and controlled variables.
3. Choose metrics before running the experiment.
4. Separate training, validation and test decisions.
5. Record seeds, configurations, failures and results.
6. Run ablations and robustness checks where feasible.
7. Explain what the evidence does—and does not—support.

## 7. Evidence gates

A topic is complete when the evidence supports it, not when its calendar slot ends.

- **Explain:** teach the concept clearly without notes.
- **Derive:** work through the core mathematics where applicable.
- **Implement:** build a minimal working version.
- **Evaluate:** test on a new or held-out problem with appropriate metrics.
- **Critique:** state assumptions, limitations and what evidence would change the conclusion.

At the end of each month, update the learning journal, experiment records and progress dashboard. Carry unresolved gaps forward transparently.

## 8. Weekly operating loop

- **Start:** choose one core concept, one paper and one experiment objective.
- **During:** alternate theory, implementation and research reading; keep a question log.
- **End:** solve a fresh problem without hints, review experiment evidence, write a concise weekly synthesis and choose the next objective.

## 9. What success after 12 months means

Success means demonstrating the ability to:
- Understand and derive important ML and deep-learning concepts.
- Build and evaluate models with sound data and experimental practices.
- Read and critique research papers.
- Reproduce a scoped result and explain discrepancies.
- Investigate learning, representations, memory and agentic behaviour using controlled experiments.
- Form a defensible research question and execute a reproducible study.
- Communicate findings with code and evidence others can inspect.

This roadmap is a strong launchpad for research-oriented roles, collaborations and further study. It does not guarantee entry into a particular lab. Research depth, project quality, mentorship, collaboration and opportunity also matter.
