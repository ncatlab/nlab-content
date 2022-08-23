
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

\begin{definition}
An **identity-on-objects [[functor]]** $F: A\to B$ between [[categories]] $A$ and $B$ is a functor between categories with the same [[set]] of [[objects]], i.e. $Ob = ob(A) = ob(B)$, and has as its underlying object function $F_{ob}: Ob \to Ob$ the [[identity function]] on $Ob$. 
\end{definition}

This definition is problematic for multiple different reasons. First of all, it mentions equality of sets, which means that the definition is not even definable in a [[structural set theory]] such as [[SEAR]] or [[ETCS with elements]], where there is no notion of equality of sets, only equality of [[functions]], [[relations]], and [[elements]]. In structural set theories, instead of talking about equality of sets, one talks about having a [[bijection]] between sets. This gives us the alternative definition suitable for structural set theories:

\begin{definition}
An **identity-on-objects [[functor]]** $F: A\to B$ between [[categories]] $A$ and $B$ is a [[functor]] whose underlying object function $F_{ob}: ob(A) \to ob(B)$ is a [[bijection]] $F_{ob}: ob(A) \simeq ob(B)$. 
\end{definition}

However, this definition still goes against the [[principle of equivalence]], since it mentions equality of objects. This is a limitation of all definitions of categories based in [[set theories]], since every object is a set, every category is a [[strict category]], and thus has equality of objects. 

One solution is to alter the definition of equality so that equality is no longer a proposition, such as the case in [[type theory]], and accordingly alter the definition of category to reflect that equality of objects is no longer a proposition. 

### Type theoretic definition

In type theory, the objects of a category form a general type, rather than a set, which means that categories are not in general strict categories anymore, nor are functors in general strict functors. Moreover, the proper of notion of equality between types is not [[bijection]] (as those are limited to sets), but rather [[equivalence in homotopy type theory|type equivalence]]: a function $f:A \to B$ where for all elements $b:B$ the fiber of $f$ at $b$ is a singleton. This suggests the following definition of an identity-on-objects functor:

\begin{definition}
An **identity-on-objects [[functor]]** $F: A\to B$ between [[categories]] $A$ and $B$ is a [[functor]] whose underlying object function $F_{ob}: ob(A) \to ob(B)$ is an [[equivalence in homotopy type theory|equivalence of types]] $F_{ob}: ob(A) \simeq ob(B)$. 
\end{definition}

However, in type theory, there *is* a way to also speak about equality of types, provided that both types live in a [[univalent universe]] $\mathcal{U}$. For types $A:\mathcal{U}$ and $B:\mathcal{U}$, there is an [[identity type]] $A =_\mathcal{U} B$ and a type of equivalences between $A$ and $B$, $A \simeq_\mathcal{U} B$, as well as a canonical function 
$$\mathrm{IdtoEquiv}:A =_\mathcal{U} B \to A \simeq_\mathcal{U} B$$
Since $\mathcal{U}$ is univalent, $\mathrm{IdtoEquiv}$ is an equivalence of types 
$$\mathrm{IdtoEquiv}:A =_\mathcal{U} B \simeq A \simeq_\mathcal{U} B$$
and thus there is a homotopy inverse 
$$\mathrm{EquivtoId}:A \simeq_\mathcal{U} B \to A =_\mathcal{U} B$$ 
This provides us with a definition which both talks about equality of objects and satisfies the principle of equivalence:

\begin{definition}
An **identity-on-objects [[functor]]** $F: A\to B$ between [[categories]] $A$ and $B$ in a [[univalent universe]] $\mathcal{U}$  is a [[functor]] with an [[identification]] $\mathrm{EquivtoId}(F_{ob}):ob(A) =_\mathcal{U} ob(B)$, where whose $F_{ob}: ob(A) \to ob(B)$ is the underlying object function of the functor $F$.
\end{definition}

### Insert title here

On the other hand, in category theory the notion of "two categories with an identity-on-objects functor between them" is much more commonly used than the notion of "an identity-on-objects functor between two previously given categories". Instead of postulating two categories with a functor whose object function is a bijection, one instead postulates one set or type $Ob$ of objects, with two families of arrows $A(x,y)$ and $B(x,y)$ for $x,y\in Ob$, each with composition and identities making each of $(Ob, A)$ and $(Ob, B)$ into a category structure, plus a family of functions $A(x,y) \to B(x,y)$ commuting with these category structures. This is the approach used in two separate definitions of [[dagger categories]] on the nLab. 

More abstractly, this can be defined as a category [[enriched category|enriched]] over the [[arrow category]] $Set^\to$.  See also [[M-category]] and [[F-category]].

## Examples

* Every [[equivalence of categories]] between two categories is an identity-of-objects functor where additionally the morphism functions of the functor are [[bijections]]. 

* A [[dagger category]] is a category $\mathcal{C}$ with a [[contravariant functor|contravariant endofunctor]] $\dagger:\mathcal{C}^\op \to \mathcal{C}$ that is an identity-on-objects functor, such that for all objects $A:\mathcal{C}$ and $B:\mathcal{C}$ and morphisms $f:Hom(A,B)$, $(f^\dagger)^\dagger = f$. 

## Related pages

* [[Freyd category]]
* [[Freyd multicategory]]
* [[dagger category]]
* [[principle of equivalence]]

[[!redirects identity-on-objects functors]]
[[!redirects identity on objects functor]]
[[!redirects identity on objects functors]]
[[!redirects io functor]]
[[!redirects io functors]]
[[!redirects i.o. functor]]
[[!redirects i.o. functors]]

[[!redirects identity-on-objects prefunctor]]
[[!redirects identity-on-objects prefunctors]]
[[!redirects identity on objects prefunctor]]
[[!redirects identity on objects prefunctors]]
[[!redirects io prefunctor]]
[[!redirects io prefunctors]]
[[!redirects i.o. prefunctor]]
[[!redirects i.o. prefunctors]]
