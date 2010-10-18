

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A [[topological groupoid]] or [[Lie groupoid]] $C$ is called an **&#233;tale groupoid** if the source-map $s : Mor C \to Obj C$ is a [[local homeomorphism]] or [[local diffeomorphism]], respectively.

It follows that all the other structure maps (target, identity composition) are also local homeomorphisms, resp. local diffeomorphisms.

This means that we may regard an &#233;tale groupoid as an [[internal groupoid]] in the [[category]] whose objects are [[topological spaces]]/[[smooth manifold]]s and whose morphisms are local homeomorphisms/diffeomorphisms.

## Properties

### Cohomology and homology

In the literature one finds, roughly speaking, two dierent approaches to the study of &#233;tale groupoids. One approach is based on the construction of the convolution algebras associated to an &#233;tale groupoid, in the spirit of Connes' [[noncommutative geometry]], and involves the study of [[cyclic homology|cyclic]] and [[Hochschild homology]] and [[Hochschild cohomology|cohomology]] of these algebras. The other approach uses methods of algebraic topology such as the construction of the [[classifying space]] of an
&#233;tale groupoid and its [[abelian sheaf cohomology|(sheaf) cohomology groups]].

## Examples

&#201;tale groupoids arise naturally as models for [[leaf space]]s of [[foliation]]s, for [[orbifold]]s, and for [[orbit space]]s of [[discrete group]] [[action]]s.


* Every [[topological space]] may be regarded as an &#233;tale groupoid with only identity morphisms.

* For $X$ a [[topological space]] and $\Gamma$ a [[discrete group]] with a continuous [[action]] $X \times \Gamma \to X$ on $X$, the [[action groupoid]] $X//\Gamma$ is &#233;tale.

* The [[Haefliger groupoid]] $\Gamma^q$ has the [[Cartesian space]] $\mathbb{R}^q$ as its space of objects. A [[morphism]] $x \to y$ is a [[germ]] of a [[diffeomorphism]] $(\mathbb{R}^q,x) \to (\mathbb{R}^q, y)$.

  This groupoid, and its [[geometric realization]] play a central role in [[foliation theory]].

* Every [[orbifold]] is an &#233;tale [[Lie groupoid]].

## References

* [[Marius Crainic]], [[Ieke Moerdijk]], _A Homology Theory for &#201;tale groupoids_ ([journal](http://www.math.uiuc.edu/K-theory/0284/))

[[!redirects étale groupoids]]

[[!redirects etale groupoid]]
[[!redirects etale groupoids]]