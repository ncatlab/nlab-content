
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
=--
=--

> this entry is under construction

#Contents#
* table of contents
{:toc}

## Idea

A _smooth super $\infty$-groupoid_ is a [[super ∞-groupoid]] equipped with _smooth_ [[cohesive (∞,1)-topos|cohesion]].

This includes [[supermanifold]]s and [[delooping]]s of [[super Lie group]]s.


## Definition

We conceive a smooth super $\infty$-groupoid as [[smooth ∞-groupoid]] but not over the [[base topos]] [[∞Grpd]] of bare [[∞-groupoid]]s, but over the [[base topos]] [[Super∞Grpd]] of [[super ∞-groupoid]]s.

Recall from the discussion at _[[super ∞-groupoid]]_ that there is a canonical [[line object]] 

$$
  \mathcal{R} \in SuperSet \hookrightarrow Super\infty Grpd
$$

which as a presheaf on the [[site]] of [[superpoint]]s is given by

$$
  \mathcal{R} : \mathbb{R}^{0|q} \mapsto (\Lambda_q)_{even}
  \,,
$$

where $\Lambda_q$ is (the underlying set of) the [[Grassmann algebra]] on $q$ generators, and $(\Lambda_q)_{even}$ is (the underlying set of) its even part.

+-- {: .num_defn}
###### Definition

Write $sCartSp$ for the [[internal site]] in $SuperSet \hookrightarrow$ [[Super∞Grpd]] whose

* [[object]]s are the [[product]]s $\mathbb{R}^{}$s for $n \in \mathbb{N}$;

* [[morphism]]s are those morphisms of supersets that are smooth with respect to the canonical [[supermanifold]] structure on $\mathbb{R}^n$ (see the section [As manifolds over the base topos on superpoints](#http://nlab.mathforge.org/nlab/show/supermanifold#OverSuperpoints))
].

* [[coverage]] is given by the internal [[good open cover]]s.

(...)

=--


+-- {: .num_defn}
###### Definition

Let

$$
  SmoothSuper\infty Grpd := Sh_{(\infty,1)}(sCartSp, Super \infty Grpd)
$$

be the [[(∞,1)-topos]] of internal [[(∞,1)-sheaves]] in [[Super∞Grpd]] over the [[internal site]] $sCartSp$.

=--

## References

See the references at [[super ∞-groupoid]].


[[!redirects super smooth ∞-groupoid]]
[[!redirects super smooth infintiy-groupoid]]


[[!redirects smooth super ∞-groupoid]]

[[!redirects SuperSmooth∞Grpd]]
