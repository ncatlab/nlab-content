[[!redirects categories with the same collection of objects]]
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

+-- {: .query}
This page is currently under major revision. See the nForum's discussion post on this article for more information. Feel free to contribute. 
=--

## Definition

A **category with an atlas** is a [[category]] $C$ equipped with with a [[set]] $G$ and an [[essentially surjective functor]] $F:G \to C$, where the set $G$ is considered as a [[discrete category]].

## See also

* [[atlas]]

## Idea

When category theorists say that two categories have the same collection of objects, they usually mean that there is one collection of objects $Ob$, and two families of sets $A(x, y)$ and $B(x, y)$ for objects $x:Ob$ and $y:Ob$, such that $(Ob, A)$ is a category and $(Ob, B)$ is also a category. 

## Definition

In this article, we are foundations agnostic, and thus use the foundations-neutral term 'collection' for type/class/set. In a certain foundation, one usually sees this structure referred to as 'categories with the same type of objects', 'categories with the same class of objects', or 'categories with the same set of objects'. 

First, we distinguish between a [[category]], and a category structure on a collection of [[objects]], in the same way one does between a [[proset]] and a [[preorder]], the equivalence relation structure on a collection of objects, in (0, 1)-category theory. 

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
A **family of categories with the same collection of objects** $C(a)$ indexed by elements $a:A$ of the index collection $A$ is a collection $Ob$ with a family of category structures $Mor(a)(x, y)$, indexed by elements $a:A$ and objects $x:Ob$ and $y:Ob$. Each category $C(a)$ is defined to be $(Ob, Mor(a))$ for all elements $a:A$. 
\end{definition}

### Historical note

Historically, there were other attempts to defining what it means for two categories with the same collection of objects, all of which involve some form of [[propositional equality]] or [[equivalence]] between the object collections $ob(A)$ and $ob(B)$ of the categories $A$ and $B$. 

In set theory, the objects of a category are required to be a set. In [[material set theories]], one could postulate the condition that $ob(A) = ob(B)$. However, it mentions equality of sets, which means that the definition is not even definable in a [[structural set theory]] such as [[SEAR]] or [[ETCS with elements]], where there is no notion of equality of sets, only equality of [[functions]], [[relations]], and [[elements]]. In structural set theories, instead of talking about equality of sets, one talks about having a [[bijection]] between sets and $F_{ob}:ob(A) \cong ob(B)$. 

In type theory, the objects of a category do not form a set, but a type. The categories whose type of objects is a set is a strict category, and as a result, the above definitions are only valid for [[strict categories]]. However, there is a generalization of both material set theory equality of sets and structural set theory bijection of sets to type theory: identity types and equivalence of types. For identity types, one postulates the existence of an [[identification]] $p:ob(A) =_\mathcal{U} ob(B)$. For equivalences, one postulates the existence of [[equivalence in homotopy type theory|equivalence]] $F_{ob}:ob(A) \simeq_\mathcal{U} ob(B)$. 

However, in general categories, when defining an [[identity-on-objects functor]] (see below), all these definitions violate the [[principle of equivalence]]. The issue is that they either refer to equality on sets, such as in [[material set theory]], or refer to either type theoretic [[identity-on-objects functors]], [[bijective-on-objects functors]], or [[equivalent-on-objects functors]], while what one actually needs are [[essentially surjective functors]]. 

Only in [[univalent categories]] are essentially surjective functors the same as equivalent-on-object functors, and additionally only when both the source and target univalent categories are in a [[univalent universe]] are essentially surjective functors between univalent categories type-theoretic identity-on-object functors. 

Thus, category theorists have resorted to the current definition above if they need a concept of categories with the same collection of objects, as that definition does not violate the [[principle of equivalence]]. 

## Functors between categories with the same collection of objects

\begin{definition}
Let $(Ob, Mor_A, Mor_B)$ be two categories with the same collection of objects. Then a **functor** $F:A \to B$ between categories $A \coloneqq (Ob, Mor_A)$ and $B \coloneqq (Ob, Mor_B)$ is an [[endofunction]] $F_{ob}:Ob \to Ob$ with a family of functions $F_{x, y}:Mor_A(x, y) \to Mor_B(x, y)$
\end{definition}

## Identity-on-objects functor

\begin{definition}
An **[[identity-on-objects functor]]** $F: A\to B$ between two categories with the same collection of objects $(A, B) \coloneqq (Ob, Mor_A, Mor_B)$ is a family of functions $F_{x, y}:Mor_A(x, y) \to Mor_B(x, y)$ indexed by objects $x:Ob$ and $y:Ob$. 
\end{definition}

In contrast to its name, an identity-on-objects functor is *not* a functor as defined above. On the other hand, every functor *is* an identity-on-objects functor between two categories with the same collection of objects. This is an example of the [[red herring principle]]. 

## See also

* [[identity-on-objects functor]]
* [[Freyd category]]
* [[Freyd multicategory]]
* [[dagger category]]

[[!redirects categories with the same type of objects]]
[[!redirects categories with the same class of objects]]
[[!redirects categories with the same set of objects]]

[[!redirects functor between categories with the same collection of objects]]
[[!redirects functor between categories with the same type of objects]]
[[!redirects functor between categories with the same class of objects]]
[[!redirects functor between categories with the same set of objects]]

[[!redirects functors between categories with the same collection of objects]]
[[!redirects functors between categories with the same type of objects]]
[[!redirects functors between categories with the same class of objects]]
[[!redirects functors between categories with the same set of objects]]