
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea 

What is called _global equivariant stable homotopy theory_ is a variant of [[equivariant stable homotopy theory]] where  [[spectra]] are equipped with $G$-[[infinity-actions]] "for all [[compact Lie groups]] $G$ at once".

Often this is referred to just as "global stable homotopy theory" or even just "global homotopy theory". But there is also _unstable_ _[[global equivariant homotopy theory]]_.


More precisely, given an [[orthogonal spectrum]] $X$, then every [[representation]] $\rho \colon G \to O(n)$ of a [[compact Lie group]] on the [[Cartesian space]] $\mathbb{R}^n$ by [[orthogonal group]] [[actions]] induces a $G$-[[equivariant spectrum]] and hence a notion of $G$-[[equivariant homotopy groups]]. 

One says that a morphism of [[orthogonal spectra]] is a **global equivariant equivalence** if it induces [[isomorphisms]] on all $G$- [[equivariant homotopy groups]], for all $G$, this way. (This definition appears for instance as ([Schwede 13, def. 2.9](#Schwede13)), there referred to just as "global equivalence". See also at _[[equivariant Whitehead theorem]]_.)

The **global equivariant stable homotopy category** $\mathcal{GH}$ is the ([[simplicial localization|simplicial]]) [[localization]] of the [[category]] of [[orthogonal spectra]] at these global equivariant equivalences (this is a [[stable (infinity,1)-category]]/[[triangulated category]].)

Since a global equivariant equivalence is in particular an ordinary [[weak homotopy equivalence]] of [[spectra]], there is a canonical functor

$$
  U \;\colon\; \mathcal{GH} \longrightarrow \mathcal{SH}
$$

from the global equivariant to the ordinary [[stable homotopy category]].

This functor has a ([[derived functor|derived]]) [[left adjoint]] and [[right adjoint]], which are both [[full and faithful functors]], hence which exhibit [[discrete object]]/[[codiscrete object]] structure

$$
  \array{
    \mathcal{GH}
    &\stackrel{\overset{L}{\leftarrow}}{\stackrel{\overset{U}{\longrightarrow}}{\underset{R}{\leftarrow}}}&
    \mathcal{SH}
  }
$$

on stable/triangulated categories ([Schwede 13, theorem IV 5.2](#Schwede13))

Global Borel-type [[equivariant cohomology]] is in the image of the [[right adjoint]] $R$ ([Schwede 13, example IV 5.12](#Schwede13))

## Properties

### Relation to plain stable homotopy theory
 {#RelationToPlainStableHomotopyTheory}

The [[forgetful functor]] from global stable homotopy theory to plain [[stable homotopy theory]] exhibits a [[recollement]].

(...)

## Examples

* [[global equivariant sphere spectrum]]

## Related concepts

* [[global family]]

## References

A comprehensive textbook account is in

* {#Schwede13} [[Stefan Schwede]], _[[Global homotopy theory]]_ ([arXiv:1802.09382](https://arxiv.org/abs/1802.09382))

Survey (with emphasis on [[global equivariant bordism homology theory]]):

* {#Schwede15} [[Stefan Schwede]], _Equivariant bordism from the global perspective_, 2015 ([pdf](http://www.math.uni-bonn.de/people/schwede/glasgow-handout.pdf), [[SchwedeGlobalEquivariantBordism.pdf:file]])

Original articles are

* [[L. Gaunce Lewis]], Jr., [[Peter May]], M. Steinberger, chapter II of _Equivariant stable homotopy theory_. Lecture Notes in Mathematics, 1213, Springer-Verlag, 1986

* [[John Greenlees]], [[Peter May]], section 5 of _Localization and completion theorems for $MU$-module spectra_ Ann. of Math. (2) 146 (1997), 509-544.

Discussion specifically in terms of equivariant [[orthogonal spectra]] is in

* [[Anna Marie Bohmann]], _Global Orthogonal Spectra_ ([arXiv:1208.4997](http://arxiv.org/abs/1208.4997))

  
Discussion for collections of [[finite group|finite]] [[subgroups]] includes

* [[Wolfgang Lueck]], _The Burnside Ring and Equivariant Stable Cohomotopy for Infinite Groups_ ([arXiv:math/0504051](http://arxiv.org/abs/math/0504051))

* [[Irakli Patchkoria]], _Proper equivariant stable homotopy and virtual cohomological dimension_, in _Oberwolfach Report_ No. 14/2015 ([pdf](https://www.mfo.de/document/1511/preliminary_OWR_2015_14.pdf))

* [[Markus Hausmann]], _Symmetric spectra model global homotopy theory of finite groups_ ([arXiv:1509.09270](http://arxiv.org/abs/1509.09270))

The example of [[algebraic K-theory]]:

* [[Stefan Schwede]], _Global algebraic K-theory_ ([arXiv:1912.08872](https://arxiv.org/abs/1912.08872))


[[!redirects global stable homotopy theory]]
[[!redirects global equivariant homotopy theory]]