
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Spheres
+--{: .hide}
[[!include spheres -- contents]]
=--
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
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

## Idea

A _spherical fibration_ is a [[fiber bundle]] of [[spheres]] of some [[dimension]] (a [[sphere fiber bundle]]). Typically this is considered in [[homotopy theory]] where one considers [[fibrations]] whose [[fibers]] have the [[homotopy type]] of [[spheres]]; and this in turn is often considered in [[stable homotopy theory]] after [[stabilization]] (hence up to tensoring with trivial spherical fibrations)  which makes spherical fibrations models for [[(∞,1)-module bundles]] for the [[sphere spectrum]] regarded as an [[E-∞ ring]].

Every [[real vector bundle]] becomes a spherical fibration in the sense of [[homotopy theory]] upon removing its [[zero section]] and this construction induces a map from vector bundles and in fact from [[topological K-theory]] to spherical fibrations, called the _[[J-homomorphism]]_.


This is closely related to the [[Thom space]]/[[Thom spectrum]] construction for vector bundles. 

## Definition


### In components

For $X$ (the [[homotopy type]] of) a [[topological space]], a _spherical fibration over it_ is a [[fibration]] $E \to X$ such that each [[fiber]] has the [[homotopy type]] of a [[sphere]].

Given two spherical fibrations $E_1, E_2 \to X$, there is their fiberwise [[smash product]] $E_1 \wedge_X E_2 \to X$. 

For $n \in \mathbb{N}$, write $\epsilon^n \colon X \times S^n \to X$ for the trivial sphere bundle of fiber dimension $n$. Two spherical fibrations $E_1, E_2 \to X$ are _stably fiberwise equivalent_ if there exists $n_1, n_2 \in \mathbb{N}$ such that there is a map

$$
  E_1 \wedge_X \epsilon^{n_1}
  \longrightarrow
  E_2 \wedge_X \epsilon^{n_2}
$$

over $X$ which is fiberwise a [[weak homotopy equivalence]].

One consider the [[abelian group]] 

$$
  Sph(X) \in Ab
$$

to be the [[Grothendieck group]] of stable fiberwise equivalence classes of spherical fibrations, under fiberwise smash product. 


### Classifying space

There is an associative [[H-space]], $G_n$, of homotopy equivalences of the $(n-1)$-sphere with composition. Then $B G_n$ acts as the [[classifying space]] for spherical fibrations with spherical fibre $S^{n-1}$ ([Stasheff 63](#Stasheff63)).

There is an inclusion of the [[orthogonal group]] $O(n)$ into $G_n$.

Suspension gives a map $G_n \to G_{n+1}$ whose limit is denoted $G$. Then $B G$ classifies stable spherical fibrations.

### As $(\infty,1)$-module bundles

(...)

## Properties

### Adams conjecture

The [[Adams conjecture]] (a theorem) characterizes certain spherical fibrations in the image of the [[J-homomorphism]] as trivial.

### Gysin sequence

The [[long exact sequence in cohomology]] induced by a spherical fibration is called a _[[Gysin sequence]]_.

### Rational homotopy type

See _[[Sullivan model of a spherical fibration]]_.

## Related concepts

* [[sphere spectrum]]

* [[Thom spectrum]]

* [[twisted cohomotopy]]

## References

### General

An original reference is

* [[Albrecht Dold]], [[Richard Lashof]], _Principal quasifibrations and fibre homotopy equivalence of bundles_, 1958 ([pdf](http://www.maths.ed.ac.uk/~aar/papers/doldlashof.pdf))
 {#DoldLashof58}

Treatment of the classifying space for spherical fibrations is in

* {#Stasheff63} [[James Stasheff]], _A classification theorem for fibre spaces_, Topology Volume 2, Issue 3, October 1963, Pages 239-246.


Review:

* {#BottTu82} [[Raoul Bott]], [[Loring Tu]], Chapter 11 of  _[[Differential Forms in Algebraic Topology]]_, Graduate Texts in Mathematics 82, Springer 1982 ([doi:10.1007/BFb0063500](https://doi.org/10.1007/BFb0063500))


* Howard Marcum, Duane Randall, _The homotopy Thom class of a spherical fibration_, Proceedings of the AMS, volume 80, number 2 ([pdf](http://www.maths.ed.ac.uk/~aar/papers/marcum1.pdf))

* Per Holm, Jon Reed, section 7 of _Structure theory of manifolds_, Seminar notes 1971[pdf](http://www.mn.uio.no/math/tjenester/kunnskap/kompendier/seminar-holm.pdf)

* Oliver Straser, Nena R&#246;ttgens, _Spivak normal fibrations_ ([pdf](http://www.map.mpim-bonn.mpg.de/images/b/be/Regensburg2012Talk5.pdf))

* S. Husseini, _Spherical fibrations_ ([pdf](http://www.maths.ed.ac.uk/~aar/papers/husseini2.pdf))

See also:

* Zhongjian Zhu, Jianzhong Pan: *Homotopy types of $S^{2k-1}$-bundles over $S^{2k}$* &lbrack;[arXiv:2508.13800](https://arxiv.org/abs/2508.13800)&rbrack;


### In rational homotopy theory

Discussion in [[rational homotopy theory]] (for more see at _[[Sullivan model of a spherical fibration]]_):

* {#FelixHalperinThomas00} [[Yves Félix]], [[Steve Halperin]], [[Jean-Claude Thomas]], p. 202 of: _Rational Homotopy Theory_, Graduate Texts in Mathematics **205** Springer (2000)

* {#MollerRaussen85} [[Jesper Møller]], [[Martin Raussen]], _Rational Homotopy of Spaces of Maps Into Spheres and Complex Projective Spaces_, Transactions of the American Mathematical Society Vol. 292, No. 2 (Dec., 1985), pp. 721-732 ([jstor:2000242 ](https://www.jstor.org/stable/2000242)) 

* {#CohenVoronov05} [[Ralph Cohen]], [[Alexander Voronov]], _Notes on string topology_ ([arXiv:math/0503625](https://arxiv.org/abs/math/0503625))

* {#FelixOpreaTanre16} [[Yves Félix]], John Oprea, [[Daniel Tanré]], Prop. 2.3 in _Lie-model for Thom spaces of tangent bundles_, Proc. Amer. Math. Soc. 144 (2016), 1829-1840 ([pdf](http://www.ams.org/journals/proc/2016-144-04/S0002-9939-2015-12829-8/S0002-9939-2015-12829-8.pdf), [doi:10.1090/proc/12829](https://doi.org/10.1090/proc/12829))


[[!redirects spherical fibrations]]

[[!redirects sphere bundle]]
[[!redirects sphere bundles]]