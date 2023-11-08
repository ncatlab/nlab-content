+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea ##

When working in [[intensional type theory]] such as [[homotopy type theory]], the notion of [[category]] has both a [[precategory]] version and a [[univalent category]] version.  The same is true for other categorical structures, in particular for [[dagger-categories]] we have $\dagger$-precategories and univalent $\dagger$-categories.

## Definition ##

+--{: .un_defn}
###### Definition
A __$\dagger$-precategory__ is defined in type theory using the "family of functions" definition of [[dagger-category]].  Thus, it consists of

* A [[precategory]] $C$, with type of objects $Ob(C)$ and hom-sets $Hom : Ob(C) \to Ob(C) \to Set$.

* For all $A,B:Ob(C)$, a function $(-)^\dagger : Hom(A,B) \to Hom(B,A)$

* For every $A \in Ob(C)$, $(1_A)^\dagger = 1_A$.

* For every $A,B \in Ob(C)$ and every $f \in Hom_C(A,B)$ and $g \in Hom_C(B,C)$, $(g \circ f)^\dagger = f^\dagger \circ g^\dagger$.

* For every $A,B \in Ob(C)$ and every $f \in Hom_C(A,B)$, $((f)^\dagger)^\dagger = f$.
=--

Note that as for any precategory, there is no [[h-level]] restriction on the type $Ob(C)$.  As usual in a $\dagger$-category, we define an isomorphism in a $\dagger$-precategory to be **unitary** if $f^{-1} = f^\dagger$.

Let $(a \cong^\dagger b)$ denote the type of unitary isomorphisms.  The identity morphism is unitary, so there is a function
$$idtouiso : (a=b) \to (a \cong^\dagger b)$$
defined by [induction on identity](identity+type#InTermsOfInductiveTypes).

+--{: .un_defn}
###### Definition
A $\dagger$-precategory is **univalent** (or **saturated**) if $idtouiso$ is an equivalence for all $a,b:Ob(C)$.
=--

We may denote the inverse of $idtouiso$ by $uisotoid$.

## Examples ##

* Every [[univalent groupoid]] is a univalent dagger category with $f^\dagger = f^{-1}$. 

* There is a $\dagger$-precategory [[Rel]] of [[h-sets]] and [[relations]] (i.e. [[Prop]]-valued binary functions), where $f^\dagger$ is the opposite relation of a relation $f$.  Assuming the global [[univalence axiom]], this $\dagger$-category is univalent because an invertible relation is necessarily a function, and hence a bijection.

* There is a $\dagger$-category $Hilb\mathbb{R}$ of Hilbert spaces over the real numbers and linear maps, where $f^\dagger$ is the adjoint linear map of $f$.  This is also univalent, assuming the univalence axiom.

Indeed, if the univalence axiom holds, then most naturally-occurring $\dagger$-categories can be proven to be univalent.

## See also ##

* [[univalence]]

* [[dagger category]]

* [[univalent setoid]]

* [[univalent groupoid]]

* [[poset]]

* [[univalent category]]

## References ##

* [[Univalent Foundations Project]], *[[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]]* (2013): Section 9.7.

* [[Benedikt Ahrens]], [[Paige North]], [[Mike Shulman]], and Dimitris Tsementzis, *The Univalence Principle*, [arxiv](https://arxiv.org/abs/2102.06275) (2021): Example 12.1.

[[!redirects univalent dagger category]]
[[!redirects univalent dagger categories]]
[[!redirects saturated dagger category]]
[[!redirects saturated dagger categories]]
[[!redirects dagger precategory]]
[[!redirects dagger precategories]]

[[!redirects univalent dagger-category]]
[[!redirects univalent dagger-categories]]
[[!redirects saturated dagger-category]]
[[!redirects saturated dagger-categories]]
[[!redirects dagger-precategory]]
[[!redirects dagger-precategories]]

[[!redirects dagger category in homotopy type theory]]
[[!redirects dagger categories in homotopy type theory]]
