
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

In [[knot theory]] a _framed weight system_ is an assignment of [[numbers]] to [[chord diagrams]] which is [[invariant]] under the [[4T-relation]]. 

If the assignment is in addition invariant under the [[1T-relation]], then it is called an _unframed weight system_, or just _weight system_, for short.

## Definition

+-- {: .num_defn #LinearSpanOfChordDiagramsModulo4T}
###### Definition
**([[linear span]] of [[chord diagrams]] [[quotient vector space|modulo]] [[4T-relations|4T]])**

Let $k$ be a [[field]] of [[characteristic zero]]. Write 

1. $\mathcal{D}^c$ for the [[set]] of [[chord diagrams]],

1. $k\langle \mathcal{D}^c\rangle$ for its $k$-[[linear span]],

1. $\mathcal{A}^c \;\coloneqq\; k\langle \mathcal{D}^c\rangle/4T$ for the [[quotient vector space]] by the [[4T-relations]].

=--

+-- {: .num_defn #FramedWeightSystems}
###### Definition
**([[framed weight system]])**

A _$k$-values framed weight system_ is a [[linear function]] on the [[linear span]] of [[chord diagrams]] [[quotient vector space|modulo]] [[4T-relations]] (Def. \ref{LinearSpanOfChordDiagramsModulo4T})

$$
  w 
  \;\colon\;
  \mathcal{A}^c \longrightarrow k
  \,,
$$

hence the $k$-[[vector space]] of framed weight systems is the [[dual vector space]]

$$
  \mathcal{W}
  \;\coloneqq\;
  (\mathcal{A}^c)^\ast
$$

=--

([Bar-Natan 95, Def. 1.6](#BarNatan95), see [Chmutov-Duzhin-Mostovoy 11, Def. 4.1.1](#ChmutovDuzhinMostovoy11), [Jackson-Moffat 19, Section 11.7](#JacksonMoffat19))


+-- {: .num_remark}
###### Remark

Since [[chord diagrams modulo 4T are Jacobi diagrams modulo STU]], framed weight systems equivalently form the [[dual vector space]]

$$
  \mathcal{W}
  \;\simeq\;
  (\mathcal{A}^t)^\ast
$$

of the [[quotient vector space]] $\mathcal{A}^t \coloneqq k\langle \mathcal{D}^t \rangle/STU$ of the [[linear span]] of [[Jacobi diagrams]] by the [[STU-relation]].

=--

## Properties

### Weight systems from Lie algebras

(...)

## Related concepts

* [[Vassiliev invariant]]

* [[Kontsevich integral]]

## References

Original articles

* {#BarNatan95} [[Dror Bar-Natan]], _On the Vassiliev knot invariants_, Topology Volume 34, Issue 2, April 1995, Pages 423-472 (<a href="https://doi.org/10.1016/0040-9383(95)93237-2">doi:10.1016/0040-9383(95)93237-2</a>, [pdf](https://www.math.toronto.edu/drorbn/papers/OnVassiliev/OnVassiliev.pdf))

Textbook accounts

* {#ChmutovDuzhinMostovoy11} [[Sergei Chmutov]], [[Sergei Duzhin]], [[Jacob Mostovoy]], Section 4 of:  _Introduction to Vassiliev knot invariants_, Cambridge University Press, 2012 ([arxiv:1103.5628](http://arxiv.org/abs/1103.5628), [doi:10.1017/CBO9781139107846](https://doi.org/10.1017/CBO9781139107846))


* {#JacksonMoffat19} [[David Jackson]], [[Iain Moffat]], Section 11.7 of: _An Introduction to Quantum and Vassiliev Knot Invariants_, Springer 2019 ([doi:10.1007/978-3-030-05213-3](https://link.springer.com/book/10.1007/978-3-030-05213-3))

[[!redirects weight systems]]

[[!redirects framed weight system]]
[[!redirects framed weight systems]]

[[!redirects unframed weight system]]
[[!redirects unframed weight systems]]

[[!redirects un-framed weight system]]
[[!redirects un-framed weight systems]]


