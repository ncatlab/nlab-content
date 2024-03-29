+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

An **E-category** is a category [[enriched category|enriched]] over [[setoids]].  This is mainly used in [[dependent type theory]]; from that point of view, it is related to a [[precategory]] but with specified [[equivalence relations]] rather than [[identity type]] as the "equality of morphisms".

## Definition

In [[intensional type theory]], an **E-category** or $\mathcal{C}$ consists of 

* a [[type]] of [[objects]] $Ob(\mathcal{C})$, 
* for each object $A:Ob(\mathcal{C})$ and $B:Ob(\mathcal{C})$, a [[setoid]] $(Hom(A, B), \sim_{Hom(A, B)})$ of [[morphisms]]
* for each object $A:Ob(\mathcal{C})$, $B:Ob(\mathcal{C})$, and $C:Ob(\mathcal{C})$, a [[binary function]] 
$$(-)\circ_{A, B, C}(-) :Hom(B, C) \times Hom(A, B) \to Hom(A, C)$$
such that for each morphism $f:Hom(A, B)$, $g:Hom(A, B)$, $h:Hom(B, C)$ and $k:Hom(B, C)$, there is a witness of extensionality
$$\mathrm{ext}(A, B, C, f, g, h, k):(f \sim_{Hom(A, B)} g) \times (h \sim_{Hom(B, C)} k) \to (h \circ_{A, B, C} f \sim_{Hom(A, C)} k \circ_{A, B, C} g)$$
* for each object $A:Ob(\mathcal{C})$, a morphism $\mathrm{id}_A:Hom(A, A)$
* such that 
  * the composition of morphisms is [[associative]]: for each object $A:Ob(\mathcal{C})$, $B:Ob(\mathcal{C})$, $C:Ob(\mathcal{C})$, and $D:Ob(\mathcal{C})$, and for each morphism $f:Hom(A, B)$, $g:Hom(B, C)$, and $h:Hom(C, D)$, there is a witness of associativity
$$\mathrm{assoc}(A, B, C, D, f, g, h):h \circ_{A, C, D} (g \circ_{A, B, C} f) \sim_{Hom(A, D)} h \circ_{B, C, D} (g \circ_{A, B, D} f)$$
  * the composition of morphisms satisfies the left and right [[unit laws]]: for each object $A:Ob(\mathcal{C})$ and $B :Ob(\mathcal{C})$ and morphism $f:Hom(A, B)$, there are witnesses for left and right unitality
$$\mathrm{lunital}(A, B, f):\mathrm{id}_B \circ_{A, B, B} f \sim_{Hom(A, B)} f$$ 
$$\mathrm{runital}(A, B, f):f \circ_{A, A, B} \mathrm{id}_A \sim_{Hom(A, B)} f$$

## Properties

An E-category is **locally univalent** or a **[[precategory]]** if for all objects $A$ and $B$ and morphisms $f:Hom(A, B)$ and $g:Hom(A, B)$ the canonical function 
$$idtoequivrel(A, B, f, g):f =_{Hom(A, B)} g \to f \sim_{Hom(A, B)} g$$ 
is an equivalence of types.

An isomorphism in a E-category is a morphism $f:Hom(A, B)$ with a morphism $g:Hom(B, A)$ and witnesses 
$$\mathrm{ret}(A, B, f, g): g \circ f \sim_{Hom(A, A)} id_A$$ 
$$\mathrm{sec}(A, B, f, g): f \circ g \sim_{Hom(B, B)} id_B$$
The type of all isomorphisms between $A$ and $B$ is represented by $A \cong_{\mathcal{C}} B$.

An E-category is **univalent**, or a **[[univalent category]]**, if it is locally univalent and for all objects $A$ and $B$ the canonical function 
$$idtoiso(A, B):A =_{Ob(\mathcal{C})} B \to A \cong_{\mathcal{C}} B$$
is an equivalence of types.

## See also

* [[precategory]]

* [[univalent category]]

* [[prebicategory]]

* [[locally univalent bicategory]]

* [[univalent bicategory]]

[[!redirects E-categories]]
[[!redirects e-category]]
[[!redirects e-categories]]
