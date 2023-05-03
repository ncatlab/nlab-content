
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea 

A _tensorial costrength_ (or simply _costrength_) for a [[functor]] $F \colon V \to V$ on a [[monoidal category]] $V$ is, in essence, the [[opposite category|dual]] of a [[tensorial strength]]. Whereas a strength provides [[morphisms]] of the form:
$$X \otimes F(Y) \to F(X \otimes Y)$$
or
$$F(X) \otimes Y \to F(X \otimes Y)$$
(a _left-strength_ or _right-strength_ respectively),
a costrength provides morphisms of the form:
$$F(X \otimes Y) \to X \otimes F(Y)$$
or
$$F(X \otimes Y) \to F(X) \otimes Y$$
(a _left-costrength_ or _right-costrength_ respectively).

When $V$ is [[symmetric monoidal category|symmetric]], tensorial left-costrengths are equivalently tensorial right-costrengths, and in this setting, one usually drops “left-” or “right-” and simply talks about tensorial costrengths.

## Definition 

For now, see *[[tensorial strength]]*, whose definition may be appropriately dualised.

## Terminology

The terminology "costrength" was introduced by [Blute, Cockett & Seely (1997)](#BCS97) for the concept described here (i.e. a strength in the [[opposite category]] $V^{op}$). Unfortunately, in the same year, [Power & Robinson](#PR97) also used the terminology "costrength" to describe a [[tensorial strength|right-strength]] (i.e. a strength in the [[reverse monoidal category]] $V^{rev}$). Both meanings can be found in recent literature. However, the former is the most consistent with standard categorical terminology (e.g. see the discussion on [[strong monad]]).

(Note that the notion of "cotensial strength" from [Kock (1972)](#kock72) is different from both concepts, and involves a costrength-like transformation involving the [[internal hom]] of a monoidal category, rather than the tensor.)

## Related concepts

* [[tensorial strength]]
* [[strong monad]]
* [[commutative monad]]

## References

* {#BCS97} [[R. F. Blute]], [[J. R. B. Cockett]], and [[R. A. G. Seely]]. _Categories for computation in context and unified logic._ Journal of Pure and Applied Algebra 116.1-3 (1997): 49-98.

The following paper introduces a conflicting definition of "costrength", which we call a [[tensorial strength|right-strength]]:

{#PR97} * [[John Power]], and [[Edmund Robinson]]. _Premonoidal categories and notions of computation_. Mathematical structures in computer science 7.5 (1997): 453-468.

The notion of cotensorial strength is mentioned briefly in:

* {#kock72} [[Anders Kock]], *Strong functors and monoidal monads*, Arch. Math **23** (1972) 113–120 &lbrack;[doi:10.1007/BF01304852](https://doi.org/10.1007/BF01304852), [pdf](http://home.imf.au.dk/kock/SFMM.pdf)&rbrack;

[[!redirects tensorial costrength]]
[[!redirects tensorial costrengths]]
[[!redirects costrong functor]]
[[!redirects costrong functors]]
[[!redirects costrength]]
[[!redirects costrengths]]

[[!redirects cotensorial strength]]
[[!redirects cotensorial strengths]]
