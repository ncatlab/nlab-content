+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definitions

### Abstract definition

\begin{definition}
**Two categories with the same collection of objects with an identity-on-objects functor** is a category $C$ enriched in the [[arrow category]] $Set^I$ of [[Set]]. 
\end{definition}

See also [[M-category]] and [[F-category]].

### By components

First, we distinguish between a [[category]], and a category structure on a [[collection]] of [[objects]], in the same way one does between a [[proset]] and a [[preorder]], the equivalence relation structure on a collection of objects, in (0, 1)-category theory. 

\begin{definition}
A **category structure** on a collection of objects $Ob$ is a family of sets $Mor(x, y)$ whose elements are called morphisms, indexed by objects $x:Ob$ and $y:Ob$, such that

* for each object $x:Ob$, a morphism $\mathrm{id}_x:Mor(x, x)$
* for each object $x:Ob$, $y:Ob$, and $z:Ob$, a function $\circ_{x, y, z}:Mor(y, z) \times Mor(x, y) \to Mor(x, z)$

such that 

* for each object $x:Ob$ and $y:Ob$ and morphism $f:Mor(x, y)$, $f \circ_{x, y, z} \mathrm{id}_x = \mathrm{id}_x$ and $\mathrm{id}_y \circ_{x, y, z} f = \mathrm{id}_y$. 
* for each object $x:Ob$, $y:Ob$, $z:Ob$, $w:Ob$ and morphism $f:Mor(x, y)$, $g:Mor(y, z)$, $h:Mor(z, w)$, 
$$h \circ_{x, z, w} (g \circ_{x, y, z} f) = (h \circ_{y, z, w} g) \circ_{x, y, w} f$$ 

\end{definition}

\begin{definition}
A **category** $C$ is a collection $Ob$ with a category structure $Mor(x, y)$ indexed by objects $x:Ob$ and $y:Ob$. 
\end{definition}

\begin{definition}
**Two categories with the same collection of objects** $A$ and $B$ is a collection $Ob$ with two category structures $Mor_A(x, y)$ and $Mor_B(x, y)$ indexed by objects $x:Ob$ and $y:Ob$. The categories $A$ and $B$ are defined to be $(Ob, Mor_A)$ and $(Ob, Mor_B)$ respectively. 
\end{definition}

\begin{definition}
**An identity-on-objects functor** between two categories with the same collection of objects $A$ and $B$ is a family of functions $F_{Mor}(x, y):Mor_A(x, y) \to Mor_B(x, y)$ which preserve the category structure on the type families:

* [[composition]] of [[morphisms]] is preserved: for all morphisms $f:Mor_A(x, y)$ and $g:Mor_B(y, z)$, $F_{Mor}(x, z)(g \circ^A_{x, y, z} f) = F_{Mor}(y, z)(g) \circ^B_{x, y, z} F_{Mor}(x, y)(f)$,

* identity morphisms are preserved: $F_{Mor}(x, x)(id^A_x) = id^B_x$.
 
\end{definition}

### Historical note

#### The notion of two categories with the same collection of objects

What does it mean for two categories to have the same collection of objects? 

The current definition defines such a structure as having one collection of object and two category structures. In [[type theory]], this could equivalently be defined as actually two categories $A$ and $B$ whose collections of objects are [[judgmental equality|judgmentally equal]] to each other: $Ob_A \equiv Ob_B$. 

Historically, authors have tried to use [[propositional equality]] to define two categories with the same collection of objects. However, this runs into a number of problems: 

* In [[material set theories]], one could postulate the condition that $Ob = ob(A) = ob(B)$. However, it mentions equality of sets, which means that the definition violates the [[principle of equivalence]]. 

* In [[structural set theory]] such as [[SEAR]] or [[ETCS with elements]], one can't use equality of sets to define "having the same object", since where there is no notion of equality of sets, only equality of [[functions]], [[relations]], and [[elements]]. One could instead use [[bijection]], but that leads to a different concept, the notion of [[bijective-on-objects functor]]. 

* In type theory, [[propositional equality]] is represented by the [[identity type]] or the [[path type]], but doesn't actually have to be valued in [[propositions]]. One postulates the existence of [[identifications]] $a:Ob =_\mathcal{U} ob(A)$ and $b:Ob =_\mathcal{U} ob(B)$, resulting in an identification $a^{-1} b: ob(A) =_\mathcal{U} ob(B)$. But this is additional structure in type theory which results in a different mathematical object than the current definition of an identity-on-objects functor. Additionally, the definition is only valid if the categories are in a [[type universe]]. For categories which don't belong to any universe, one could instead use [[equivalence in homotopy type theory|equivalence]], but that leads to a different concept, the notion of [[equivalent-on-objects functor]]. 

Hence, the notion of "two categories with the same collection of objects" is somewhat of a [[red herring principle|red herring]], because it is defined as an object with two category structures, rather than two categories with the same collection of objects. 

#### Is the identity-on-objects functor a functor?

Historically, the notion of **identity-on-objects functor** in between two categories with the same collection of objects was defined to be an actual functor, additionally having a function on the objects $F_{Ob}:Ob_C \to Ob_C$ which is the [[identity function]] on $Ob_C$. This was where the original name "identity-on-objects functor" comes from. The problem with this definition is twofold: 

* In a [[material set theory]] or [[structural set theory]] or a type theory with [[axiom K]], the above definition violates the [[principle of equivalence]] if one were to use it to define concrete [[dagger categories]] such as [[Rel]], [[Hilb]] or concrete [[groupoids]] such as the [[permutation category]], since in those cases the definition explicitly refers to [[propositional equality]] of [[sets]]. 

* In a [[univalent type theory]], [[identity functions]] do not necessarily violate the [[principle of equivalence]], because the [[identity type]] $id(x) =_Ob x$ for object $x:A$ is not necessarily a proposition, and in the presence of [[univalence]], is necessarily required to satisfy the [[principle of equivalence]]. However, the [[identifications]] $p(x):id(x) =_Ob x$ are additional structure on the mathematical object, and thus does not result in the same object as the definitions above do. 

As a result, the current definition of an identity-on-objects functor, valid in all foundations and respecting the [[principle of equivalence]], was adopted, which doesn't have such an identity function on the objects. However, the name "identity-on-objects functor" then becomes a [[red herring principle|red herring]], since it is not actually a [[functor]] between the two objects collections. 

## Contravariant endofunctor which is the identity-on-objects

Sometimes we want an identity-on-objects functor which behaves like a [[contravariant functor|contravariant]] [[endofunctor]]. In this case, one does not need the notion of "two categories with the same collection of objects". 

\begin{definition}
A **contravariant endofunctor which is the identity-on-objects** on a category $C$ is a family of functions $F_{Mor}(x, y):Mor(x, y) \to Mor(y, x)$ such that 

* [[composition]] of [[morphisms]] is reversed: for all morphisms $f: Mor_A(x, y)$ and $g:Mor_B(y, z)$, $F_{Mor}(x, z)(g \circ_{x, y, z} f) = F_{Mor}(x, y)(f) \circ_{x, y, z} F_{Mor}(y, z)(g)$,

* identity morphisms are preserved: $F_{Mor}(x, x)(id_x) = id_x$.
 
\end{definition}

This is used in particular for defining [[dagger categories]] and [[groupoids]]. 

## Examples

* A [[dagger category]] is a category $\mathcal{C}$ with an identity-on-objects contravariant endofunctor $(-)^{\dagger_{A, B}}:Mor(A,B) \to Mor(B, A)$, such that for all objects $A:\mathcal{C}$ and $B:\mathcal{C}$ and morphisms $f:Hom(A,B)$, $(f^{\dagger_{A, B}})^{\dagger_{B, A}} = f$. 

* A [[groupoid]] is a category $\mathcal{C}$ with an identity-on-objects contravariant endofunctor $(-)^{(-1)_{A, B}}:Mor(A,B) \to Mor(B, A)$ such that for all objects $A:\mathcal{C}$ and $B:\mathcal{C}$ and morphisms $f:Hom(A,B)$, $f \circ f^{(-1)_{A, B}} = id_B$ and $f^{(-1)_{A, B}} \circ f = id_A$. 

## Related pages

* [[bijective-on-objects functor]]
* [[equivalent-on-objects functor]]
* [[essentially surjective functor]] 
* [[displayed category]]
* [[Freyd category]]
* [[Freyd multicategory]]
* [[dagger category]]
* [[principle of equivalence]]

[[!redirects identity-on-objects]]
[[!redirects identity on objects]]

[[!redirects identity-on-objects functor]]
[[!redirects identity-on-objects functors]]
[[!redirects identity on objects functor]]
[[!redirects identity on objects functors]]
[[!redirects io functor]]
[[!redirects io functors]]
[[!redirects i.o. functor]]
[[!redirects i.o. functors]]
