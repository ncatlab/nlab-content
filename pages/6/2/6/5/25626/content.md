
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

A __tensorial costrength__ (or simply __costrength__) for a [[functor]] $F \colon V \to V$ on a [[monoidal category]] $V$ is, in essence, the [[opposite category|dual]] of a [[tensorial strength]]. Whereas a strength provides a coherent [[natural transformation]] of the form:
$$X \otimes F(Y) \to F(X \otimes Y)$$
or
$$F(X) \otimes Y \to F(X \otimes Y)$$
(a __left-strength__ or __right-strength__ respectively),
a costrength provides a coherent [[natural transformation]] of the form:
$$F(X \otimes Y) \to X \otimes F(Y)$$
or
$$F(X \otimes Y) \to F(X) \otimes Y$$
(a __left-costrength__ or __right-costrength__ respectively).

When $V$ is [[symmetric monoidal category|symmetric]], the [[braiding]] $b$ allows to obtain a left-costrength from a right-costrength, and in this setting, one usually drops “left-” or “right-” and simply talks about __tensorial costrengths__.

More generally, a __costrength__ (on a monoidal category which is not necessarily symmetric) is a left-costrength and a right-costrength such that the two induced maps $T(X\otimes (Y\otimes Z)) \to (X \otimes T Y) \otimes Z$ agree.

## Definition 

For now, see *[[tensorial strength]]*, whose definition may be appropriately dualised.

## Terminology

The terminology "costrength" was introduced by [Blute, Cockett & Seely (1997)](#BCS97) for the concept described here. This terminology is consistent with the usual convention in category theory of prefixing a term by "co-" when it is the same concept in the [[opposite category]] $V^{op}$.

Unfortunately, in the same year, [Power & Robinson](#PR97) also used the terminology "costrength" to describe a [[tensorial strength|right-strength]]. A right-strength is a left-strength with respect to the reversal of the tensor product, i.e. a left-strength in the [[reverse monoidal category]] $V^{rev}$. While both usages can be found in recent literature, we prefer the terminology that is consistent with prior categorical terminology.

(Note that the notion of "cotensorial strength" from [Kock (1972)](#kock72) is different from both concepts, and involves a costrength-like transformation involving the [[internal hom]] of a monoidal category, rather than the tensor.)

## Related concepts

* [[tensorial strength]]
* [[strong monad]]
* [[commutative monad]]

## References

* {#BCS97} [[R. F. Blute]], [[J. R. B. Cockett]], and [[R. A. G. Seely]]. _Categories for computation in context and unified logic._ Journal of Pure and Applied Algebra 116.1-3 (1997): 49-98.

The following paper introduces a conflicting definition of "costrength", which we call a [[tensorial strength|right-strength]]:

* {#PR97} [[John Power]], and [[Edmund Robinson]]. _Premonoidal categories and notions of computation_. Mathematical structures in computer science 7.5 (1997): 453-468.

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
