<div class="rightHandSide toc">
[[!include monoidal categories - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

## Definition

A **rigid monoidal category**, also called an **autonomous monoidal category**, is a [[monoidal category]] where every [[object]] has [[dualizable object|duals]] on both sides.  If only one type of dual exists, we speak of **left rigid** (or autonomous) or **right rigid** categories.

Conventions differ regarding which type of duals are which.  One convention is as follows: a _right dual_ of an object $V$ in a monoidal category is an object $V^*$ equipped with unit $\eta : 1 \rightarrow V^* \otimes V$ and counit maps $\epsilon: V \otimes V^* \rightarrow 1$ satisfying the [[triangle identities]] (the snake diagrams), while a left dual is is the dual notion.  This convention fits in with the standardized conventions regarding [[adjoint functor]]s: anendofunctor $F : C \rightarrow C$ has a right adjoint $F^* : C \rightarrow C$ if and only if $F^*$ is a right dual of $F$ in the [[monoidal category]] $End(C)$. 

## Remarks

Note that this definition only asserts the existence of the dual objects. It does _not_ assert that specific duals have been chosen.

Nor does it assert that the right dual of an object is isomorphic to its left dual: this need not be the case in general, though it is true in a [[braided monoidal category]], and thus automatically also in a [[symmetric monoidal category]].  A rigid monoidal category which is also symmetric is sometimes called [[compact closed category|compact closed]] or simply "compact".

In practice, algebraic geometers are the most frequent users of the term 'rigid', and they focus on the symmetric monoidal case, so they ignore the difference between right and left duals.

[[!redirects rigid monoidal categories]]
[[!redirects autonomous monoidal category]]
[[!redirects autonomous category]]
[[!redirects autonomous monoidal categories]]
[[!redirects autonomous categories]]
