
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Knot theory
+--{: .hide}
[[!include knot theory - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}


## Idea

On the [[vector space]] $\mathcal{A}$ of [[Jacobi diagrams]] [[quotient vector space|modulo]] [[STU-relations]] ([[chord diagrams modulo 4T are Jacobi diagrams modulo STU|equivalently]] [[chord diagrams]] [[quotient vector space|modulo]] [[4T relations]])  there is a system of [[linear maps]] (for $q \in \mathbb{Z}$, $q \neq 0$)

$$
  \psi^q
  \;\colon\;
  \mathcal{A}
  \longrightarrow
  \mathcal{A}
$$

which respect the [[coalgebra]] [[mathematical structure|structure]] and satisfy

$$
  \psi^{q_2} \circ \psi^q_1
  \;=\;
  \psi^{q_1 \cdot q_2}
$$

and as such are (dually) analogous to the [[Adams operations]] on [[topological K-theory]].

([Bar-Natan 95, Def. 3.11 & Theorem 7](#BarNatan95))

In fact, when evaluated in [[Lie algebra weight systems]] $w_{\mathbf{N}}$ and under the identification (see [here](equivariant+K-theory#RelationToRepresentationTheory)) of the [[representation ring]] of a [[compact Lie group]] $G$ with the $G$-[[equivariant K-theory]] of the point, these Adams operations on [[Jacobi diagrams]] correspond to the [[Adams operations]] on [[equivariant K-theory]]:


$$
  w_{\mathbf{N}}(\psi^q D)
  \;=\;
  w_{\psi^q \mathbf{N}}(D)
  \,.
$$

([Bar-Natan 95, Exc. 6.24](#BarNatan95)
)


## References

* {#BarNatan95} [[Dror Bar-Natan]], _On the Vassiliev knot invariants_, Topology Volume 34, Issue 2, April 1995, Pages 423-472 (<a href="https://doi.org/10.1016/0040-9383(95)93237-2">doi:10.1016/0040-9383(95)93237-2</a>, [pdf](https://www.math.toronto.edu/drorbn/papers/OnVassiliev/OnVassiliev.pdf)) 

[[!redirects Adams operations on Jacobi diagrams]]
