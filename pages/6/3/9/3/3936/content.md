
This page is about the notion of _model_ in [[logic]]. For the notion in [[physics]] see _[[model (in theoretical physics)]]_.

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Model theory
+-- {: .hide}
[[!include model theory - contents]]
=--
=--
=--

#Model#
* table of contents
{:toc}


## Idea

In [[model theory]], a __model__ of a [[theory]] is a realization of the [[types]], operations, [[relations]], and [[axioms]] of that theory.  In ordinary model theory one usually studies mainly models in [[sets]], but in [[categorical logic]] we study models in other [[categories]], especially in [[topoi]].

The term _[[structure in model theory|structure]]_ is often used to mean a realization of types, operations, and relations in some [[signature (in logic)|signature]], but not satisfying any particular axioms.  This is of course the same as a model for the "empty theory" in that signature, which has the same types, operations, and relations, but no axioms at all.  One then talks about whether a given structure is, or is not, a *model* of a given theory in a given signature.


## Definition

### In first-order theories

The basic concept is of a _[[structure in model theory|structure]]_ for a [[first-order language]] $L$: a set $M$ together with an interpretation of $L$ in $M$. A theory $T$ is specified by a language and a set of sentences in $L$. 

An $L$-structure $M$ is a __model__ of $T$ if for every sentence $\phi$ in $T$, its interpretation in $M$, $\phi^M$ is true ("$\phi$ holds in $M$"). 

We say that $T$ is __consistent__ or satisfiable (relative to the universe in which we do model theory) if there exist at least one model for $T$ (in our universe). Two theories, $T_1$, $T_2$ are said to be __equivalent__ if they have the same models. 

Given a class $K$ of structures for $L$, there is a theory $Th(K)$ consisting of all sentences in $L$ which hold in every structure from $K$. Two structures $M$ and $N$ are __elementary equivalent__ (sometimes written by equality $M=N$, sometimes said "elementarily equivalent") if $Th(M)=Th(N)$, i.e. if they satisfy the same sentences in $L$. Any set of sentences which is equivalent to $Th(K)$ is called a __set of axioms__ of $K$. A theory is said to be __finitely axiomatizable__ if there exist a finite set of axioms for $K$. 

A theory is said to be __complete__ if it is equivalent to $Th(M)$ for some structure $M$. 

### For Lawvere theories

For $Syn(T)$ the [[syntactic category]] of an [[algebraic theory]] (where $Syn(T)$ is perhaps better known as a [[Lawvere theory]]), and for $C$ any category with finite [[limit]]s, a _model_ for $T$ in $C$ is a product-preserving functor

$$
  N : Syn(T) \to C
  \,.
$$

The **category of models** in this case is hence the [[full subcategory]] of the [[functor category]] $[Syn(T),C]$ on product-preserving functors.

## Examples

* [[models in presheaf toposes]]

## Related entries


* [[structure in model theory]]

[[!redirects models]]
[[!redirects category of models]]
[[!redirects categories of models]]

[[!redirects model (logic)]]
