
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

A [[functor]] $U:D\to C$ is _monadic_ iff it has a left adjoint $F:C\to D$ and the adjunction $F\dashv U$ 'comes from' the induced [[monad]] on $C$ -- that is, $U$ _monadic_ iff $F\dashv U$ is a [[monadic adjunction]].

In this situation $U$ in some sense 'looks like' the forgetful functor from the [[Eilenberg-Moore category]] of the monad $(U\circ F,\eta,U\epsilon_F)$ on $C$, and has 'nice properties' similar to these forgetful functors.

The [[monadicity theorem]] characterizes monadic functors and makes these 'nice properties' precise.

## Definition

Given a pair of [[adjoint functors]] $F: C \to D :U$, $F \dashv U$, with [[unit of an adjunction|unit]] $\eta: Id_C \to U \circ F$ and counit $\epsilon: F \circ U \to Id_D$, one constructs a [[monad]] $\mathbf{T}=(T,\mu,\eta)$ setting $T = U \circ F: C \to C$, $\mu = U \epsilon F: T T = U F U F \to U F = T$. 

Consider the [[Eilenberg-Moore category]] $C^{\mathbf{T}}$ of $T$-algebras ($T$-modules) in $C$. Clearly $U (\epsilon_M): T U M = U F U M \to U M$ is a $T$-action. In fact there is a canonical __comparison functor__ $K^{\mathbf{T}}: D \to C^{\mathbf{T}}$ given on objects by $K(M)=(U M, U (\epsilon_M))$.  We then say that we have a (resp. strictly) [[monadic adjunction]] iff $K$ is an equivalence (resp. isomorphism) of categories.

A [[functor]] $U: D \to C$ is **monadic** (resp. **strictly monadic**) if it has a [[left adjoint]] $F: C\to D$ and the comparison functor $K^{\mathbf{T}}: D \to C^{\mathbf{T}}$ is an [[equivalence of categories]] (resp. an isomorphism of categories).  In other words, up to equivalence, monadic functors are precisely the [[forgetful functor]]s defined on Eilenberg--Moore categories for monads, and strictly monadic functors are the same as these forgetful functors up to isomorphism. A __category__ $D$ is __monadic__ over a category $C$ if there is a functor $U: D \to C$ which is monadic.

Monadic functors are sometimes called **functors of effective descent type**. See the page on [[monadic descent]] for more details.

## Properties

Various versions of Beck's [[monadicity theorem]] (old-fashioned name of some schools: tripleability theorem) give sufficient, and sometimes necessary, conditions for a given functor to be monadic. There are also dual, [[comonadic functor|comonadic versions]].

A monadic functor is strictly monadic if and only if it is also an [[amnestic functor|amnestic]] [[isofibration]]: clearly, a strictly monadic functor is an amnestic isofibration; and if a monadic functor $U$ is amnestic, then the comparison functor $K$ is also amnestic, and if $U$ is a monadic isofibration, so is $K$; therefore in this case $K$ must be an isomorphism of categories. 

Beware that monadic functors are not closed under composition. For a specific example: the category of [[reflexive graph|reflexive quivers]] is monadic over $Set$ via the functor $RefGph \to Set$ sending a graph to its set of edges, and the category of categories is monadic over reflexive graphs via the forgetful functor $Cat \to RefGph$, but $Cat$ is not monadic over $Set$ (via any functor whatsoever, since such categories are [[regular categories]] but $Cat$ is not).

This is an instance of a general phenomenon: Let $\mathcal{C}$ be a reflective subcategory of a presheaf category $\widehat{A}$ (e.g. every [[locally presentable category]] is of this form). Then the adjunction between $\mathcal{C}$ and $\widehat{A}$ is monadic, and the adjunction between $\widehat{A}$ and $\mathrm{Set}^{\mathrm{Ob} A}$ is also monadic. But the composite adjunction between $\mathcal{C}$ and $\mathrm{Set}^{\mathrm{Ob} A}$ is often not monadic. For instance, if it is monadic, then $\mathcal{C}$ must be a [[Barr-exact category]].


## Related concepts

* [[monadic adjunction]], [[structure-semantics adjunction]]

* [[comonadic functor]], [[monadicity theorem]]

* If the comparison functor is only [[fully faithful]], a functor is sometimes called [[premonadic]] or said to be of [[descent type]].

* [[monadic decomposition]]

[[!redirects monadic]]
[[!redirects monadic category]]
[[!redirects monadic functors]]

[[!redirects comonadic]]
[[!redirects co-monadic]]

[[!redirects comonadic functor]]
[[!redirects co-monadic functor]]
[[!redirects comonadic functors]]
[[!redirects co-monadic functors]]

[[!redirects effective descent type]]
[[!redirects functor of effective descent type]]
[[!redirects functors of effective descent type]]

