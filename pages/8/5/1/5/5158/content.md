
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definitions

There are several things that one might mean by a "(possibly [[weak homotopy equivalence|weak]]) [[homotopy equivalence]] of [[toposes]] (or [[(∞,1)-toposes]])."   Some candidates are:

1. A [[geometric morphism]] that induces an [[equivalence]] of the [[fundamental ∞-groupoid of a locally ∞-connected (∞,1)-topos]], or more generally of [[shape of an (∞,1)-topos|shapes]].

1. A geometric morphism which induces an [[isomorphism]] on all [[cohomology]] with [[constant coefficients]].

1. A geometric morphism which has an inverse up to "homotopy" in the classical sense of a map $E\times [0,1]\to F$, where since $E$ and $F$ are toposes, we have to incarnate $[0,1]$ as the topos $Sh([0,1])$.

Of these, the first two are arguably a notion of *weak* homotopy equivalence.  Moreover, they are equivalent, since $\Pi_\infty$ of a topos [[representable functor|represents]] locally constant sheaves/stacks.

## Adjunctions induce homotopy equivalences

One important thing to note is that any [[adjunction]] in the [[2-category]] [[Topos]] induces a homotopy equivalence in any of the above senses.  For the first (hence also the second) sense, we just observe that $\Pi_\infty$ is 2-functorial, whereas it lands in the (∞,1)-category ?Gpd where all 2-morphisms are invertible; hence adjunctions get sent to adjunctions, which are necessarily equivalences.

For the third, we note that has [[weighted limit|tensors]] with the [[interval category]], that are given by [[cartesian product]] with sheaves on the [[Sierpinski space]] $\Sigma$.  Thus, a natural transformation between two geometric morphisms $E\to F$ is the same as a single geometric morphism 
$E\times Sh(\Sigma)\to F$.  Now just pick a map $[0,1]\to \Sigma$ that doesn't identify the endpoints, like the classifying map of $[0,\frac1 2]$, to get an actual "homotopy" between the same two geometric morphisms.  Hence, any 2-morphism in $Topos$ gives a homotopy, so any adjunction gives a homotopy equivalence.

In particular, this means that any [[local geometric morphism]] or [[totally connected geometric morphism]] is a homotopy equivalence.

[[!redirects homotopy equivalence of toposes]]
[[!redirects homotopy equivalence of topoi]]
[[!redirects homotopy equivalences of toposes]]
[[!redirects homotopy equivalences of topoi]]
[[!redirects topos homotopy equivalence]]
[[!redirects topos homotopy equivalences]]
[[!redirects weak homotopy equivalence of toposes]]
[[!redirects weak homotopy equivalence of topoi]]
[[!redirects weak homotopy equivalences of toposes]]
[[!redirects weak homotopy equivalences of topoi]]
[[!redirects topos weak homotopy equivalence]]
[[!redirects topos weak homotopy equivalences]]
