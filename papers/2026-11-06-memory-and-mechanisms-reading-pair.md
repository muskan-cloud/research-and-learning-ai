# Memory and Mechanisms Reading Pair — 2026-11-06

This pair extends the existing Transformer/grokking foundations into two complementary questions: how neural systems retain information over long sequences, and how we can inspect the computations that produce model behaviour.

## 1. Titans: Learning to Memorize at Test Time

- **Authors:** Ali Behrouz, Peilin Zhong, Vahab Mirrokni
- **Year / venue:** 2025, *Advances in Neural Information Processing Systems 38 (NeurIPS 2025)*, Main Conference Track
- **Status:** Peer-reviewed conference paper. First arXiv version submitted 31 December 2024.
- **Canonical paper:** [NeurIPS proceedings page](https://papers.neurips.cc/paper_files/paper/2025/hash/a4ca07aa108036f80cbb5b82285fd4b1-Abstract-Conference.html)
- **Preprint:** [arXiv:2501.00663](https://arxiv.org/abs/2501.00663)
- **PDF:** [NeurIPS paper PDF](https://papers.neurips.cc/paper_files/paper/2025/file/a4ca07aa108036f80cbb5b82285fd4b1-Paper-Conference.pdf)

### Research question

Can a sequence model combine attention's precise access to a bounded context with a learned, persistent memory of earlier information—while retaining efficient training and retrieval over long sequences?

### Main contribution

The authors introduce **Titans**, a family of architectures that pair limited-window attention (treated as short-term memory) with a neural long-term memory module that learns to store and retrieve information while processing a sequence. They also introduce a separate, learned persistent-memory component for task-level information.

### Method

- The long-term memory is a neural network (an MLP in the main experiments) whose parameters are updated online at test time.
- It learns key–value associations using an associative-memory loss. The update is driven by a **surprise** signal based on gradients; a momentum-like term carries recent surprise forward.
- A data-dependent decay / weight-decay mechanism lets the memory forget information when appropriate.
- The authors design chunk-wise computations to make memory updates more parallelizable.
- They test three ways to combine memory and attention: **Memory as Context (MAC)**, **Memory as Gate (MAG)**, and **Memory as Layer (MAL)**.

### Key evidence

- The paper evaluates language modelling, common-sense reasoning, long-context retrieval, genomics, and time-series tasks, comparing against Transformer and recurrent/hybrid baselines.
- On the RULER long-context benchmark, Titans MAC reports an average score of **86.7** across the 16K–128K settings, compared with **83.2** for EM-LLM and **68.5** for the Transformer baseline reported in the same table.
- In the paper's 760M-parameter / 30B-token comparison, Titans variants report higher average common-sense reasoning accuracy than Transformer++ (52.3–52.5 versus 48.7).
- Ablations report drops when momentum, adaptive forgetting, convolution, or persistent memory are removed, suggesting these design choices contribute to the measured results.

### Limitations and cautions

- The authors explicitly leave formal guarantees about memory capacity and memory management for future work.
- Because test-time information is compressed into model parameters, the authors flag possible security, safety, and alignment risks.
- The results are benchmark- and setup-dependent; strong long-context retrieval scores do not by themselves establish robust memory, reasoning, or continual learning in every real-world setting.
- This is a neural, parameter-updating memory architecture—not the same thing as an external database, vector store, or agent memory service.

### Why it matters for the Intelligence Lab path

This is a concrete architecture-level account of remembering, updating, retrieving, and forgetting. It gives a useful bridge from attention and sequence modelling to memory mechanisms, online learning, and continual adaptation. It is especially useful for asking what a memory system should retain, how it should decide what is surprising, and how forgetting can be controlled.

### Reading questions

1. Why does the memory update use both a momentary surprise signal and a momentum-like trace of past surprise?
2. What is gained—and what might be lost—when historical information is compressed into neural-network parameters instead of kept as an explicit token sequence?
3. Which experiment would best test whether Titans' memory is robust to distribution shifts, irrelevant distractions, or conflicting information?

---

## 2. On the Biology of a Large Language Model

- **Authors:** Jack Lindsey, Wes Gurnee, Emmanuel Ameisen, Brian Chen, Adam Pearce, Nicholas L. Turner, Craig Citro, David Abrahams, Shan Carter, Basil Hosmer, Jonathan Marcus, Michael Sklar, Adly Templeton, Trenton Bricken, Callum McDougall, Hoagy Cunningham, Thomas Henighan, Adam Jermyn, Andy Jones, Andrew Persic, Zhenyi Qi, T. Ben Thompson, Sam Zimmerman, Kelley Rivoire, Thomas Conerly, Chris Olah, Joshua Batson
- **Year / date:** 2025; published online 27 March 2025
- **Status:** Anthropic / Transformer Circuits research report (non-peer-reviewed; the canonical source does not list a conference or journal venue). It is not presented as a workshop paper.
- **Canonical paper:** [Transformer Circuits Thread](https://transformer-circuits.pub/2025/attribution-graphs/biology.html)
- **Companion methods paper:** [Circuit Tracing: Revealing Computational Graphs in Language Models](https://transformer-circuits.pub/2025/attribution-graphs/methods.html)

### Research question

Can we move beyond observing a model's outputs and identify the internal features and computational pathways that help produce particular behaviours in a production-scale language model?

### Main contribution

The authors apply **circuit tracing** and attribution graphs to Claude 3.5 Haiku. Across a set of case studies, they build hypotheses about how internal features interact during reasoning, planning, multilingual processing, arithmetic, diagnosis, hallucination, refusal, and other behaviours. The paper's contribution is a collection of detailed mechanistic case studies—not a complete explanation of the model.

### Method

- The researchers use cross-layer transcoders and interpretable feature representations to approximate parts of the model's internal computation.
- They construct **attribution graphs** that trace how prompt-related features contribute to intermediate features and a selected output token.
- They then use targeted feature interventions / perturbations in selected cases to test whether the proposed intermediate mechanism affects the model's behaviour.
- The graphs are partial explanations: they are tools for generating and testing mechanistic hypotheses, not a full readout of every computation.

### Key evidence

- In a two-hop example, the model answers that Austin is the capital of the state containing Dallas. The analysis identifies an intermediate representation of **Texas** and investigates its role in producing the answer.
- In poetry examples, the model activates candidate rhyming words before completing the line, suggesting a form of forward planning in those cases.
- The authors identify both language-specific and language-independent features, and show examples of arithmetic-related circuitry being reused across different contexts.
- Other case studies examine candidate diagnoses, familiar versus unfamiliar entities, refusal behaviour, a jailbreak, and cases where the model's written chain of thought does—or does not—match the computation identified by the analysis.

### Limitations and cautions

- The authors frame the case studies as evidence that particular mechanisms exist in particular examples; they do not establish how frequently those mechanisms occur across prompts or models.
- The graphs explain only part of the computation. The companion methods paper notes that the approach does not fully explain how attention patterns are formed, and reconstruction errors can hide important computation.
- Transcoder-based explanations may not be mechanistically faithful to the original network in every case; some graph interpretations can disagree with intervention results.
- Building and interpreting graphs is labour-intensive, and the selected examples are not a systematic census of the model's behaviour.

### Why it matters for the Intelligence Lab path

This is a strong bridge from transformer internals to mechanistic interpretability. It shows how to turn a behavioural observation into a testable hypothesis about features, intermediate representations, and circuits. It also reinforces an important research habit: distinguish a plausible visual explanation from a mechanism that survives targeted intervention.

### Reading questions

1. What does an attribution graph explain, and which parts of the model's computation does it leave out?
2. In the Dallas → Texas → Austin example, what evidence supports the claim that the intermediate representation is functionally involved rather than merely correlated with the answer?
3. How should we test whether a circuit found in one prompt generalises across paraphrases, tasks, model sizes, and different model families?

---

## Suggested reading order

1. **Titans** — read the introduction and memory-update sections first. Focus on the distinction between short-term attention, learned long-term memory, persistent memory, and forgetting.
2. **On the Biology of a Large Language Model** — read the introductory Dallas → Texas → Austin case study, then inspect one further case study. Use the companion methods paper when the attribution-graph construction is unclear.

## Research hygiene

- Keep the status labels distinct: Titans is a peer-reviewed NeurIPS main-conference paper; On the Biology of a Large Language Model is a non-peer-reviewed research report.
- Treat reported benchmark scores and mechanistic case studies as evidence within their stated experimental scope, not as proof of universal capabilities.
- After reading, record one claim you can explain, one figure or method you can reconstruct, one limitation, and one experiment you would run.
