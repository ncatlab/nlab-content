+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Model theory
+-- {: .hide}
[[!include model theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea
Given a collection of finite(ly-generated) [[structure|first-order structures]] which formally resemble collections of finite(ly-generated) substructures found inside an infinite structure, there are additional assumptions on such collections we can make which ensure that they can be amalgamated into an infinite structure which somehow captures the "generic theory" of the collection we started with.

## Definition
A class of finitely-generated structures closed under substructures and isomorphisms such that:

1. (Amalgamation) every [[span]] of embeddings (not necessarily elementary) admits a [[cocone]], and

2. (Joint embedding) Every pair of structures admits a [[cocone]]

is called a _Fra&#239;ss&#233; class_.

A _Fra&#239;ss&#233; limit_ $\underset{\rightarrow}{\operatorname{Flim}}(\mathcal{C})$ of a Fra&#239;ss&#233; class $\mathcal{C}$ is the unique (existence and uniqueness was Fra&#239;ss&#233;'s theorem) countable _ultrahomogeneous_ (every isomorphism of finitely-generated substructures extends to an automorphism of $M$) structure into which every member of $\mathcal{C}$ embeds.

## Constructing Fra&#239;ss&#233; limits

[Will fill this in after I learn how to typeset diagrams]

## Examples
- The [[DLO|countable dense linear order]] is the Fraisse limit of the class of finite linear orders.

- The [[countable random graph]] is the Fraisse limit of the class of finite graphs.

- The [[Henson graph]] (the generic triangle-free graph) is the Fraisse limit of the class of finite triangle-free graphs.

- A modification ([[Hrushovski construction|Hrushovski constructions]]) to the Fra&#239;ss&#233; construction was used by [[Ehud Hrushovski]] to produce a counterexample to [[Zilber's trichotomy conjecture]] classifying the possible [[matroid|combinatorial geometry]] on a [[strongly minimal]] set.

## Remarks
- Olivia Caramello remarks in her topos-theoretic Fra&#239;ss&#233; paper (linked below) that the [[classifying topos]] of an [[omega-categorical]] structure $A$ presentable as a Fra&#239;ss&#233; limit is precisely the [[category of G-sets|category of continuous Aut(A)]]-sets, where the automorphism group of $A$ is equipped with the topology of pointwise convergence.

- It is interesting when a structure is presentable as both a Fra&#239;ss&#233; limit and ultraproduct of finite structures. In more suggestive terminology, this means that the _generic_ and the _almost-sure_ (one way of obtaining the almost-sure theory of a collection of finite structures is to take the theory of their ultraproduct) theories of the underlying collection of finite structures coincide. For example, the countable random graph above satisfies a zero-one law.

- Recently, Zilber has been trying to study [[field with one element|F_1-geometry]] by 'fusing' the algebraic closures of finite fields together with a Hrushovski construction and studying a nonstandard extension ([[ultrapower]]) of the result.


## Related concepts
[[omega-categorical structure]]

[[homogeneous structure]]

## References
- David Corfield, [Fra&#239;ss&#233; limits](https://golem.ph.utexas.edu/category/2009/11/fraisse_limits.html) 

- Hodges, [A shorter model theory](http://www.cambridge.org/catalogue/catalogue.asp?isbn=9780521587136)

- Olivia Caramello, [Fra&#239;ss&#233;'s construction from a topos-theoretic perspective](https://arxiv.org/abs/0805.2778)

[[!redirects Fraisse limit]]
