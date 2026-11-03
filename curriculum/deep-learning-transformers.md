# Deep Learning and Transformers

## Learning objective

Understand neural networks as parameterised computational systems, including their training dynamics and internal information flow.

## Core sequence

### Neural networks
- Perceptrons and multilayer perceptrons.
- Activation functions and expressive capacity.
- Forward propagation and computational graphs.
- Backpropagation and automatic differentiation.
- Initialisation, normalisation, and regularisation.
- Optimisers and training stability.

### Representation learning
- Embeddings and learned feature spaces.
- Distributed representations.
- Feature learning and invariances.
- Latent spaces and dimensionality reduction.

### Transformers
- Query, key, and value projections.
- Scaled dot-product attention.
- Multi-head attention.
- Positional information.
- Residual streams and layer normalisation.
- Feed-forward blocks.
- Causal masking and autoregressive objectives.
- Pretraining and next-token prediction.

## Implementation milestones

1. Train a tiny multilayer perceptron on a synthetic dataset.
2. Implement backpropagation for a small network.
3. Build a minimal self-attention layer.
4. Assemble a small transformer block.
5. Train a tiny language model on a small, documented corpus.
6. Inspect activations and attention patterns without assuming that attention weights alone explain model reasoning.

## Exit criteria

Trace data through a transformer, explain the role of each major component, and reproduce a small training run with documented configuration and limitations.
