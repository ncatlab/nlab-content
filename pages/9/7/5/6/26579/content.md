
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The [[category]] whose [[objects]] are [[finite sets]] and whose [[morphisms]] are [[stochastic maps]] (or [[stochastic matrices]]) is often denotes _FinStoch_, or similar; a [[full subcategory]] of [[Stoch]].

This is an elementary but nontrivial example of a [[Markov category]], and together with its subcategory [[Stoch#borelstoch|BorelStoch]], one of the most important categories of [[category-theoretic probability]].

## Definition

_FinStoch_ is the category whose 

* [[Objects]] are [[finite sets]];
* [[Morphisms]] are [[stochastic matrices]].

See at [[stochastic matrix]] for more details.

## Properties

* _FinStoch_ is closely related to the Kleisli category of the [[distribution monad]]: it is its [[full subcategory]] whose objects are finite sets.

* _FinStoch_ is a [[Cauchy-complete category]].

* As a [[Markov category]], it has [[Markov category#conditionals|conditionals]], and is hence [[Markov category#positivity_and_causality|positive and causal]].

## Characterizations

* _FinStoch_ is the [[opposite category]] of the [[Lawvere theory]] for [[convex spaces]]. One can then dualize the presentation of convex spaces to obtain a characterization of _FinStoch_ as a category with coproducts. It being [[symmetric monoidal]] corresponds to the fact that the algebraic theory is [[commutative algebraic theory|commutative]]. A presentation would have generators $c_p:1\to 1+1$ (corresponding to the binary operations $c_p$) together with equations amounting to the equations presenting convex spaces. 

* For a simple specific case, let _DyFinStoch_ be the [[wide subcategory]] of _FinStoch_ where the probabilities are [[dyadic rational numbers]]. This is the [[opposite category]] of the [[Lawvere theory]] for [[midpoint algebra]]s. It is also therefore the free [[distributive monoidal category]] that is [[semicartesian monoidal category|semicartesian]] and with a map $c:1\to 1+1$ such that $s\circ c=c$ where $s:1+1\to 1+1$ is the symmetry of the coproduct. For the third axiom at [[midpoint algebra]]s says that the theory is [[commutative algebraic theory|commutative]], the first says that it is [[semicartesian monoidal category|semicartesian]], and the law  $s\circ c=c$ is the second axiom. 

* Let _BinStoch_ be the full subcategory of _FinStoch_ where the objects are powers of two. Then this category as a [[symmetric monoidal category]] is characterized in [Piedeleu et al](#binstochA).

## Related concepts

* [[Markov category]]
* [[Markov kernel]]
* [[category of couplings]]
* [[probability monad]]
* [[Giry monad]]
* [[Kleisli category]]
* [[categorical probability]]


## References:

* [[Marshall Stone|Marshall H Stone]], _Postulates for the barycentric calculus_, Ann. Mat. Pura. Appl. (4), 29:25&#8211;30, 1949.

* {#markov_support} [[Tobias Fritz]], Tomáš Gonda, Antonio Lorenzin, [[Paolo Perrone]], Dario Stein, _Absolute continuity, supports and idempotent splitting in categorical probability_ &lbrack;[arXiv:2308.00651](https://arxiv.org/abs/2308.00651)&rbrack;

* {#binstochA} [[Robin Piedeleu]], Mateo Torres-Ruiz, Alexandra Silva, [[Fabio Zanasi]], ''A Complete Axiomatisation of Equivalence for Discrete Probabilistic Programming'', [arXiv:2408.14701](https://arxiv.org/abs/arXiv:2408.14701), 2024.

category: category, probability

[[!redirects Finstoch]]