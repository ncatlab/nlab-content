
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Directed Type Theory
+-- {: .hide}
[[!include directed homotopy type theory - contents]]
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
=--
=--



\tableofcontents

## Idea

In [[dependent type theory]] with a notion of [[hom type]] (i.e. modelling [[(infinity,1)-category|$\infty$-categories]] as envisioned in [[directed homotopy type theory]]) and a notion of [[type universe]], the *directed univalence axiom* for a type universe $U$ states that given two $U$-small types $A \colon U$ and $B \colon U$ there is an [[equivalence of types]] between the hom-type $\mathrm{hom}_U(A, B)$ and the [[function type]] $A \to B$:

$$
  \mathrm{dua}_U(A, B)
  \;\colon\;
  \mathrm{hom}_U(A, B) 
    \,\simeq\, 
  (A \to B)
  \,.
$$

The definition also makes sense in analytic models of [[(infinity,1)-categories]] such as those constructed from [[simplicial sets]]. 

## Definition

### In simplicial homotopy type theory

In [[simplicial homotopy type theory]], a [[Tarski universe]] of [[discrete Segal types]] is a [[Segal type]] $U$ with a type family $A \colon U \vdash T(A) \; \mathrm{type}$ such that given an element $A \colon U$, every type $T(A)$ is a [[discrete Segal type]]. Such a Tarski universe behave similarly to [[Tarski universes]] in traditional [[homotopy type theory]], as the types model [[infinity-groupoids]], and thus the Tarski universe models a [[concrete (infinity,1)-category]]. The Tarski universe of discrete Segal types is **directed univalent** if given two elements $A \colon U$ and $B \colon U$ there is an [[equivalence of types]] between the hom-type $\mathrm{hom}_U(A, B)$ and the [[function type]] $T(A) \to T(B)$:

$$
  \mathrm{dua}_U(A, B)
  \;\colon\;
  \mathrm{hom}_U(A, B) 
    \,\simeq\, 
  (T(A) \to T(B))
  \,.
$$

## See also

* [[univalence axiom]]

* [[directed homotopy type theory]]

## References

* [[Hoang Kim Nguyen]], *Directed univalence in simplicial sets*, talk in *[Homotopy Type Theory Electronic Seminar Talks](https://www.uwo.ca/math/faculty/kapulkin/seminars/hottest.html)* (March 2023) &lbrack;[video](https://www.youtube.com/watch?v=GgcJqzGvq80), [slides](https://www.uwo.ca/math/faculty/kapulkin/seminars/hottestfiles/Nguyen-2023-03-09-HoTTEST.pdf)&rbrack;

[[!redirects directed univalence]]