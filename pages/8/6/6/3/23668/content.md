[[!redirects dagger 2-posets]]
[[!redirects dagger 2-preorder]]
[[!redirects dagger 2-preorders]]
[[!redirects dagger 2-proset]]
[[!redirects dagger 2-prosets]]
[[!redirects univalent dagger 2-poset]]
[[!redirects univalent dagger 2-posets]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

## Contents ##
* table of contents
{:toc}

## Definition ##

A dagger 2-poset is a [[dagger category]] $C$ such that 

1. for each object $A \in Ob(C)$ and $B \in Ob(C)$ and morphisms $R \in Hom(A, B)$ and $S \in Hom(A, B)$ there is a [[binary relation]] $R \leq_{A, B} S$ 
2. for each object $A \in Ob(C)$ and $B \in Ob(C)$ and morphism $R \in Hom(A, B)$, $R \leq_{A, B} R$. 
3. for each object $A \in Ob(C)$ and $B \in Ob(C)$ and morphisms $R \in Hom(A, B)$ and $S \in Hom(A, B)$, $R \leq_{A, B} S$ and $S \leq_{A, B} R$ implies that $R = S$. 
4. for each object $A \in Ob(C)$ and $B \in Ob(C)$ and morphism $R \in Hom(A, B)$, $S \in Hom(A, B)$, and $T \in Hom(A, B)$, $R \leq_{A, B} S$ and $S \leq_{A, B} T$ implies that $R \leq_{A, B} T$. 
5. for each object $A \in Ob(C)$ and $B \in Ob(C)$ and morphisms $R \in Hom(A, B)$ and $S \in Hom(A, B)$, $R \leq_{A, B} S$ implies $R^\dagger \leq_{B, A} S^\dagger$. 

A dagger 2-poset which only satisfies 1., 2., 4., and 5. is called a **dagger 2-preorder** or a **dagger 2-proset**. 

A dagger 2-poset is a **univalent dagger 2-poset** if the underlying dagger-category is a [[univalent dagger category]]. 

## Morphisms ##

* [[onto morphism in a dagger 2-poset]]
* [[functional morphism in a dagger 2-poset]]
* [[entire morphism in a dagger 2-poset]]
* [[injective morphism in a dagger 2-poset]]
* [[map in a dagger 2-poset]]
* [[category of maps]]
* [[monic map in a dagger 2-poset]]
* [[epic map in a dagger 2-poset]]
* [[unitary isomorphism]]

## Examples ##

* [[semiadditive dagger 2-poset]]
* [[unital dagger 2-poset]]
* [[tabular dagger 2-poset]]
* [[division dagger 2-poset]]
* [[power dagger 2-poset]]
* [[elementarily topical dagger 2-poset]]
* [[W-topical dagger 2-poset]]
* [[well-pointed topical dagger 2-poset]]
* [[coherent dagger 2-poset]]
* [[geometric dagger 2-poset]]
* [[Heyting dagger 2-poset]]
* [[Boolean dagger 2-poset]]
* [[Boolean topical dagger 2-poset]]
* [[allegory]]
* [[groupoid]]
* [[ETCR]]

## See also ##

* [[dagger category]]
* [[2-poset]]