A Grothendieck pretopology is a collection of families of maps in a category which can be considered as [[cover|covers]].  It is sometimes known as a ''basis for a [[Grothendieck topology]]'', as a pretopology generates a Grothendieck topology.  Note that different pretopologies can generate the same Grothendieck topology.

An even weaker notion than a Grothendieck pretopology, which also generates a Grothendieck toplogy, is a [[coverage]].  A Grothendieck pretopology can be defined as a coverage that also satisfies a couple of extra saturation conditions.


##Definition##

Let $S$ be a category. A __Grothendieck pretopology__ is a collection of families $\{\{U_i \to A\}_{i\in I}\}$, called covering families, for each object $A$, satisfying the following conditions:

* If $A' \to A$ is an isomorphism, then $\{A' \to A\}$ is a covering
family,

* Given a covering family $\{U_i \to A\}_{i\in I}$ and a map $B \to
A$, the pullbacks $B \times_A U_i$ exist and $\{B \times_A U_i \to
B\}_{i\in I}$ is a covering family,

* Given a covering family $\{U_i \to A\}_{i\in I}$ and for each $i \in
I$ a covering family $\{V_ij \to U_i\}_{j\in J_i}$, then $\{V_ij \to
A\}_{j\in J_i,i\in I}$ is a covering family.

If we drop the first and third conditions, we obtain the notion of a [[coverage]]; conversely every coverage generates a Grothendieck pretopology by an evident closure process.  However, many coverages that arise in practice are actually already Grothendieck pretopologies.


## Examples ##

The prototype is the pretopology consisting of open covers of a
topological space/manifold.  Other pretopologies on [[Top]] include:

* [[local section|Local-section]]-admitting surjections
* Surjective [[open map|open maps]]
* Surjective [[topological submersion|topological submersions]]
* Surjective [[local homeomorphism|local homeomorphisms]]

An example for the category of manifolds is the pretopology of [[surjective submersion]]s.  All of these have covering families consisting of single arrows. Such a pretopology is called a *singleton* pretopology (or, if you prefer the name [[coverage]], a singleton coverage).

Most of the examples of [[coverage|coverages]] are in fact Grothendieck pretopologies.

(Other examples ..)
