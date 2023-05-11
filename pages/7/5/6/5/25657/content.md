
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
#### Universes
+-- {: .hide}
[[!include universe - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--

\tableofcontents

## Idea

In [[dependent type theory]] with a notion of [[hom]]-[[type]] (i.e. for an [[(infinity,1)-category]]) and a notion of [[type universe]], the directed univalence axiom for a universe $U$ states that given two $U$-small types $A:U$ and $B:U$ there is an [[equivalence of types]] between the hom-type $\mathrm{hom}_U(A, B)$ and the [[function type]] $A \to B$:

$$\mathrm{dua}_U(A, B):\mathrm{hom}_U(A, B) \simeq (A \to B)$$

The definition also makes sense in analytic models of [[(infinity,1)-categories]] such as those constructed from [[simplicial sets]]. 

## See also

* [[univalence axiom]]
* [[directed homotopy type theory]]

## References

* [[Hoang Kim Nguyen]], *Directed univalence in simplicial sets*, ([video](https://www.youtube.com/watch?v=GgcJqzGvq80), [slides](https://www.uwo.ca/math/faculty/kapulkin/seminars/hottestfiles/Nguyen-2023-03-09-HoTTEST.pdf))

[[!redirects directed univalence]]