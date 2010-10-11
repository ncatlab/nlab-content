
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

A __Cartesian space__ is a [[topological space]] of the form $\mathbb{R}^n$: the $n$-fold [[Cartesian product]] in [[Top]] of the [[real line]] $\mathbb{R}$ with itself where $n$ is some [[natural number]] (possibly zero).
There is a canonical [[smooth structure]] on $\mathbb{R}^n$ that makes it a [[smooth manifold]].

In particular:
*  $\mathbb{R}^0$ is the [[point]],
*  $\mathbb{R}^1$ is the real line itself,
*  $\mathbb{R}^2$ is the real plane, which may be identified (in two canonical ways) with the [[complex number|complex plane]] $\mathbb{C}$.

Sometimes one is interested in allowing $n$ to take other values, in which case one wants a [[product]] in some category that might not be the Cartesian product on underlying sets.

For example, if one is studying Cartesian spaces as inner product spaces, then one might want an $\aleph_0$-dimensional Cartesian space to be the $\aleph_0$-dimensional [[Hilbert space]] $l^2$, which is a proper subset of the cartesian product $\mathbb{R}^{\aleph_0}$.


## Properties

### The category of Cartesian spaces

Note that a Cartesian space has maximal structure; it comes equipped with a system of coordinates.  Usually we are interested only in some of this structure; what is useful is that the category [[CartSp]] of cartesian spaces and (appropriately) structure-preserving maps is a [[small category]] equivalent to the (usually large) category of *all* finite-dimensional spaces with the structure in question.  This holds at least in the following examples:

*  [[vector space]]s,
*  [[affine space]]s,
*  [[normed vector space]]s,
*  [[inner product space]]s,
*  [[Euclidean space]]s.

$Cart Sp$ can also be understood, for appropriate morphisms, as a category of models for at least the following examples:

*  topological [[manifold]]s,
*  [[smooth space]]s,
*  [[Riemannian manifold]]s.

### Topological structure

The [[open n-ball]] is [[homeomorphic]] [[Cartesian space]] $\mathbb{R}^n$

$$
  \mathbb{B}^n \simeq \mathbb{R}^n
  \,.
$$


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

In $d = 4$ the analog of this statement is false. One says that on $\mathb{R}^4$ there exist [[exotic smooth structure]]s.
 
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

## References

* [[John Stallings]], _The piecewise linear structure of Euclidean space_ , Proc. Cambridge Philos. Soc. 58 (1962), 481-488. ([pdf](http://journals.cambridge.org/production/action/cjoGetFulltext?fulltextid=2118140))
{#Stallings}

* V. Ozols, _Largest normal neighbourhoods_ ,
Proceedings of the American Mathematical Society
Vol. 61, No. 1 (Nov., 1976), pp. 99-101  ([jstor](http://www.jstor.org/stable/2041672))
{#Ozols}

[[!redirects Cartesian space]]
[[!redirects cartesian spaces]]
[[!redirects Cartesian spaces]]