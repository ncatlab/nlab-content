
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

### For strict categories

In set theory, everything is a set, and so the objects of a category form a set, every category is a [[strict category]], and every functor is a [[strict functor]]. Thus, we have the following definition:

\begin{definition}
An **identity-on-objects [[functor]]** $F: A\to B$ between [[categories]] $A$ and $B$ is a functor between categories with the same [[set]] of [[objects]], i.e. $Ob = ob(A) = ob(B)$, and has as its underlying object function $F_{ob}: Ob \to Ob$ the [[identity function]] on $Ob$. 
\end{definition}

This simple definition goes against the [[principle of equivalence]], since it mentions equality of objects, and indeed identity of *sets* of objects. One solution is to alter the definition of equality so that equality is no longer a proposition, such as in type theory. 

However, in type theory, not every category is a strict category anymore, and not every functor is a strict functor anymore. Thus, we have to specifically talk about strict categories and strict functors in our definition:

\begin{definition}
In [[type theory]], an **identity-on-objects [[functor]]** $F: A\to B$ between [[strict categories]] $A$ and $B$ in a [[univalent universe]] $\mathcal{U}$ is a [[strict functor]] between strict categories with the same [[set]] of [[objects]], i.e. there exists a set $Obj:\mathcal{U}$ and [[identity types]] $a:Ob =_\mathcal{U} ob(A)$ and $b:Ob =_\mathcal{U} ob(B)$, and has as its underlying object function $F_{ob}: Ob \to Ob$ the [[identity function]] on $Ob$. 
\end{definition}

The identity types above are [[set]]s. This is in contrast to the situation in [[set theory]] where identity/equality is always a [[proposition]]. 

If the [[type universe]] $\mathcal{U}$ above is not univalent, then one has to replace the identity types with equivalences, which for sets are [[bijections]]: i.e. there exists a set $Obj:\mathcal{U}$ and bijections $a:Ob \simeq_\mathcal{U} ob(A)$ and $b:Ob \simeq_\mathcal{U} ob(B)$, and which its underlying object function $F_{ob}: ob(A) \to ob(B)$ comes with an identity type $p:F_{ob} \circ a =_\mathcal{U} b$, or equivalently, which satisfies the [[commutative square]]

$$\array{& Ob & \overset{a}\rightarrow & ob(A) & \\
          id_{Ob} & \downarrow &&\downarrow & F_{ob}\\
          &Ob & \underset{b}\rightarrow& ob(B) & \\
}$$

This is the same as saying that the underlying object function $F_{ob}: ob(A) \to ob(B)$ is a bijection $F_{ob}: ob(A) \simeq ob(B)$. 

\begin{definition}
An **identity-on-objects [[functor]]** $F: A\to B$ between [[strict categories]] $A$ and $B$ is a [[strict functor]] whose underlying object function $F_{ob}: ob(A) \simeq ob(B)$ is a [[bijection]]. 
\end{definition}

This definition reflects the [[principle of equivalence]] that the true notion of identity between sets is bijection, rather than propositional equality. 

On the other hand, in category theory the notion of "two categories with an identity-on-objects functor between them" is much more commonly used than the notion of "an identity-on-objects functor between two previously given categories". Instead of postulating two categories with a functor whose object function is a bijection, one instead postulates one set or type $Ob$ of objects, with two families of arrows $A(x,y)$ and $B(x,y)$ for $x,y\in Ob$, each with composition and identities making each of $(Ob, A)$ and $(Ob, B)$ into a category structure, plus a family of functions $A(x,y) \to B(x,y)$ commuting with these category structures. This is the approach used to define [[dagger categories]] on the nLab in a way which doesn't violate the [[principle of equivalence]]. 

More abstractly, this can be defined as a category [[enriched category|enriched]] over the [[arrow category]] $Set^\to$.  See also [[M-category]] and [[F-category]].

## Identity-on-objects prefunctors

There is a similar notion of an identity-on-objects prefunctor between [[precategories]], where the objects form a [[type]] or [[infinity-groupoid]] rather than a [[set]]:

\begin{definition}
An **identity-on-objects [[prefunctor]]** $F: A\to B$ between [[precategories]] $A$ and $B$ in a [[univalent universe]] $\mathcal{U}$ is a [[prefunctor]] between precategories with the same [[type]] of [[objects]], i.e. there exists a set $Obj:\mathcal{U}$ and [[identity types]] $a:Ob =_\mathcal{U} ob(A)$ and $b:Ob =_\mathcal{U} ob(B)$, and has as its underlying object function $F_{ob}: Ob \to Ob$ the [[identity function]] on $Ob$. 
\end{definition}

\begin{definition}
An **identity-on-objects [[prefunctor]]** $F: A\to B$ between [[precategories]] $A$ and $B$ is a [[prefunctor]] whose underlying object function $F_{ob}: ob(A) \simeq ob(B)$ is an [[equivalence in homotopy type theory|equivalence of types]] of objects. 
\end{definition}

## Examples

* A dagger precategory is a precategory $\mathcal{C}$ with a contravariant endoprefunctor $\dagger:\mathcal{C}^\op \to \mathcal{C}$ that is an identity-on-objects prefunctor, such that for all objects $A:\mathcal{C}$ and $B:\mathcal{C}$ and morphisms $f:Hom(A,B)$, $(f^\dagger)^\dagger = f$. 

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
