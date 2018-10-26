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
* two [[presheaves]] $Tm,Ty \in [C^{op},Set]$
* a morphism $of:Tm \to Ty$
* An *algebraic representation* for the map $of$, i.e. a function assigning to each morphism $A:y \Gamma \to Ty$, where $\Gamma\in C$ and $y$ denotes the [[Yoneda embedding]], an object $\Gamma.A\in C$ and a [[pullback square]]
$$\array{ y(\Gamma.A) & \to & Tm \\ \downarrow &&\downarrow \\ y\Gamma & \xrightarrow{A} & Ty. } $$
=--

+--{: .un_defn}
###### Definition
Let $C$ and $D$ be CwFs.  A **CwF morphism** is a functor $F:C\to D$ together with a commutative square in $[C^{op},Set]$:
$$\array{ Tm_C & \to & F^*(Tm_D) \\ \downarrow & & \downarrow \\ Ty_C & \to & F^*(Ty_D) }$$
such that (TODO)
=--

This defines a category $\mathbf{CwF}$ of categories with families and their morphisms, in which we aim to construct an initial object.

## Type structure

Each type forming operation corresponds to structure on a CwF that can be expressed naturally in terms of categorical operations in the presheaf category $[C^{op},Set]$.

### $\Pi$-types

include [[Initiality Project - Semantics - Pi-types]]
