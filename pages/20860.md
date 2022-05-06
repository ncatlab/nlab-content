
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

1. the set $\mathcal{D}^t$ of connected [[Feynman diagrams]] for [[Chern-Simons theory]] in the presence of one [[Wilson line]] (also called "chinese character diagrams" ([Bar-Natan 95, Def. 1.8](#BarNatan95))).

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

([Bar-Natan 95, Theorem 6](#BarNatan95))

<center>
<img src="https://ncatlab.org/nlab/files/ChordsMod4TIsCSModSTU.jpg" width="800">
</center>

> graphics grabbed form [Bar-Natan & Stoimenow 97](#BarNatanStoimenow97)

## Related concepts

* [[Vassiliev invariant]]

* [[graph complex]]

## References

The result is due to 

* {#BarNatan95} [[Dror Bar-Natan]], Theorem 6 in: _On the Vassiliev knot invariants_, Topology Volume 34, Issue 2, April 1995, Pages 423-472 (<a href="https://doi.org/10.1016/0040-9383(95)93237-2">doi:10.1016/0040-9383(95)93237-2</a>, [pdf](https://www.math.toronto.edu/drorbn/papers/OnVassiliev/OnVassiliev.pdf))

Review:

* {#BarNatanStoimenow97} [[Dror Bar-Natan]], Alexander Stoimenow, _The Fundamental Theorem of Vassiliev Invariants_ ([arXiv:q-alg/9702009](https://arxiv.org/abs/q-alg/9702009))


[[!redirects 4T relation]]
[[!redirects 4T relations]]
[[!redirects 4T-relation]]
[[!redirects 4T-relations]]

[[!redirects STU relation]]
[[!redirects STU relations]]
[[!redirects STU-relation]]
[[!redirects STU-relations]]
