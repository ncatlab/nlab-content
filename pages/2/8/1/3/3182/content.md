[[!redirects Euclidean topological infinity-groupoid]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
=--
=--

> this entry is under construction. Much of what should eventually go here is currently at [[Lie infinity-groupoid|smooth ∞-groupoid]]

#Contents#
* table of contents 
{:toc}


## Idea 

A _Euclidea-topological $\infty$-groupoid_ is an [[∞-groupoid]] equipped with  [[cohesive (∞,1)-topos|cohesion]] in the form of [[Euclidean topology]].


## Definition

Let [[CartSp]]${}_{top}$ be the [[site]] of [[open ball]]s with the [[good open cover]] [[coverage]].

+-- {: .un_defn}
###### Definition

Define

$$
  ETop \infty Grpd := (\infty,1)Sh(CartSp_{top})
$$

to be the [[(∞,1)-category of (∞,1)-sheaves]] on $CartSp_{top}$.

=--

+-- {: .un_prop}
###### Proposition


This is a [[cohesive (∞,1)-topos]].

=--

$$
  \infty TopGrpd
  \stackrel{\stackrel{\overset{\Pi}{\to}}{\underset{Disc}{\leftarrow}}}{\stackrel{\underset{\Gamma}{\to}}{\underset{Codisc}{\leftarrow}}}
  \infty Grpd
  \,.
$$

+-- {: .proof}
###### Proof

The site [[CartSp]]${}_{top}$ an  [[∞-cohesive site]].  See there for details.

=--

## Properties

### Homotopy invariance and topological spaces

The sub-[[(∞,1)-category]] [[∞-stack]]s on [[Top]] (even on [[Diff]]) that are homotopy invariant is equivalent to plain [[∞Grpd]]. 

**Idea**

A central result about the [[(∞,1)-topos]] $Sh_{(\infty,1)}(Top)$ of [[∞-stack]]s on [[Top]] is that the [[homotopy localization]] is equivalent to [[Top]] itself

$$
  Sh_{(\infty,1)}(Top)^I \simeq Top
  \,.
$$

A discussion of this is in (the nice but not quite finished) ([Dugger](#Dugger)).

In fact, this is true even for [[Lie ∞-groupoid]]s, i.e. [[∞-stack]]s on [[Diff]]: the homotopy invariant ones model plain [[topological space]]s.

This provides a useful resolution of [[topological space]]s that often helps to disentangle the two different roles played by a topological space: on the one hand as a model for an [[∞-groupoid]], in the other as a [[locale]].

**Details**

Let $SPSh(Diff)^{loc}$ be the local [[model structure on simplicial presheaves]] obtained by left [[Bousfield localization of model categories|Bousfield localization]] at the [[Cech nerve]]s of 
[[Cech cover]]s with respect to the standard [[Grothendieck topology]] on [[Diff]]. This is a [[models for ∞-stack (∞,1)-toposes|model for ∞-stacks]] on [[Diff]].

Let $SPSh(Diff)^{loc}_I$ be furthermore the left [[Bousfield localization of model categories|Bousfield localization]]
at the set of projection morphisms out of [[product]]s of the form $X \times \mathbb{R} \to X$ for all $X \in Diff$. The $\infty$-stacks that are [[local object]]s with respect
to these morphisms are the _homotopy invariant_ $\infty$-stacks, so this localization models the [[(∞,1)-topos]] of homotopy invariant
$\infty$-stacks on $Diff$.

There is a [[adjunction]]

$$
  L : SSet \stackrel{\leftarrow}{\to} SPSh(Diff) : R
$$

where $L$ sends a simplicial set to the simplicial presheaf constant on that simplicial
set, and where evaluates a simplicial presheaf on the manifold that is the [[point]]. 

**Theorem (Dugger)**

This adjunction $(L \dashv R)$ is a [[Quillen equivalence]] with respect to the  standard [[model structure on simplicial sets]] on the left and the above model structure $SPSh(Diff)_{loc}^I$ on the right.


## Structures

We discuss what some of the general abstract <a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#Structures">Structures in a cohesvive (∞,1)-topos</a> look like in the model $ETop \infty Grpd$.


### Geometric homotopy an Galois theory

(...)

[[nerve theorem]]

### Cohomology

+-- {: .un_theorem }
###### Theorem

For [[paracompact space|paracompact]] $X$ we have an equivalence of [[cocycle]] [[∞-groupoid]]s

$$
  ETop∞Grpd(X, LConst A)
  \simeq
  Top(X, |A|)
$$

and hence in particular an isomorphism on cohomology

$$
  H(X,A) \simeq \pi_0   ETop∞Grpd(X, LConst A)
$$

=--

+-- {: .proof}
###### Proof

By the above (...).

=--




### Path $\infty$-groupoid

(...)

## References

Some discussion of the $(\infty,1)$-category of $(\infty,1)$-sheaves on the category of manifolds and its restriction to open balls is in:

* [[Dan Dugger]], _Sheaves and homotopy theory_ ([web](http://www.uoregon.edu/~ddugger/cech.html), [dvi](http://www.uoregon.edu/~ddugger/cech.dvi), [pdf](http://ncatlab.org/nlab/files/cech.pdf))
{#Dugger}

[[!redirects Euclidean topological ∞-groupoid]]

[[!redirects Euclidean topological infinity-groupoids]]
[[!redirects Euclidean topological ∞-groupoids]]


[[!redirects Euclidean-topological ∞-groupoid]]
[[!redirects Euclidean-topological infnity-groupoid]]


[[!redirects Euclidean-topological infinity-groupoids]]
[[!redirects Euclidean-topological ∞-groupoids]]


[[!redirects ETop∞Grpd]]

[[!redirects topological infinity-groupoid]]


[[!redirects topological ∞-groupoid]]
[[!redirects topological ∞-groupoids]]

[[!redirects ?TopGrpd]]

[[!redirects continuous infinity-groupoid]]
[[!redirects continuous infinity-groupoids]]
[[!redirects continuous ∞-groupoid]]
[[!redirects continuous ∞-groupoids]]

