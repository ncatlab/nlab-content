A **cochain complex** $V^\bullet$ in an [[Ab-enriched category]] $C$ is nothing but a [[chain complex]] in $C$, but with the sign of the $\mathbb{Z}$-grading reversed.

This means that for a cochain complex $(V^\bullet,d)$ the differential (or *coboundary*) $d$ _increases_ the degree

$$
  d : V^{k} \to V^{k+1}
  \,.
$$


# Examples #

* An archetypical example is the deRham cochain complex of [[differential form]]s on a [[manifold]] $X$, or more generally of [[differential forms in synthetic differential geometry]]. 

* The dual (in some suitable sense) of a [[chain complex]] $(V_\bullet, \partial_k : V_k \to V_{k-1})$ is canonically a cochain complex with $V^k := (V_k)^*$ and $d_k := (\partial_k)^*$.

* A [[monoid]] in chain compexes as well as cochain complexes is a [[differential graded algebra]].

  * In their dual formulation [[L-infinity-algebra]]s and more generall [[Lie infinity-algebroid]]s are encoded by such monoids in cochain complexes.

* By the dual [[Dold-Kan correspondence]] cochain complexes in non-negative degree are equivalent to [[simplicial object|cosimplicial]] abelian groups.


[[!redirects cochain complexes]]