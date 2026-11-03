# Learning Progress Dashboard

> Updated: 2026-11-03  
> Tracking rule: a topic is not marked mastered just because it was explained. Mastery requires an independent explanation, a derivation or implementation, and a fresh problem without step-by-step help.

## Current position

| Field | Current status |
|---|---|
| Learning track | Mathematical foundations → calculus and optimisation |
| Current module | Derivatives, gradients, chain rule, and backpropagation |
| Current lesson | Session 01 — guided baseline and foundations |
| Overall status | In progress |
| Next checkpoint | Explain and calculate a complete chain-rule gradient independently |

## Topic tracker

| Topic | Status | Evidence so far | Next action |
|---|---|---|---|
| Derivatives | Practised with guidance | Differentiated (x^2); evaluated derivatives at given values | Solve a fresh set independently |
| Gradients | Practised with guidance | Interpreted positive and negative gradients; connected sign to direction of change | Explain gradient geometrically and solve fresh examples |
| Gradient descent | Practised with guidance | Updated scalar and two-variable weights using a learning rate | Implement a simple optimiser from scratch |
| Partial derivatives | Practised with guidance | Calculated partial derivatives for (3x^2+2y^2) | Practise with a new multivariable function |
| Chain rule | Practised with guidance | Applied local derivatives across multi-step expressions | Derive a new composite function independently |
| Computational graphs | Introduced and practised | Traced (w \rightarrow a \rightarrow b \rightarrow L) in two examples | Draw a graph for a small neural-network layer |
| Backpropagation | Introduced; understanding developing | Multiplied local derivatives backwards to obtain (dL/dw) | Explain why gradients flow backwards and complete a fresh example |
| Numerical gradient checking | Not started | — | Implement finite-difference checks |
| Jacobians and Hessians | Not started | — | Study after multivariable chain rule |

## Latest worked example

Given:

```
a = wx
b = a + 5
L = b²
x = 2, w = 3
```

Forward pass:
- (a = 6)
- (b = 11)
- (L = 121)

Backward pass:
- (dL/db = 22)
- (db/da = 1)
- (da/dw = 2)
- (dL/dw = 22 \times 1 \times 2 = 44)

Interpretation: the positive gradient means a small increase in (w) increases the loss locally. Gradient descent therefore updates in the negative-gradient direction.

## Learning observations

- Correctly computed several derivatives and gradient-descent updates during guided practice.
- Correctly identified the dependency chain in computational-graph examples.
- Needed clarification that backpropagation traces how the final loss depends on earlier weights; it is not the loss itself travelling through the network.
- Current evidence shows promising guided understanding, but independent mastery has not yet been established.

## Next session

1. Revisit the chain rule without hints.
2. Draw a computational graph from a short sequence of equations.
3. Calculate all local derivatives and combine them.
4. Explain the sign and magnitude of the final gradient.
5. Introduce a small neural-network example only after the above is secure.

## Progress history

| Date | Session | Result |
|---|---|---|
| 2026-11-03 | Session 01 — calculus, optimisation, and backpropagation foundations | Guided practice completed; independent checkpoint pending |

## Evidence policy

Use these status labels consistently:
- **Not started** — no meaningful study yet.
- **Introduced** — concept explained, but little practice.
- **Practised with guidance** — solved examples with prompts or hints.
- **Practised independently** — solved fresh problems without step-by-step help.
- **Mastered** — can explain, derive, apply, and transfer the concept to a new setting.
