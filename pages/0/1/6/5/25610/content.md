## Idea
The posetal reflection of a [[preorder]] is the [[poset]] obtained by enforcing antisymmetry by quotienting out [[isomorphisms]].

## Construction
Formally, let $(A, \leq)$ be a preorder. Define the equivalence relation:
\[
a \simeq b \quad\text{iff}\quad a \leq b \ \text{and}\ b \leq a.
\]
Then the posetal reflection $A'$ of $A$ is the preorder on the quotient $A/\simeq$ given by
\[
[a] \leq' [b] \quad\text{iff}\quad a \leq b
\]
It's easy to show both $\simeq$ and $\leq'$ are well-defined.

Abstractly, the correspondence $(A, \leq) \mapsto (A', \leq')$ is functorial from preorders to posets, and in fact exhibits posets as a [[reflective subcategory]] of preorders (hence the name).
