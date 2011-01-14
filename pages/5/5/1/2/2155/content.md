
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

+-- {: .un_defn}
###### Definition

A __Cartesian space__ is a [[topological space]] of the form $\mathbb{R}^n$ equipped with the [[Euclidean topology]]: 

the $n$-fold [[Cartesian product]] in [[Top]] of the [[real line]] $\mathbb{R}$ with itself where $n$ is some [[natural number]] (possibly zero).

=--


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

### As a site

+-- {: .un_defn}
###### Definition

Write

* $CartSp_{top}$ for the category whose [[object]]s are Cartesian spaces and whose [[morphism]]s are all [[continuous maps]] between these.

* $CartSp_{smooth}$ for the category whose [[object]]s are Cartesian spaces and whose [[morphism]]s are all [[smooth functions]] between these.

* $CartSp_{synthdiff}$ for the [[full subcategory]] of the category of [[smooth loci]] on those of the form $\mathbb{R}^n \times D$ for $D$ an [[infinitesimal space]] (the formal dual of a Weil algebra).

=--

+-- {: .un_prop}
###### Proposition

In all three cases there is the [[good open cover]] [[coverage]] that makes $CartSp$ a [[site]].

=--

+-- {: .proof}
###### Proof

For $CartSp_{top}$ this is obvious. For $CartSp_{smooth}$ this is somewhat more subtle. It is a folk theorem (see the references at [[open ball]]). A detailed proof is at [[good open cover]]. This directly carries over to $CartSp_{synthdiff}$.

=--

+-- {: .un_prop}
###### Proposition

Equipped with this structure of a site, $CartSp$ is an 
[[∞-cohesive site]].

=--

The corresponding [[cohesive topos]] [[sheaf topos|of sheaves]] is

* $Sh_{(1,1)}(CartSp_{smooth})$, discussed at [[diffeological space]].

* $Sh_{(1,1)}(CartSp_{synthdiff})$, discussed at [[Cahiers topos]].

The corresponding [[cohesive (∞,1)-topos]] [[(∞,1)-category of (∞,1)-sheaves|of (∞,1)-sheaves]] is

* $Sh_{(\infty,1)}(CartSp_{top}) =$ [[ETop∞Grpd]];

* $Sh_{(\infty,1)}(CartSp_{smooth}) =$ [[Smooth∞Grpd]];

* $Sh_{(\infty,1)}(CartSp_{synthdiff}) =$ [[SynthDiff∞Grpd]];


### As a category with open maps

There is a canonical structure of a category with [[open map]]s on $CartSp$ (...)


### As an algebraic theory

The category $CartSp$ is (the [[syntactic category]] of ) a [[Lawvere theory]]: the theory for [[smooth algebra]]s.


### As a pre-geometry

Equipped with the above [[coverage]]-structure,  [[open map]]-structure and [[Lawvere theory]]-property, $CartSp$ is essentially a [[pregeometry (for structured (∞,1)-toposes)]].

(Except that the pullback stability of the open maps holds only in the weaker sense of [[coverage]]s).

(...)






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