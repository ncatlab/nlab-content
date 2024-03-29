
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Notions of subcategory
+-- {: .hide}
[[!include notions of subcategory]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A __locally full sub 2-category__ is one whose embedding [[2-functor]] $C\to D$ is [[locally fully faithful 2-functor|locally fully faithful]].  This means that each $C(c_1,c_2)$ is a [[full subcategory]] of $D(c_1, c_2)$.

## Examples

* The sub-2-category of $Prof_{rep} \hookrightarrow$ [[Prof]] on all [[representable profunctor]]s is locally full.

* The sub-2-category of the 2-category $T Alg_l$ of algebras for a [[2-monad]] and [[lax morphisms]] between them contains, as a locally full sub-2-category, the 2-category $T Alg_p$ of algebras and pseudo morphisms (or of strict morphisms, if $T$ is strict).

Both of these examples are also [[wide subcategories]].  A wide and locally full sub-2-category is equivalent to an [[F-category]].  See also [[2-category equipped with proarrows]].


[[!redirects locally full sub-2-categories]]