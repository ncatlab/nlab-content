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

A notion of [[precategory]] which uses the [[equivalence relation]] of [[setoids]] rather than the [[identity type]] of [[h-sets]]. 

## Definition

In [[intensional type theory]], a **(2,1)-preorder** or **locally setoidal prebicategory** $\mathcal{C}$ consists of 

* a [[type]] of [[objects]] $Ob(\mathcal{C})$, 
* for each object $A:Ob(\mathcal{C})$ and $B:Ob(\mathcal{C})$, a [[setoid]] $(Hom(A, B), \sim_{Hom(A, B)})$ of [[morphisms]]
* for each object $A:Ob(\mathcal{C})$, $B:Ob(\mathcal{C})$, and $C:Ob(\mathcal{C})$, a [[binary function]] 
$$(-)\circ_{A, B, C}(-) :Hom(B, C) \times Hom(A, B) \to Hom(A, C)$$
which preserves the setoid equivalence relation
* for each object $A:Ob(\mathcal{C})$, a morphism $\mathrm{id}_A:Hom(A, A)$
* such that 
  * the composition of morphisms is [[associative]]: for each object $A:Ob(\mathcal{C})$, $B:Ob(\mathcal{C})$, $C:Ob(\mathcal{C})$, and $D:Ob(\mathcal{C})$, and for each morphism $f:Hom(A, B)$, $g:Hom(B, C)$, and $h:Hom(C, D)$, 
$$h \circ_{A, C, D} (g \circ_{A, B, C} f) \sim_{Hom(A, D)} h \circ_{B, C, D} (g \circ_{A, B, D} f)$$
  * the composition of morphisms satisfies the left and right [[unit laws]]: for each object $A:Ob(\mathcal{C})$ and $B :Ob(\mathcal{C})$ and morphism $f:Hom(A, B)$, $\mathrm{id}_B \circ_{A, B, B} f \sim_{Hom(A, B)} f$ and $f \circ_{A, A, B} \mathrm{id}_A \sim_{Hom(A, B)} f$.

The latter two axioms are actually inhabitants of the [[equivalence relation]], hence are data included in the definition just like the first four.  However, by definition elements of an equivalence relations are (typally) unique whenever they exist, so in most cases their presence as data can be ignored.

## Properties

A (2,1)-preorder is **locally univalent** or a **[[precategory]]** if for all objects $A$ and $B$ and morphisms $f:Hom(A, B)$ and $g:Hom(A, B)$ the canonical function 
$$idtoequivrel(A, B, f, g):f =_{Hom(A, B)} g \to f \sim_{Hom(A, B)} g$$ 
is an equivalence of types. In a [[univalent type theory]], every setoid is a set and thus every (2,1)-preorder is a precategory. 

An isomorphism in a (2,1)-preorder is a morphism $f:Hom(A, B)$ with a morphism $g:Hom(B, A)$ such that $g \circ f \sim_{Hom(A, A)} id_A$ and $f \circ g \sim_{Hom(B, B)} id_B$. The type of all isomorphisms between $A$ and $B$ is represented by $A \cong_{Ob(\mathcal{C})} B$ and is also a setoid. 

A (2,1)-preorder is **globally univalent** if for all objects $A$ and $B$ the canonical function 
$$idtoiso(A, B):A =_{Ob(\mathcal{C})} B \to A \cong_{Ob(\mathcal{C})} B$$ 
is an equivalence of setoids. 

A (2,1)-preorder is **univalent** or a **[[univalent category]]** if it is both locally univalent and globally univalent. 

A (2, 1)-preorder is **strict** if for all objects $A$ and $B$ the canonical function 
$$idtoproptruncid(A, B):A =_{Ob(\mathcal{C})} B \to \vert A =_{Ob(\mathcal{C})} B \vert$$ 
is an equivalence of types. 

## See also

* [[2-preorder]]

* [[precategory]]

* [[univalent category]]

* [[prebicategory]]

* [[locally univalent bicategory]]

* [[univalent bicategory]]