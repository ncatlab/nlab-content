[[!redirects stringy weight systems]]

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

Where a [[weight system]] on [[chord diagrams]] is equivalently a [[weight system]] on [[Jacobi diagrams]] (since [[chord diagrams modulo 4T are Jacobi diagrams modulo STU]]) and hence an assignment of [[Feynman amplitude]]-factors to [[Chern-Simons theory|Chern-Simons-]][[Feynman diagrams]] (in the presence of a [[Wilson loop]]), a _stringy weight system_ assigns such amplitude factors instead to the [[ribbon graph]] [[surfaces]] of [[open string]] [[worldsheets]] which become [[Jacobi diagrams]] in the [[worldline formalism|point particle limit]] ([Bar-Natan 95, Theorem 10](#BarNatan95), see also [Kneissler 97, Section 1.3](#Kneissler97))

## Details

Given any [[ground field]] $\mathbb{F}$, consider 

\[
  \label{LinearSpanOfMarkedSurfaces}
  Span\big( MarkedSurfaces_{/\sim} \big)
  \;\in\;
  Vect
\]

the [[linear span]] of the [[set]] of [[diffeomorphism]] [[equivalence class|classes]] of [[surfaces]] [[manifold with boundary|with boundary]] equipped with a [[finite number]] of chosen oriented points on their boundary, at least one on each [[connected component]] ([Bar-Natan 95, Def. 1.12](#BarNatan95)).

A _stringy weight system_ is a [[linear map]] from this space to the [[ground field]], hence the space of stringy weight systems is the [[dual vector space]]

\[
  \label{SpaceOfStringyWeightSystems}
  \mathcal{S}
  \;\coloneqq\;
  \Big(
    Span\big( MarkedSurfaces_{/\sim} \big)
  \Big)^\ast
  \,.
\]

Of course a [[linear function]] $Span\big( MarkedSurfaces_{/\sim}\big) \to \mathbb{F}$ is equivalently a plain [[function]] $MarkedSurfaces \to \mathbb{F}$, but for the following construction it is necessary to consider [[formal linear combinations]] of marked surfaces:

The [['t Hooft double line construction]] constitutes a [[linear map]] from the [[linear span]] of [[Jacobi diagrams]] [[quotient vector space|modulo]] [[STU-relations]] to the linear span of marked surfaces (eq:LinearSpanOfMarkedSurfaces)

<center>
<img src="https://ncatlab.org/nlab/files/AtHooftConstrictionIII.jpg" width="650">
</center>

([Bar-Natan 95, Theorem 10 with Theorem 8](#BarNatan95))

> graphics from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]

Under passage to [[dual vector spaces]] this yields a linear map

\[
  \label{PointParticleLimitOfStringyWeightSystems}
  \mathcal{S}
  \overset{
    (tH \,\circ\, perm)^\ast
  }{\longrightarrow}
  \underset{n \in \mathbb{N}}{\prod}
  \big(
    \mathcal{W}^n
  \big)
\]

from stringy weight systems (eq:SpaceOfStringyWeightSystems) to ordinary [[weight systems]]. This may be regarded as the [[worldline formalism|point particle limit]] of stringy weight systems.

## Properties

### Relation to Lie algebra weight systems

+-- {: .num_remark}
###### Remark
**([[stringy weight systems span classical Lie algebra weight systems]])**

The [[image]] of the [[vector space]] (eq:SpaceOfStringyWeightSystems) of [[stringy weight systems]] under the point particle limit map (eq:PointParticleLimitOfStringyWeightSystems) inside the space of ordinary [[weight systems]] coincides with the [[direct sum]] of the linear span of [[Lie algebra weight systems]] for the [[general linear Lie algebras]] $\mathfrak{gl}(N)$ and the [[special orthogonal Lie algebras]] $\mathfrak{so}(N)$, and contains that of [[symplectic Lie algebras]] $\mathfrak{sp}(N)$:

<center>
<img src="https://ncatlab.org/nlab/files/StringyWeightsSpanClassicalLieAlgebraWeight.jpg" width="450">
</center>

=--

([Bar-Natan 95, Theorem 11](#BarNatan95))

> graphics from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]


## Related concepts

* [['t Hooft double line notation]]

* [[Chern-Simons theory as a topological string theory]]

[[!include chord diagrams and weight systems -- table]]

## References

The concept (not by this name, though) is due to

* {#BarNatan95} [[Dror Bar-Natan]], p. 9 and section 6 of: _On the Vassiliev knot invariants_, Topology Volume 34, Issue 2, April 1995, Pages 423-472 (<a href="https://doi.org/10.1016/0040-9383(95)93237-2">doi:10.1016/0040-9383(95)93237-2</a>, [pdf](https://www.math.toronto.edu/drorbn/papers/OnVassiliev/OnVassiliev.pdf))

where it is attributed (Remark 1.13) to private communication with [[Maxim Kontsevich]].

See also

* {#Kneissler97} [[Jan Kneissler]], Section 1.3 of: _The number of primitive Vassiliev invariants up to degree 12_ ([arXiv:q-alg/9706022](https://arxiv.org/abs/q-alg/9706022))

* {#ChmutovDuzhinMostovoy11} [[Sergei Chmutov]], [[Sergei Duzhin]], [[Jacob Mostovoy]], Section 6.2.4 of: _Introduction to Vassiliev knot invariants_, Cambridge University Press, 2012 ([arxiv:1103.5628](http://arxiv.org/abs/1103.5628), [doi:10.1017/CBO9781139107846](https://doi.org/10.1017/CBO9781139107846))

