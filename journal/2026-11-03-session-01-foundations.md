# Session 01 — Calculus, Optimisation, and Backpropagation Foundations

**Date:** 2026-11-03  
**Track:** Mathematical foundations  
**Format:** Guided concept lesson and worked problems

## Topics covered

- Derivatives and evaluating derivatives at a point.
- Gradient as the direction of steepest increase.
- Gradient descent as movement opposite the gradient.
- Scalar and multivariable gradient-descent updates.
- Partial derivatives.
- Chain rule for composite functions.
- Computational graphs and forward/backward passes.
- Introductory backpropagation.

## Worked evidence

### Gradient descent

For (L(w)=w^2), with (w=2) and learning rate (0.1):
- Gradient: (dL/dw=4).
- Updated weight: (w_{new}=2-0.1(4)=1.6).

For (L(w_1,w_2)=w_1^2+w_2^2), starting at ((2,3)) with learning rate (0.1):
- Gradients: ((4,6)).
- Updated weights: ((1.6,2.4)).

### Chain rule

For (y=wx) and (L=(y-10)^2), with (x=2,w=3):
- Prediction (y=6), loss (L=16).
- Gradient (dL/dw=2(y-10)x=-16).
- With learning rate (0.1), updated weight (w=4.6).

### Multi-step computational graph

For (a=wx), (b=a+5), (L=b^2), with (x=2,w=3):
- Forward: (a=6, b=11, L=121).
- Backward: (dL/db=22, db/da=1, da/dw=2).
- Combined gradient: (dL/dw=22\times1\times2=44).

## What went well

- Correctly evaluated derivatives and gradients in the guided examples.
- Correctly updated weights using gradient descent.
- Correctly calculated partial derivatives in a two-variable loss.
- Correctly traced the dependency path (w\rightarrow a\rightarrow b\rightarrow L).
- Correctly combined local derivatives using the chain rule in the final example.

## Concepts to revisit

- The gradient points in the direction of steepest local increase; gradient descent moves in the opposite direction.
- Backpropagation computes how the final loss depends on earlier parameters by applying the chain rule backwards through the computational graph.
- A positive gradient indicates that a small increase in the parameter increases the loss locally; a negative gradient indicates the opposite.

## Assessment

This was guided practice, not a formal mastery test. The learner showed good progress with worked examples and conceptual prompts. A fresh independent problem set is needed before marking these topics as independently practised or mastered.

## Next steps

1. Solve a new chain-rule problem without hints.
2. Explain a computational graph in the learner's own words.
3. Implement gradient descent for a simple scalar loss.
4. Compare analytical gradients with finite-difference estimates.
