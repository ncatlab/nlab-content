
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
#### Differential geometry
+-- {: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea
  {#Idea}

A __Cartesian space__ is a [[finite product|finite]] [[Cartesian product]] of the [[real line]] $\mathbb{R}$ with itself. Hence, a Cartesian space has the form $\mathbb{R}^n$ where $n$ is some [[natural number]] (possibly [[zero]]). 

What exactly this means depends on which [[category]] the [[real line]] $\mathbb{R}$ is being considered as an [[object]] of. 

For instance, if $\mathbb{R}$ is regarded as a [[topological space]] (hence an object in the category [[Top]]), then $\mathbb{R}^n$ is a [[Euclidean space]]. Another possibility is to regard $\mathbb{R}$ as a [[topological manifold]], [[differentiable manifold]] or [[smooth manifold]] (hence an object in the categories [[TopMfd]] or [[Diff]]), in which case $\mathbb{R}^n$ is the archetypical such [[manifold]] of [[dimension of a manifold|dimension]] $n$ (the basic [[coordinate chart]]).

The Cartesian space $\mathbb{R}^n$ with its standard [[topological space|topology]]/[[smooth structure]] is also called *real $n$-dimensional space*.

One could also regard $\mathbb{R}$ as the [[real vector space]] of [[dimension of a vector space|dimension]] 1, in which case $\mathbb{R}^n$ would be the real vector space of dimension $n$ (maybe understood as equipped with the [[linear basis]] canonically induced by this presentation), hence [[generalized the|the]] "real $n$-dimensional vector space". However, a vector space would typically not be referred to as a "Cartesian space".

But in between the last two examples, regarding $\mathbb{R}^n$ as an *[[affine space]]* makes it the the basis of "[analytic geometry](https://en.m.wikipedia.org/wiki/Analytic_geometry)" in the sense originally due to [[René Descartes]] ([[Cartesian geometry]]), and this is where the term "Cartesian space" originates from.



One might also speak of the [[complexified]] cartesian space $\mathbb{C}^n$ as a [[complex manifold]], or indeed of the cartesian space $K^n$ for any [[field]] $K$, maybe regarded as an [[analytic space]], though this is not common terminology.


+-- {: .un_example}
###### Example

In particular:

*  $\mathbb{R}^0$ is the [[point]],
*  $\mathbb{R}^1$ is the [[real line]],
*  $\mathbb{R}^2$ is the real [[plane]], which may be identified (in two canonical ways) with the [[complex number|complex plane]] $\mathbb{C}$.

=--


+-- {: .un_remark}
###### Remark

Cartesian spaces carry plenty of further canonical structure:


* It is canonically a [[metric space]] and the [[Euclidean topology]] is the corresponding [[metric space|metric topology]].

* There is a canonical [[smooth structure]] on $\mathbb{R}^n$ that makes it a [[smooth manifold]].

* A Cartesian space is canonically a[[vector space]] over the [[field]] of [[real number]]s.


Sometimes one is interested in allowing $n$ to take other values, in which case one wants a [[product]] in some category that might not be the Cartesian product on underlying sets.

For example, if one is studying Cartesian spaces as [[inner product space]]s, then one might want an $\aleph_0$-dimensional Cartesian space to be the $\aleph_0$-dimensional [[Hilbert space]] $l^2$, which is a proper subset of the cartesian product $\mathbb{R}^{\aleph_0}$.

=--

## Properties

### Topological structure


The [[open n-ball]] is [[homeomorphic]] [[Cartesian space]] $\mathbb{R}^n$

$$
  \mathbb{B}^n \simeq \mathbb{R}^n
  \,.
$$

* [[topological invariance of dimension]]

### Smooth structures

For all $n \in \mathbb{N}$, the [[open n-ball]] with its standard [[smooth structure]] is [[diffeomorphic]] to the [[Cartesian space]] $\mathbb{R}^n$ with its standard smooth structure

$$
  \mathbb{B}^n \simeq \mathbb{R}^n
  \,.
$$

In fact, in $d \neq 4$ there is no choice:

+-- {: .un_theorem}
###### Theorem

For $n \in \mathbb{N}$ a [[natural number]] with $n \neq 4$, there is a unique (up to [[isomorphism]]) smooth structure on the [[Cartesian space]] $\mathbb{R}^n$. 

=--

This was shown in ([Stallings](#Stallings)).

+-- {: .un_theorem}
###### Theorem

In $d = 4$ the analog of this statement is false. One says that on $\mathbb{R}^4$ there exist [[exotic smooth structure]]s.
 
=--

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


## The category of Cartesian spaces

See [[CartSp]].


## Related concepts

* [[super Cartesian space]]

* [[polydisk]]

* [[affine space]]

In [[complex geometry]] for purposes of [[Cech cohomology]] the role of Cartesian spaces is played by [[Stein manifolds]].

* [[topological invariance of dimension]]

## References

Named after [[René Descartes]].

* {#Stallings} [[John Stallings]], _The piecewise linear structure of Euclidean space_ , Proc. Cambridge Philos. Soc. 58 (1962), 481-488. ([pdf](http://journals.cambridge.org/production/action/cjoGetFulltext?fulltextid=2118140))


* {#Ozols} V. Ozols, _Largest normal neighbourhoods_ ,
Proceedings of the American Mathematical Society
Vol. 61, No. 1 (Nov., 1976), pp. 99-101  ([jstor](http://www.jstor.org/stable/2041672))



There are various slight variations of the category $CartSp$ that one can consider without changing its basic properties as a category of test spaces for [[generalized smooth space]]s. A different choice that enjoys some popularity in the literature is the category of open (contractible) subsets of Euclidean spaces. For more references on this see [[diffeological space]].

The [[site]] $ThCartSp$ of infinitesimally thickened Cartesian spaces is known as the site for the [[Cahiers topos]]. It is considered 

in detal in section 5 of

* [[Anders Kock]], _Convenient vector spaces embed into the Cahiers topos_ ([numdam](http://www.numdam.org/item?id=CTGDC_1986__27_1_3_0))

and briefly mentioned in example 2) on p. 191 of

* [[Anders Kock]], _Synthetic differential geometry_ ([pdf](http://home.imf.au.dk/kock/sdg99.pdf))

following the original article

* [[Eduardo Dubuc]], _Sur les modeles de la geometrie differentielle synthetique_ ([numdam](http://www.numdam.org/item?id=CTGDC_1979__20_3_231_0)).

With an eye towards [[Frölicher space]]s the site is also considered in section 5 of 

* Hirokazu Nishimura, _Beyond the Regnant Philosophy of Manifolds_ ([arXiv:0912.0827](http://arxiv.org/abs/0912.0827))



[[!redirects Cartesian space]]
[[!redirects cartesian spaces]]
[[!redirects Cartesian spaces]]
[[!redirects real n-dimensional space]]

[[!redirects Cartesian Space]]
[[!redirects Cartesian Spaces]]
[[!redirects smooth Cartesian space]]
[[!redirects smooth Cartesian spaces]]


