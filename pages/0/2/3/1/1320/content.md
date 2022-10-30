
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

A [[functor]] is _monadic_ if it is [[natural isomorphism|equivalent]] to the [[forgetful functor]] from a [[category]] of [[algebras over a monad]]. In this case it is part of a _[[monadic adjunction]]_.

The [[monadicity theorem]] characterizes monadic functors.

## Definition


Given a pair of [[adjoint functors]] $F: C \to D :U$, $F \dashv U$, with [[unit of an adjunction|unit]] $\eta: Id_C \to U \circ F$ and counit $\epsilon: F \circ U \to Id_D$, one constructs a [[monad]] $\mathbf{T}=(T,\mu,\eta)$ setting $T = U \circ F: C \to C$, $\mu = U \epsilon F: T T = U F U F \to U F = T$. 

Consider the [[Eilenberg–Moore category]] $C^{\mathbf{T}}$ of $T$-algebras ($T$-modules) in $C$. Clearly $U (\epsilon_M): T U M = U F U M \to U M$ is a $T$-action. In fact there is a canonical __comparison functor__ $K^{\mathbf{T}}: D \to C^{\mathbf{T}}$ given on objects by $K(M)=(U M, U (\epsilon_M))$.  We then say that we have a [[monadic adjunction]].

A [[functor]] $U: D \to C$ is **monadic** (resp. **strictly monadic**) if it has a [[left adjoint]] $F: C\to D$ and the comparison functor $K^{\mathbf{T}}: D \to C^{\mathbf{T}}$ is an [[equivalence of categories]] (resp. an isomorphism of categories).  In other words, up to equivalence, monadic functors are precisely the [[forgetful functor]]s defined on Eilenberg--Moore categories for monads, and strictly monadic functors are the same as these forgetful functors up to isomorphism. A __category__ $D$ is __monadic__ over a category $C$ if there is a functor $U: D \to C$ which is monadic. 

## Properties

Various versions of Beck's [[monadicity theorem]] (old-fashioned name of some schools: tripleability theorem) give sufficient, and sometimes necessary, conditions for a given functor to be monadic. There are also dual, [[comonadic functor|comonadic versions]].

A monadic functor is strictly monadic if and only if it is also an [[amnestic functor|amnestic]] [[isofibration]]: clearly, a strictly monadic functor is an amnestic isofibration; and if a monadic functor $U$ is amnestic, then the comparison functor $K$ is also amnestic, and if $U$ is a monadic isofibration, so is $K$; therefore in this case $K$ must be an isomorphism of categories.


## Related concepts

* [[monadic adjunction]], [[structure-semantics adjunction]]

* [[comonadic functor]], [[monadicity theorem]]



[[!redirects monadic]]
[[!redirects monadic category]]
[[!redirects monadic functors]]