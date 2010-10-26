
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

> this entry is under construction. Much of what should eventually go here is currently at [[Lie infinity-groupoid|smooth ∞-groupoid]] and [[schreiber:path ∞-groupoid]].

#Contents#
* automatic table of contents goes here
{:toc}


## Idea 

A _topological $\infty$-groupoid_ is an [[∞-groupoid]] equipped with  [[cohesive (∞,1)-topos|cohesion]] in the form of [[topology]].


## Definition

Let $TopBalls$ be the [[site]] of [[open ball]]s with the [[good open cover]] [[coverage]].

+-- {: .un_defn}
###### Definition

Define

$$
  \infty TopGrpd := (\infty,1)Sh(TopBalls)
$$

to be the [[(∞,1)-category of (∞,1)-sheaves]] on $TopBalls$.

=--

+-- {: .un_lemma}
###### Lemma


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

The site $TopBalls$ clearly satisfies the properties of a  [[(∞,1)-cohesive site]]. 

=--

+-- {: .un_defn}
###### Definition

A **topological $\infty$-groupoid** is a [[concrete (∞,1)-sheaf]] on $TopBalls$. The [[(∞,1)-quasitopos]] of topological $\infty$-groupoids is

$$
  \infty Grpd
   \hookrightarrow
   Concr(\infty TopGrpd)
  \stackrel{\overset{concretization}{\leftarrow}}{\hookrightarrow}
  \infty TopGrpd
  \,.
$$

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

## Related concepts

* [[cohesive (∞,1)-topos]]

  * [[∞-groupoid]]

  * **topological $\infty$-groupoid**

  * [[smooth ∞-groupoid]]



## References

* [[Dan Dugger]], _Sheaves and homotopy theory_ ([web](http://www.uoregon.edu/~ddugger/cech.html), [dvi](http://www.uoregon.edu/~ddugger/cech.dvi), [pdf](http://ncatlab.org/nlab/files/cech.pdf))
{#Dugger}

[[!redirects topological ∞-groupoid]]
[[!redirects topological ∞-groupoids]]

[[!redirects ?TopGrpd]]