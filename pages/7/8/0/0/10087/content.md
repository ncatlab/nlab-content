
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _spherical fibration_ is a [[fiber bundle]] of [[homotopy types]] of [[spheres]] of some [[dimension]]. Typically this is considered after [[stabilization]] (hence up to tensoring with trivial spherical fibrations)  which makes spherical fibrations models for [[(∞,1)-module bundles]] for the [[sphere spectrum]] regarded as an [[E-∞ ring]].

Every real [[vector bundle]] becomes a spherical fibration upon removing its [[zero section]] and this construction induces a map from vector bundles and in fact from [[topological K-theory]] to spherical fibrations, called the _[[J-homomorphism]]_.


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

### As $(\infty,1)$-module bundles

(...)

## Properties

### Adams conjecture

The [[Adams conjecture]] (a theorem) characterizes certain spherical fibrations in the image of the [[J-homomorphism]] as trivial.

### Gysin sequence

The [[long exact sequence in cohomology]] induced by a spherical fibration is called a _[[Gysin sequence]]_.

## Related concepts

* [[sphere spectrum]]

* [[Thom spectrum]]

## References

An original reference is

* [[Albrecht Dold]], [[Richard Lashof]], _Principal quasifibrations and fibre homotopy equivalence of bundles_, 1958 ([pdf](http://www.maths.ed.ac.uk/~aar/papers/doldlashof.pdf))
 {#DoldLashof58}

Reviews include

* Howard Marcum, Duane Randall, _The homotopy Thom class of a spherical fibration_, Proceedings of the AMS, volume 80, number 2 ([pdf](http://www.maths.ed.ac.uk/~aar/papers/marcum1.pdf))

* Per Holm, Jon Reed, section 7 of _Structure theory of manifolds_, Seminar notes 1971[pdf](http://www.mn.uio.no/math/tjenester/kunnskap/kompendier/seminar-holm.pdf)

* Oliver Straser, Nena R&#246;ttgens, _Spivak normal fibrations_ ([pdf](http://www.map.mpim-bonn.mpg.de/images/b/be/Regensburg2012Talk5.pdf))


* S. Husseini, _Spherical fibrations_ ([pdf](http://www.maths.ed.ac.uk/~aar/papers/husseini2.pdf))


[[!redirects spherical fibrations]]

[[!redirects sphere bundle]]
[[!redirects sphere bundles]]