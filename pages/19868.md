# Initiality Project - Semantics

This page is part of the [[Initiality Project]].

* table of contents
{:toc}

## Idea

See [[categorical model of dependent types]], for now.

## Basic definitions

+--{: .un_defn}
###### Definition
A (natural-model-style) **category with families** (abbreviated **CwF**) consists of:

* a (small) [[category]] $C$
* a [[terminal object]] $1\in C$
* two [[presheaves]] $Tm,Ty \in [C^{op},Set]$
* a morphism $of:Tm \to Ty$
* An *algebraic representation* for the map $of$, i.e. a function assigning to each morphism $A:y \Gamma \to Ty$, where $\Gamma\in C$ and $y$ denotes the [[Yoneda embedding]], an object $\Gamma.A\in C$ and a [[pullback square]]
$$\array{ y(\Gamma.A) & \to & Tm \\ \downarrow &&\downarrow \\ y\Gamma & \xrightarrow{A} & Ty. } $$
=--

Note that an algebraic representation for $of$ can be equivalently expressed as choice of a right adjoint $\mathsf{ext}$ for the corresponding functor of [[category of elements|categories of elements]] $el(Tm) \to el(Ty)$.

We consider categories with families as set-level structures (in particular, as [[strict categories]]), with morphism between them that preserve all the structure "on the nose" rather than merely up to isomorphism.

+--{: .un_defn}
###### Definition
Let $C$ and $D$ be CwFs.  A **CwF morphism** is a functor $F:C\to D$, preserving the specified terminal objects (on the nose), together with a commutative square in $[C^{op},Set]$:
$$\array{ Tm_C & \to & F^*(Tm_D) \\ \downarrow & & \downarrow \\ Ty_C & \to & F^*(Ty_D) }$$
such that, for all $\Gamma \in C$, and $A : y\Gamma \to C$, the square
$$
\array{
y(F(\Gamma.A)) & \to & Tm_D \\
\downarrow & & \downarrow \\
y(F(\Gamma)) & \to & Ty_D
}
$$
is equal (on the nose) to the chosen pullback square corresponding to the morphism $y(F(\Gamma)) \to Ty_D$.
=--

The last condition can be reformulated in terms of categories of elements by requiring that the square of categories and functors
$$
\array{
el(Ty_C) & \to & el(Ty_D) \\
\downarrow & & \downarrow \\
el(Tm_C) & \to & el(Tm_D)
}
$$
commutes strictly, where the vertical maps are the $\mathsf{ext}$ functors corresponding to the chosen algebraic representations and the horizontal maps are $\el (F_*)$ the category of elements functor composed with the direct image functor applied to $F$.

This defines a category $\mathbf{CwF}$ of categories with families and their morphisms, in which we aim to construct an initial object.

## Type structure

Each type forming operation corresponds to structure on a CwF that can be expressed naturally in terms of categorical operations in the presheaf category $[C^{op},Set]$.

### $\Pi$-types

[[!include Initiality Project - Semantics - Pi-types]]

category: Initiality Project
