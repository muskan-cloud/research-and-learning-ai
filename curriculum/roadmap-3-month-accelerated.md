# Intelligence Lab — 90-Day Intensive Research Roadmap

**Sprint:** 9 November 2026 – 6 February 2027  
**Target effort:** 30–36 focused hours/week when sustainable; one lighter/recovery day.  
**North-star question:** How do learning systems acquire, represent, retain, and use knowledge to generalise and act?

> This is a 90-day intensive foundation-and-research sprint, not a claim that frontier AI research mastery or lab readiness can be achieved in three months. It is designed for an Applied AI Engineer with prior CS, data-science, ML and AI engineering experience. Move quickly through demonstrated strengths; spend extra time only on gaps. Protect sleep and health.

## 1. What the 90 days should achieve

By Day 90, aim to have:
- Audited and strengthened the mathematical, statistical, ML and deep-learning foundations needed for the chosen research question.
- Explored all four research pillars: learning/generalisation, mechanistic interpretability, memory/continual learning, and agentic intelligence.
- Read and critiqued a focused set of primary papers.
- Reproduced or implemented at least one scoped method/result.
- Designed and run one integrated, controlled research project with baselines, ablations and honest limitations.
- Published a reproducible repository, research-style report and next-stage research plan.

This is a strong launchpad for continued research, not a guarantee of publication, expertise or employment at a frontier lab.

## 2. Four connected research pillars

Keep all four in view; do not force premature specialisation.

1. **Learning and generalisation:** how systems acquire useful structure, generalise beyond training data and adapt.
2. **Mechanistic interpretability:** what representations and computations emerge internally, and how to test explanations causally.
3. **Memory and continual learning:** how systems retain, retrieve, update and forget information over time.
4. **Agentic intelligence:** how systems plan, reason, use tools, interact with environments and learn from feedback.

Use one unifying lens: how knowledge is learned, represented, retained and used. Investigate connections experimentally rather than assuming a single explanation.

## 3. Sprint structure

### Phase I — Compress and validate foundations (Days 1–21; 9–29 Nov)

**Week 1: accelerated diagnostic**
- Linear algebra, calculus, probability and scientific Python.
- Statistics, classical ML, evaluation and leakage-safe data workflows.
- Optimisation, gradients, PyTorch and neural-network fundamentals.
- Transformer architecture and a minimal self-attention implementation.
- Integrated practical challenge and independent checkpoint.

Familiar topics are signed off through evidence, not re-taught from scratch. Record only genuine gaps.

**Weeks 2–3: close gaps and establish experimental discipline**
- Targeted maths/statistics/optimisation revision based on diagnostic results.
- PyTorch training loop, MLP and backpropagation practice where needed.
- PCA implementation and interpretation.
- Finish the fraud-classification experiment, including feature ablation, validation-based model comparison and a clear report.
- Refresh experiment tracking, Git, tests, data versioning and reproducibility.

**Phase I evidence**
- Foundation gap map and independent checkpoint.
- PCA notebook.
- Reproducible fraud-classification experiment report.
- One paper critique.

### Phase II — Explore the four pillars and reproduce work (Days 22–56; 30 Nov–3 Jan)

**Weeks 4–5: learning, generalisation and representations**
- Empirical risk, regularisation, bias–variance and generalisation.
- Optimisation dynamics, learning curves and controlled training experiments.
- Representation learning, embeddings and feature learning.
- Read and critique work on grokking/generalisation or related learning dynamics.

**Weeks 6–7: interpretability and memory**
- Features, neurons, superposition, residual streams and attention/MLP contributions.
- Activation analysis, ablation and introductory causal interventions.
- Parametric versus external memory, retrieval, updates, forgetting and catastrophic forgetting.
- Reproduce a small, scoped interpretability or memory result using an accessible model/task.

**Phase II evidence**
- At least two structured paper critiques.
- One scoped reproduction or implementation with a baseline.
- One controlled experiment and ablation.
- A comparison note explaining what the evidence supports and what it does not.

### Phase III — Agents, integration and independent research (Days 57–90; 4 Jan–6 Feb)

**Weeks 8–9: agentic intelligence and synthesis**
- Agent loops: observe, plan, act, evaluate and recover.
- Tool use, memory, feedback and short-horizon task evaluation.
- Reliability, robustness, cost and failure analysis.
- Map connections among learning, representations, memory and agent behaviour.
- Select one narrow, testable research question based on papers and observed evidence.

**Weeks 10–12: research execution**
- State a falsifiable hypothesis and define success metrics before experiments.
- Establish simple baselines and controlled conditions.
- Run the core experiment, ablations and at least one robustness check.
- Record failed runs, negative results, uncertainty and limitations.
- Seek feedback if available; revise the analysis and report.

**Final days: package and communicate**
- Reproducible code, configurations, data notes and experiment logs.
- Research-style report with question, related work, method, results, limitations and next steps.
- Short technical presentation and a 6-month follow-on research plan.

**Phase III evidence**
- A scoped independent research project.
- Reproducible repository and report.
- A defensible explanation of findings, limitations and alternative interpretations.

## 4. Integrated capstone direction

Do not attempt four separate large projects. Build one small, controlled study that touches the pillars where technically feasible.

Possible starting question:

**How does adding an explicit memory mechanism change an agent's ability to learn and generalise across a sequence of tasks, and what evidence can we obtain about the representations or computations supporting that behaviour?**

This is a candidate question, not a pre-decided thesis. Refine it after literature review and initial experiments. Keep the scope small enough to run reliably with available compute.

Possible experimental structure:
- A simple task sequence and a transparent baseline agent/model.
- Compare no-memory and memory-enabled conditions.
- Measure task success, retention, adaptation, retrieval quality and generalisation.
- Add a small ablation to test which memory component matters.
- Inspect internal representations or behaviour only where the model/tooling supports meaningful analysis.
- Avoid claiming mechanistic explanations from correlations or visualisations alone.

## 5. Engineering foundations throughout the sprint

Reserve roughly 4–5 hours/week, increasing only when the project requires it.

- **Data:** SQL, data quality, dataset splits, leakage, pipelines and evaluation datasets.
- **Systems:** Linux, Git, Docker, testing, profiling, experiment tracking and reproducibility.
- **Cloud:** storage, compute, networking, IAM/security, deployment, monitoring and cost awareness.
- **Research infrastructure:** environments, configurations, logs, checkpoints and artifact storage.

Learn these through concrete project needs rather than collecting tools or certifications without application.

## 6. Weekly time allocation

| Workstream | Hours/week |
|---|---:|
| Mathematics and theory | 5–7 |
| Data, Python, cloud and systems | 4–5 |
| Deep learning implementation | 5–6 |
| Papers and research synthesis | 5–6 |
| Experiments and project work | 8–10 |
| Review and communication | 2–3 |
| **Total** | **30–36** |

Passive video time is not equivalent to active work. Prioritise derivations, implementation, evaluation, reading and writing. If the workload is not sustainable alongside work or health, reduce it rather than sacrificing recovery.

## 7. Research operating system

For each paper:
1. State the research question and central claim.
2. Identify assumptions, method, data and evaluation.
3. Reconstruct the key experiment or argument.
4. Record limitations and competing explanations.
5. Write one question that could lead to a testable experiment.

For each experiment:
1. State a falsifiable hypothesis.
2. Define a baseline and controlled variables.
3. Choose metrics before running it.
4. Separate training, validation and test decisions.
5. Record seeds, configurations, failures and results.
6. Run ablations and robustness checks where feasible.
7. Explain what the evidence does—and does not—support.

## 8. Evidence gates

A topic is complete when demonstrated, not merely covered:
- **Explain:** teach it clearly without notes.
- **Derive:** work through the core mathematics where applicable.
- **Implement:** build a minimal working version.
- **Evaluate:** test on a new or held-out problem with appropriate metrics.
- **Critique:** state assumptions, limitations and what evidence would change the conclusion.

At the end of each week, update the journal and experiment records. At Day 30, 60 and 90, review evidence and adjust scope transparently.

## 9. After Day 90

The 90-day sprint is a launchpad. The next stage should be determined by the evidence:
- Deepen the pillar where the strongest research question emerged.
- Improve the capstone into a more rigorous study or replication.
- Seek research mentorship, collaboration and external feedback.
- Expand the literature map and plan the next 3–6 months.

The objective is not to declare expertise in four fields after 90 days. It is to become substantially more capable of asking, testing and communicating meaningful research questions across them.
