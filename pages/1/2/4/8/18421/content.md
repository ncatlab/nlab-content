
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

A _topological ∞-groupoid_ is meant to be an [[∞-groupoid]] that is equipped with [[topology|topological]] structure. For instance a [[0-truncated object|0-truncated]] topological $\infty$-groupoid should just be a [[topological space]], and 1-truncated topological $\infty$-groupoids should reproduce [[topological groupoids]]/[[topological stacks]], etc.

A generic way to make sense of this in a _[[gros topos]]_ perspective is to pick some small [[subcategory]] $Top_{sm}$ of the category [[Top]] of [[topological spaces]], regard it as a [[site]] with respect to an evident [[coverage]] by [[open covers]], and then take the [[(∞,1)-topos]] of generalized topological $\infty$-groupoids to be the [[(∞,1)-category of (∞,1)-sheaves]] on this site:

$$
  Top \infty Grpd \coloneqq Sh_\infty(Top_{sm})
  \,.
$$

This gives a nice category with very general objects. In there one may find smaller, less nice categories of nicer objects.

There are different choices of [[sites]] $Top_{sm}$ to make. For instance

1. taking $Top_{sm}$ to be a small site of [[locally contractible topological spaces]] yields a concept of _[[locally contractible topological infinity-groupoids]]_;

1. taking $Top_{sm}$ be the the subcategory of topological [[Cartesian spaces]] yield a concept of [[Euclidean-topological infinity-groupoids]].

These two happen to constitute [[cohesive ∞-toposes]], due to the local contractibility of the objects in the site.

## Related concepts

* [[discrete ∞-groupoid]]

* [[D-topological ∞-groupoid]]

* [[smooth ∞-groupoid]]

* [[formal smooth ∞-groupoid]]

* [[super formal smooth ∞-groupoid]]

[[!redirects topological infinity-groupoid]]
[[!redirects topological infinity-groupoids]]
[[!redirects topological ∞-groupoid]]
[[!redirects topological ∞-groupoids]]

[[!redirects ?TopGrpd]]

[[!redirects continuous infinity-groupoid]]
[[!redirects continuous infinity-groupoids]]
[[!redirects continuous ∞-groupoid]]
[[!redirects continuous ∞-groupoids]]

[[!redirects topological infinity-group]]
[[!redirects topological infinity-groups]]
[[!redirects topological ∞-group]]
[[!redirects topological ∞-groups]]

[[!redirects topological infinity-stack]]
[[!redirects topological infinity-stacks]]

[[!redirects topological ∞-stack]]
[[!redirects topological ∞-stacks]]

