+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

For $n \in \mathbb{N}$ a [[natural number]], the $n$-[[dimension]]al **ball** is the [[topological space]]

$$
  B^n := \{ \vec x \in \mathbb{R}^n | \sum_{i} (x^i)^2 \leq 1\}
  \subset \mathbb{R}^n
$$ 

equipped with the [[induced topology]] as a subspace of the [[Cartesian space]] $\mathbb{R}^n$.

Its [[interior]] is the **open $n$-ball**

$$
  \mathbb{B}^n := \{ \vec x \in \mathbb{R}^n | \sum_{i} (x^i)^2 \lt 1 \}
  \subset \mathbb{R}^n
  \,.
$$ 

Its [[boundary]] is the $(n-1)$-[[sphere]].

## Properties

The open $n$-ball is [[homeomorphic]] and even [[diffeomorphic]] to the [[Cartesian space]] $\mathbb{R}^n$

$$
  \mathbb{B}^n \simeq \mathbb{R}^n
  \,.
$$

The open $n$-ball is naturally a ([[smooth manifold|smooth]]) [[manifold]]. And every (smooth) $n$-dimensional manifold is locally isomorphic to $\mathbb{B}^n$.

+-- {: .un_theorem}
###### Theorem

In [[dimension]] $d \in \mathbb{N}$ for $d \neq 4$ we have:

every open subset of $\mathbb{R}^d$ which is [[homeomorphic]] to $\mathbb{B}^d$ is also [[diffeomorphic]] to it.

=--

See the first page of ([Ozols](#Ozols)) for a list of references. 


+-- {: .un_remark}
###### Remark

In dimension 4 the analog statement fails due to the existence of [[exotic smooth structure]]s on $\mathbb{R}^4$.

=--

## References

* V. Ozols, _Largest normal neighbourhoods_ ,
Proceedings of the American Mathematical Society
Vol. 61, No. 1 (Nov., 1976), pp. 99-101  ([jstor](http://www.jstor.org/stable/2041672))
{#Ozols}

[[!redirects  balls]]

[[!redirects open ball]]
[[!redirects open balls]]

[[!redirects open n-ball]]
[[!redirects open n-balls]]

[[!redirects closed ball]]
[[!redirects closed balls]]

[[!redirects closed n-ball]]
[[!redirects closed n-balls]]