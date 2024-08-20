+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

\tableofcontents

## Definition

In an [[intensional type theory]] such as [[homotopy type theory]], a [[bicategory]] is **globally univalent** if a Rezk completion condition is satisfied for the objects of the bicategory: equality of objects is [[adjoint equivalence]] of objects. 

More specifically, it is a bicategory $C$ for which the canonical function 
$$idtoiso^{2,0}(a, b):(a = b) \to adjequiv(a, b)$$
is an equivalence of types for all objects $a:Ob(C)$, $b:Ob(C)$. 

## See also

* [[bicategory]]

* [[locally univalent bicategory]]

* [[univalent bicategory]]

## References

* [[Benedikt Ahrens]], [[Dan Frumin]], [[Marco Maggesi]], [[Niels van der Weide]], _Bicategories in Univalent Foundations_, Mathematical Structures in Computer Science **31** 10 (2022) 1232-1269 &lbrack;[arXiv:1903.01152](https://arxiv.org/abs/1903.01152), [doi:10.1017/S0960129522000032](https://doi.org/10.1017/S0960129522000032)&rbrack

[[!redirects globally univalent bicategories]]


