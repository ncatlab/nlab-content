
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The *posetal reflection* of a [[preorder]] is the [[poset]] obtained by enforcing antisymmetry by quotienting out [[isomorphisms]].

## Construction

Let $(A, \leq)$ be a [[preorder]]. Define the [[equivalence relation]]:
\[
a \simeq b \quad\text{iff}\quad a \leq b \ \text{and}\ b \leq a.
\]
The corresponding posetal reflection $A'$ of $A$ is the preorder on the [[quotient]] $A/\simeq$ given by
\[
[a] \leq' [b] \quad\text{iff}\quad a \leq b
\]
It's easy to show both $\simeq$ and $\leq'$ are well-defined.

Abstractly, the correspondence $(A, \leq) \mapsto (A', \leq')$ is [[functor|functorial]] from preorders to posets, and in fact exhibits [[Pos]] as a [[reflective subcategory]] of preorders (hence the name).
