
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A **cochain complex** $V^\bullet$ in an [[Ab-enriched category]] $C$ may be regarded as a [[chain complex]] (see there for more) in $C$, but with the sign of the $\mathbb{Z}$-grading reversed.

This means that for a cochain complex $(V^\bullet,d)$ the [[differential]] (or *coboundary* operator) $d$ _increases_ the degree

$$
  d \colon V^{k} \to V^{k+1}
  \,.
$$


## Examples 

* An archetypical example is the deRham cochain complex of [[differential form]]s on a [[manifold]] $X$, or more generally of [[differential forms in synthetic differential geometry]]. 

* The dual (in some suitable sense) of a [[chain complex]] $(V_\bullet, \partial_k : V_k \to V_{k-1})$ is canonically a cochain complex with $V^k := (V_k)^*$ and $d_k := (\partial_k)^*$.

* A [[monoid]] in chain complexes as well as cochain complexes is a [[differential graded algebra]].

  * In their dual formulation [[L-infinity-algebra]]s and more generall [[Lie infinity-algebroid]]s are encoded by such monoids in cochain complexes.

* By the dual [[Dold-Kan correspondence]] cochain complexes in non-negative degree are equivalent to [[simplicial object|cosimplicial]] abelian groups.

[[!redirects cochain complexes]]


