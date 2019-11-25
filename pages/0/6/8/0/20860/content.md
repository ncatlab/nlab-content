[[!redirects chord diagrams modulo 4T are Chern-Simons diagrams modulo STU]]

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


## Ingredients

Consider 

1. the [[set]] $\mathcal{D}^c$ of [[chord diagrams]];

1. the set $\mathcal{D}^t$ of [[Jacobi diagrams]];

Write

* $\mathcal{D}^c \overset{i}{\hookrightarrow} \mathcal{D}^t$ for the canonical [[injection]];

* $Span(\mathcal{D}^c)$ and $Span(\mathcal{D}^t)$, respectively, for the [[linear span]] of these sets 

  > [[characteristic zero]] necessary?

and finally

\[
  \label{QuotientSpaces}
  \mathcal{A}^c 
    \;\coloneqq\;
  Span(\mathcal{D}^c)/4T 
  \,,
  \phantom{AAAA}
  \mathcal{A}^t 
    \;\coloneqq\;
  Span(\mathcal{D}^t)/STU
\]

for the respective [[quotient spaces]] by the [[4T relations]] 

<img src="https://ncatlab.org/nlab/files/4TRelation.jpg" width="500">


and by the [[STU relations]]


<img src="https://ncatlab.org/nlab/files/STURelation.jpg" width="500">

respectively.

> graphics grabbed from [Bar-Natan 95](#BarNatan95)

## Statement

The linear extension of the canonical inclusion $\mathbb{D}^c \overset{i}{\hookrightarrow} \mathbb{D}^t$ descends to the quotients (eq:QuotientSpaces) and yields a [[linear isomorphism]]:

$$
  \mathcal{A}^c
  \underoverset{\simeq}{i}{\longrightarrow}
  \mathcal{A}^t
$$

<center>
<img src="https://ncatlab.org/nlab/files/ChordsMod4TIsCSModSTU.jpg" width="840">
</center>

> graphics grabbed form [Bar-Natan & Stoimenow 97](#BarNatanStoimenow97)

This is due to [Bar-Natan 95, Theorem 6](#BarNatan95). See also [Chmutov-Duzhin-Mostovoy 11, 5.3](#ChmutovDuzhinMostovoy11)

The key step of the **proof** is to observe that the [[STU-relations]] imply the [[4T-relations]] as follows:

<img src="https://ncatlab.org/nlab/files/4TRelationFromSTURelation.jpg" width="600">

> graphics grabbed form [Bar-Natan & Stoimenow 97](#BarNatanStoimenow97)


## Related concepts

* [[Vassiliev invariant]]

* [[graph complex]]

## References

The result is due to 

* {#BarNatan95} [[Dror Bar-Natan]], Theorem 6 in: _On the Vassiliev knot invariants_, Topology Volume 34, Issue 2, April 1995, Pages 423-472 (<a href="https://doi.org/10.1016/0040-9383(95)93237-2">doi:10.1016/0040-9383(95)93237-2</a>, [pdf](https://www.math.toronto.edu/drorbn/papers/OnVassiliev/OnVassiliev.pdf))

Lecture notes

* {#BarNatanStoimenow97} [[Dror Bar-Natan]], Alexander Stoimenow, _The Fundamental Theorem of Vassiliev Invariants_ ([arXiv:q-alg/9702009](https://arxiv.org/abs/q-alg/9702009))

Textbook accounts:

* {#ChmutovDuzhinMostovoy11} S. Chmutov, Sergei Duzhin, J. Mostovoy, Sectin 5.3 of  _Introduction to Vassiliev knot invariants_, Cambridge University Press, 2012 ([arxiv/1103.5628](http://arxiv.org/abs/1103.5628), [doi:10.1017/CBO9781139107846](https://doi.org/10.1017/CBO9781139107846))



[[!redirects 4T relation]]
[[!redirects 4T relations]]
[[!redirects 4T-relation]]
[[!redirects 4T-relations]]

[[!redirects STU relation]]
[[!redirects STU relations]]
[[!redirects STU-relation]]
[[!redirects STU-relations]]
