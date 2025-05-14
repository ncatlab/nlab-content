
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Directed type theory
+-- {: .hide}
[[!include directed homotopy type theory - contents]]
=--
#### Universes
+-- {: .hide}
[[!include universe - contents]]
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

In [[simplicial homotopy type theory]], let $A$ be a [[Segal type]] and let $x:A \vdash B(x)$ be a [[covariant type family]]. The covariant type family $x:A \vdash B(x)$ satisfies the **directed univalence axiom** if given two elements $x \colon A$ and $y \colon A$ there is an [[equivalence of types]] between the [[hom type]] $\mathrm{hom}_A(x, y)$ and the [[function type]] $B(x) \to B(y)$:

$$
  \mathrm{dua}_A(x, y)
  \;\colon\;
  \mathrm{hom}_A(x, y) 
    \,\simeq\, 
  (B(x) \to B(y))
  \,.
$$

Equivalently, let $I$ denote the directed interval used in the definition of hom-types. Then the directed univalence axiom states that there is an equivalence of types between functions $I \to A$ and functions in $A$:

$$\mathrm{dua}_{I, A, B}:(I \to A) \simeq \sum_{x:A} \sum_{y:A} B(x) \to B(y)$$

## See also

* [[univalence axiom]]

* [[directed homotopy type theory]]

## References

* [[Hoang Kim Nguyen]], *Directed univalence in simplicial sets*, talk in *[Homotopy Type Theory Electronic Seminar Talks](https://www.uwo.ca/math/faculty/kapulkin/seminars/hottest.html)* (March 2023) &lbrack;[video](https://www.youtube.com/watch?v=GgcJqzGvq80), [slides](https://www.uwo.ca/math/faculty/kapulkin/seminars/hottestfiles/Nguyen-2023-03-09-HoTTEST.pdf)&rbrack;

* {#RiehlShulman17} [[Emily Riehl]], [[Michael Shulman]], *A type theory for synthetic $\infty$-categories* $[$[arXiv:1705.07442](https://arxiv.org/abs/1705.07442)$]$

* César Bardomiano Martínez, *Limits and colimits of synthetic $\infty$-categories* $[$[arXiv:2202.12386](https://arxiv.org/abs/2202.12386)$]$

* {#GWB24} [[Daniel Gratzer]], [[Jonathan Weinberger]], [[Ulrik Buchholtz]], *Directed univalence in simplicial homotopy type theory* ([arXiv:2407.09146](https://arxiv.org/abs/2407.09146))

* {#GWB25} [[Daniel Gratzer]], [[Jonathan Weinberger]], [[Ulrik Buchholtz]], *The Yoneda embedding in simplicial type theory* ([arXiv:2501.13229](https://arxiv.org/abs/2501.13229))

[[!redirects directed univalence]]

[[!redirects directed univalent universe]]
[[!redirects directed univalent universes]]

[[!redirects directed univalent]]

[[!redirects directed univalent covariant family]]
[[!redirects directed univalent covariant families]]

[[!redirects directed univalent covariant type family]]
[[!redirects directed univalent covariant type families]]