The notion of fibration theory was created by James Wirth in his PhD thesis in 1965. It allows classification of what would now be called $\infty$-[[principal infinity-bundle|bundles]].


### The axioms ###

A *fibration theory* $E$ is an assignment of a [[category]] $E(B)$ to each [[topological space]] $B$ and a [[contravariant functor]] $f^*:E(C) \to E(B)$ to each continuous map $f:B \to C$ such that $id^*$ is the [[identity functor]]. $E$ is required to satisfy the following

1. For a [[numerable open cover]] $U = \coprod U_i$ of a space $B$ and a system of objects (morphisms) $E_i$ over each $U_i$ such that $E_i$ and $E_j$ agree over $U_i\cap U_j$, then there is a unique common extension of the $E_i$ over $B$

1. If $\phi$ is a morphism in $E(B)$ such that each restriction $\phi|_{U_i}$ for a numerable open cover $U$ of $B$ is a [[homotopy equivalence]], then $\phi$ is a homotopy equivalence. If $H\in E(I\times B)$, then the restrictions $H|_{\{t\}\times B}$ are homotopy equivalent (for objects) or homotopic (for morphisms)

1. (Mapping cylinder axiom) If $\phi:F \to F' \in E(B)$ is a homotopy equivalence, then there is an object $M(\phi)\in E(I\times B)$ which serves as a *mapping cylinder* for $\phi$. That is, $M(\phi)$ restricts to $F$ at $t=0$ and to $F'$ at $t=1$ with a characterising homotopy equivalence $\psi_M:M(\phi) \to I\times F'$ which restricts to $\{0\}\times\phi$, respectively $\{1\}\times id$.

## References

Original PhD thesis:

* James Frederick Wirth. Fiber spaces and the higher homotopy cocycle relations. PhD thesis, University
of Notre Dame, 1965.

Modern treatment:

* James Wirth, [[Jim Stasheff]], _Homotopy transition cocycles_ J. Homotopy Relat. Struct., 1(1):273–283, 2006.  [EuDML](https://eudml.org/doc/128360), [arXiv](https://arxiv.org/abs/math/0609220).

