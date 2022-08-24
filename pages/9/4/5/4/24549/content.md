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

In [[type theory]], the concept of a [[bijective-on-objects functor]] is only valid for [[categories]] whose type forms a [[set]], i.e. [[strict categories]]. However, we would want a similar notion for general categories. Thus, comes the concept of equivalent-on-objects functor. 

## Definition

A function $f:A \to B$ between two types $A$ and $B$ is an [[equivalence in homotopy type theory|equivalence]] if for all elements $b:B$ the fiber of $f$ at $b$ is a singleton. This suggests the following definition of an identity-on-objects functor:

\begin{definition}
An **identity-on-objects [[functor]]** $F: A\to B$ between [[categories]] $A$ and $B$ is a [[functor]] whose underlying object function $F_{ob}: ob(A) \to ob(B)$ is an [[equivalence in homotopy type theory|equivalence of types]] $F_{ob}: ob(A) \simeq ob(B)$. 
\end{definition}

## Properties

### Relation to identity-on-objects functors

If both categories live in a [[univalent universe]] $\mathcal{U}$, an equivalent-on-objects functor also becomes an [[identity-on-objects functor]] due to the [[univalence axiom]]: 

For types $A:\mathcal{U}$ and $B:\mathcal{U}$, there is an [[identity type]] $A =_\mathcal{U} B$ and a type of equivalences between $A$ and $B$, $A \simeq_\mathcal{U} B$, as well as a canonical function $\mathrm{IdtoEquiv}:A =_\mathcal{U} B \to A \simeq_\mathcal{U} B$. Since $\mathcal{U}$ is univalent, $\mathrm{IdtoEquiv}$ is an equivalence of types $\mathrm{IdtoEquiv}:A =_\mathcal{U} B \simeq A \simeq_\mathcal{U} B$ and thus there is a homotopy inverse $\mathrm{EquivtoId}:A \simeq_\mathcal{U} B \to A =_\mathcal{U} B$. Thus, in an univalent universe, equivalent-on-objects functors and identity-on-objects functors are the same:

\begin{definition}
An **identity-on-objects [[functor]]** $F: A\to B$ between [[categories]] $A$ and $B$ in a [[univalent universe]] $\mathcal{U}$ is a [[functor]] with an [[identification]] $\mathrm{EquivtoId}(F_{ob}):ob(A) =_\mathcal{U} ob(B)$, where $F_{ob}: ob(A) \to ob(B)$ is the underlying object function of the functor $F$.
\end{definition}

### Relation to bijective-on-objects functors

For [[strict categories]], an equivalent-on-objects functor is a [[bijective-on-objects functor]], as equivalence of sets is [[bijection]] of sets, and the type of objects for strict categories is a set. 

### Relation to essentially surjective functors. 

For [[univalent categories]], an equivalent-on-objects functor is a [[essentially surjective functor]]. This is because the type of objects of every [[univalent category]] is a [[groupoid]]/[[1-truncated]], which means that equivalence of the object types is [[equivalence of groupoids]] and thus essentially surjective. 

An isomorphism of categories is a [[fully faithful functor|fully faithful]] equivalent-on-objects functor. As a result, every [[adjoint equivalence]] of [[univalent categories]] is an isomorphism of univalent categories, since every adjoint equivalence is essentially surjective. 

## See also

* [[identity-on-objects functor]]
* [[bijective-on-objects functor]]
* [[essentially surjective functor]]

## References

For the definition of isomorphism of categories and adjoint equivalence of univalent categories, and equivalence of the two definitions for functors between univalent categories: 

* Univalent Foundations Project, [[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)