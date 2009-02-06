A Grothendieck pretopology is a collection of maps in a category which can be considered as [[cover|covers]]. It is sometimes known as a ''basis for a [[Grothendieck topology]]'', as a pretopology generates a Grothendieck topology. Note that different pretopologies can generate the same Grothendieck topology.

The prototype is the pretopology consisting of open covers of a topological space/manifold. Other pretopologies on $Top$ include:

* Local-section-admitting surjections
* Surjective open maps
* [[Topological submersion]]s
* Surjective local homeomorphisms

All of these have covering families consisting of single arrows.
(David Roberts says: I propose some sort of name for this property, since it is common around here. How about ''singleton pretopology''?)

(Other examples ..)


An example for the category of manifolds is the pretopology of surjective submersions.



##Definition##

Let $S$ be a category. A _Grothendieck pretopology_ is a collection of families $\{\{U_i \to A\}_{i\in I}\}$, called covering families, for each object $A$, satisfying the following conditions:

* If $A' \to A$ is an isomorphism, then $\{A' \to A\}$ is a covering family,

* Given a covering family $\{U_i \to A\}_{i\in I}$ and a map $B \to A$, the pullbacks $B \times_A U_i$ exist and $\{B \times_A U_i \to B\}_{i\in I}$ is a covering family,

* Given a covering family $\{U_i \to A\}_{i\in I}$ and for each $i \in I$ a covering family $\{V_ij \to U_i\}_{j\in J_i}$, then $\{V_ij \to A\}_{j\in J_i,i\in I}$ is a covering family.



