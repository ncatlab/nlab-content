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