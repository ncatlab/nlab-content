
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The concept of an [[identity-on-objects functor]] is important for defining various structures in [[category theory]], such as [[Freyd categories]] and [[dagger categories]]. However, in a [[structural set theory]] such as [[ETCS]] or [[SEAR]], there is no concept of [[equality]] of [[sets]], and thus, an [[identity-on-objects functor]] cannot be defined via the usual definition. Instead, equality of sets is expressed through [[bijection]] of sets, which, when applied to the definition of identity-on-objects functor, yields a bijective-on-objects functor. 

In [[foundations]] where categories are weak by default and thus the collection of objects do not form a set, the concept of a bijective-on-objects functor still makes sense for [[strict categories]], where the functor is a [[strict functor]] by definition. 

Another motivation for bijective-on-objects functors is that they together with [[full and faithful functors|full and faithful]] [[strict functors]] form an [[weak factorization system|orthogonal factorization system]] on [[StrCat]]; see [[bo-ff factorization system]]. This factorization system can also be constructed using a [[generalized kernel]].

## Definition

\begin{definition}
A [[strict functor]] between two [[strict categories]] $A$ and $B$ is called **bijective-on-objects**, or **bo**, if it is a [[bijection]] on [[objects]], if its underlying object function $F_{ob}: ob(A) \to ob(B)$ is a [[bijection]] $F_{ob}: ob(A) \simeq ob(B)$. 
\end{definition}

## Principle of equivalence

To be more in accord with the [[principle of equivalence]], one could require that the functor be bijective on objects only up to isomorphism; that is, it is [[essentially surjective functor|essentially surjective]] and [[full functor|full]] on isomorphisms.  However, from the point of view of [[factorization systems]], the version of the concept of a  bo functor which is in accord with the [[principle of equivalence]] is nothing more or less than an [[essentially surjective functor]], since essentially surjective functors and ff functors form a bicategorical factorization system on the [[bicategory]] $Cat$.

## Properties

[[R. Street]] in _[Categorical and combinatorial aspects of descent theory](http://arxiv.org/pdf/math/0303175)_ proves

Proposition. A functor is bijective on objects if and only if it exhibits its
codomain as the (2-categorical) [[descent object|codescent object]] of some simplicial category.

This can be generalized to any [[regular 2-category]].

### Relation to equivalent-on-objects functors

Every bijective-on-objects functor between two strict categories is an [[equivalent-on-objects functor]] between two strict categories. 

### Relation to identity-on-objects functors

In the context of [[type theory]], if both strict categories live in a [[univalent universe]] $\mathcal{U}$, a bijective-on-objects functor also becomes an [[identity-on-objects functor]] due to the [[univalence axiom]] and the fact that equivalences between sets are equivalent to bijections of sets: 

For sets $A:\mathcal{U}$ and $B:\mathcal{U}$, there is an [[identity type]] $A =_\mathcal{U} B$, a type of equivalences between $A$ and $B$, $A \simeq_\mathcal{U} B$, and a type of bijections between $A$ and $B$, $A \cong_\mathcal{U} B$, as well as canonical canonical functions $\mathrm{IdtoEquiv}:A =_\mathcal{U} B \to A \simeq_\mathcal{U} B$ and $\mathrm{IdtoBij}:A =_\mathcal{U} B \to A \cong_\mathcal{U} B$. 

Since between equivalences between sets are equivalent to bijections between sets, there is a function $\mathrm{EquivtoBij}:A \simeq_\mathcal{U} B \simeq A \cong_\mathcal{U} B$ which is an equivalence of types. 

Since $\mathcal{U}$ is univalent, $\mathrm{IdtoEquiv}$ is an equivalence of types $\mathrm{IdtoEquiv}:A =_\mathcal{U} B \simeq A \simeq_\mathcal{U} B$. By the properties of equivalences, the function $\mathrm{IdtoBij}$ is also an equivalence of types $\mathrm{IdtoBij}:A =_\mathcal{U} B \simeq A \cong_\mathcal{U} B$. Thus there is a homotopy inverse $\mathrm{BijtoId}:A \simeq_\mathcal{U} B \to A =_\mathcal{U} B$. 

Thus, in an univalent universe, bijective-on-objects functors and identity-on-objects functors are the same:

\begin{definition}
An **identity-on-objects [[functor]]** $F: A\to B$ between [[strict categories]] $A$ and $B$ in a [[univalent universe]] $\mathcal{U}$ is a [[strict functor]] with an [[identification]] $\mathrm{BijtoId}(F_{ob}):ob(A) =_\mathcal{U} ob(B)$, where $F_{ob}: ob(A) \to ob(B)$ is the underlying object function of the functor $F$.
\end{definition}

## Related pages

* [[strict category]]
* [[identity-on-objects functor]]
* [[equivalent-on-objects functor]]
* [[essentially surjective functor]]

[[!include properties of functors -- contents]]

[[!redirects bijective-on-objects]]
[[!redirects bijective on objects]]

[[!redirects bijective on objects functor]]
[[!redirects bijective on objects functors]]

[[!redirects bijective-on-objects functor]]
[[!redirects bijective-on-objects functors]]


[[!redirects bo functor]]
[[!redirects bo functors]]

[[!redirects b.o. functor]]
[[!redirects b.o. functors]]

