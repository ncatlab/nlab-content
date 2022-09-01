
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

In an [[intensional type theory]] such as [[homotopy type theory]], a [[bicategory]] is **locally univalent** if every [[hom-category]] is a [[univalent category]]. 

More specifically, it is a bicategory $C$ for which the canonical functions 
$$idtoiso^{2,1}(f, g):(f = g) \to inv2cell(f, g)$$
is an equivalence of types for all objects $a:Ob(C)$, $b:Ob(C)$, and morphisms $f:Mor_C(a,b)$ and $g:Mor_C(a,b)$. 

## See also

* [[bicategory]]

## References

* [[Benedikt Ahrens]], Dan Frumin, Marco Maggesi, Niels van der Weide, _Bicategories in Univalent Foundations_ ([arXiv:1903.01152](https://arxiv.org/abs/1903.01152))

[[!redirects locally univalent bicategories]]