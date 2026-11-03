# Foundational Reading Pair — 2026-11-04

Two papers selected to connect current mathematical learning with the longer-term goal of understanding modern AI systems.

## 1. Attention Is All You Need

- **Authors:** Ashish Vaswani, Noam Shazeer, Niki Parmar, Jakob Uszkoreit, Llion Jones, Aidan N. Gomez, Łukasz Kaiser, Illia Polosukhin
- **Venue / year:** NeurIPS 2017
- **Canonical paper:** https://arxiv.org/abs/1706.03762
- **PDF:** https://arxiv.org/pdf/1706.03762
- **Status:** Peer-reviewed conference paper

### What question does it address?
Can sequence models for tasks such as machine translation work without recurrent or convolutional sequence-processing layers?

### Brief
The authors introduce the Transformer, an encoder–decoder architecture built around attention mechanisms. Instead of processing tokens sequentially with recurrence, self-attention lets tokens interact directly, while positional information helps represent order. The paper demonstrates strong machine-translation results and improved parallelisation compared with the recurrent/convolutional approaches of its time.

### Why read it?
This is a foundational paper behind the architecture used by modern language models. It connects linear algebra (vectors and matrices), dot products, learned projections, and optimisation to a practical neural architecture.

### Suggested reading focus
1. Understand the motivation for replacing recurrence.
2. Study scaled dot-product attention and the roles of queries, keys, and values.
3. Follow how multi-head attention uses learned projections.
4. Do not worry if every implementation detail is unclear on the first pass.

### Questions to keep in mind
- Why does attention use a query–key dot product?
- What does the softmax do to the attention scores?
- Why are multiple attention heads useful?
- What information is lost if token order is not represented?

---

## 2. Grokking: Generalization Beyond Overfitting on Small Algorithmic Datasets

- **Authors:** Alethea Power, Yuri Burda, Harri Edwards, Igor Babuschkin, Vedant Misra
- **Year:** 2022 (first posted to arXiv in January 2022; related ICLR 2021 workshop version)
- **Canonical paper:** https://arxiv.org/abs/2201.02177
- **PDF:** https://arxiv.org/pdf/2201.02177
- **Status:** arXiv preprint / workshop research

### What question does it address?
Why can a neural network continue training long after it has memorised its training set, and then suddenly begin to generalise well to unseen examples?

### Brief
The paper studies small, algorithmically generated datasets where memorisation and generalisation can be tracked clearly. In some experiments, a network first fits the training data while test performance remains poor. After substantially more optimisation, test performance can improve sharply—a phenomenon called *grokking*. The work uses controlled settings to investigate the relationship between data, optimisation, memorisation, and generalisation.

### Why read it?
It directly extends the overfitting and generalisation ideas from the recent assessment. It also opens a path toward research questions about learning dynamics: what changes inside a network before generalisation improves?

### Suggested reading focus
1. Understand the training-accuracy and test-accuracy curves.
2. Identify the difference between memorisation and generalisation.
3. Note the role of training duration and regularisation.
4. Separate the controlled experimental findings from broader claims about all neural networks.

### Questions to keep in mind
- Why does low training error not guarantee good generalisation?
- What changes during the long period before test performance improves?
- Which parts of the result depend on the synthetic task?
- What experiment could distinguish memorisation from learning a reusable rule?

---

## Suggested reading order

1. **Grokking** first: it connects to overfitting, regularisation, and generalisation already covered.
2. **Attention Is All You Need** second: use it as a first look at the Transformer, returning to the equations after more linear algebra and deep-learning foundations.

## Reading notes

After reading, add a short note for each paper:
- One idea you can explain without looking.
- One equation or figure you can reconstruct.
- One limitation or unanswered question.
- One small experiment you could run.

*These briefs are orientation notes, not substitutes for reading the papers and checking their methods and results.*
