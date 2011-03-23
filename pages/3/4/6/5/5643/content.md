
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

Let [[CartSp]]${}_{smooth}$ be the site of [[Cartesian space]]s and [[smooth function]]s between them. Notice that the [[(∞,1)-sheaf (∞,1)-topos]] $Smooth \infty Grpd := Sh_{(\infty,1)}(CartSp_{smooth})$ is that of [[smooth ∞-groupoid]]s. This is an [[(∞,1)-topos]] over the  [[base topos]]

$$
  Smooth \infty Grpd \stackrel{\overset{Disc}{\leftarrow}}{\underset{\Gamma}{\to}}
  Sh_{(\infty,1)}(Point) \simeq \infty Grpd
  \,.
$$

Consider in this construction the replacement of the category $Point = \{*\}$ with the categoy $SuperPoint$ of [[superpoints]].


+-- {: .num_defn}
###### Definition

The [[(∞,1)-topos]] of **super smooth ∞-groupoids** is the [[(∞,1)-category of (∞,1)-sheaves]] on [[CartSp]]${}_{smooth}$ with values in [[super ∞-groupoid]]s

$$
  \begin{aligned}
    SuperSmooth\infty Grpd 
     & := Sh_{(\infty,1)}(CartSp_{smooth}, Super \infty Grpd)
     \\
     & =: Sh_{(\infty,1)}(CartSp_{smooth} \times SuperPoint)
  \end{aligned}
 \,,
$$

where the product site $CartSp_{smooth} \times SuperPoint$ is equipped with the product topology, whose [[covering]] families are precisely those of the form 
$\{U_i \times D  \stackrel{(p_i, id)}{\to} U \times D\}$ for $\{U_i \stackrel{p_i}{\to} U\}$ a covering family in [[CartSp]]${}_{smooth}$ (a [[good open cover]]).

=--

+-- {: .num_note}
###### Note

This definition follows the Molotkov-Voronov-Schwarz school on [[superalgebra]] and [[supergeometry]] that works over the [[base topos|base]] [[presheaf topos]] on [[superpoints]]. See the references listed at [[super ∞-groupoid]].

=--

## Properties

The [[(∞,1)-topos]] $SmoothSuper\infty Grpd$ is a [[cohesive (∞,1)-topos]] over [[Super∞Grpd]].

It is an <a href="http://nlab.mathforge.org/nlab/show/cohesive%20(infinity,1)-topos#structures_in_the_presence_of_infinitesimal_cohesion_149">infinitesimal thickening</a> of [[Smooth∞Grpd]]. As such it is similar to [[SynthDiff∞Grpd]] but differs subtly from it. Both are unified in the $(\infty,1)$-topos [[SSynthDiff∞Grpd]] of _super synthetic differential $\infty$-groupoids_

(...)

## References

See the references at [[super ∞-groupoid]].


[[!redirects super smooth ∞-groupoid]]
[[!redirects super smooth infintiy-groupoid]]


[[!redirects smooth super ∞-groupoid]]

[[!redirects SuperSmooth∞Grpd]]
