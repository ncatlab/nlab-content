+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--


# Locally univalent bicategories
* table of contents
{:toc}

## Definition

In an [[intensional type theory]] such as [[homotopy type theory]], a [[locally univalent bicategory]] is **univalent** if a Rezk completion condition is satisfied for the objects of the bicategory: equality of objects is [[adjoint equivalence]] of objects. 

More specifically, it is a locally univalent bicategory $C$ for which the canonical function 
$$idtoiso^{2,0}(a, b):(a = b) \to adjequiv(a, b)$$
is an equivalence of types for all objects $a:Ob(C)$, $b:Ob(C)$. 

### In set-level foundations

A univalent bicategory in [[set-level foundations]] is the same thing as a [[locally posetal 2-category|locally posetal]] [[gaunt category]]. 

## See also

* [[bicategory]]

* [[locally univalent bicategory]]

## References

* [[Benedikt Ahrens]], Dan Frumin, Marco Maggesi, Niels van der Weide, _Bicategories in Univalent Foundations_ ([arXiv:1903.01152](https://arxiv.org/abs/1903.01152))

[[!redirects univalent bicategories]]