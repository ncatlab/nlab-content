
# Formally real rings
* table of contents
{: toc}

## Idea

When working with algebras (possibly [[associative algebra|associative]], possibly [[nonassociative algebra|nonassociative]]) over the [[real numbers]], we often want to express the fact that $-1$ has no [[square root]] in the algebra.  However, this by itself is not enough, since the algebra may lack square roots for other reasons, so we say that $-1$ is not a _sum_ of squares.  Even this may be too weak if the algebra has too little division, because we also want to ensure that other negative squares are not sums of squares.  So the really general statement is that $0$ is not a sum of squares, except as a sum of squares of $0$ itself.

At this point, we notice that the $\mathbb{R}$-linear structure is irrelevant, and the concept applies to more general [[rings]] (possibly [[nonassociative rings|nonassociative]]).  Even the existence of opposites is not needed, and the concept applies to (possibly nonassociative) [[rigs]].  Really, we just need multiplication, addition, and zero.


## Definitions

Let $A$ be [[ring]], or more generally a [[magma]] in the category of [[abelian monoids]].  Then $A$ is __formally real__ if, whenever
$$ \sum_i x_i^2 = 0 $$
(for a finite sum), each $x_i = 0$.

Given an [[involution]], we have a generalization: a $*$-[[star-ring|ring]] is __formally complex__ if, whenever
$$ \sum_i x_i^* x_i = 0 $$
(for a finite sum), each $x_i = 0$.  (Then a ring is formally real iff it is formally complex when equipped with the trivial involution.)


## Examples

Of course, the [[real numbers]] themselves form a formally real ring; the [[complex numbers]] do not, since
$$ \mathrm{i}^2 + 1^2 = 0 .$$
However, the complex numbers are formally complex.  (These examples are the source of the names.)

Actually, all of the [[Cayley–Dickson algebra]]s are formally complex.  (This is because $x^* x$ is always a real number and is $0$ only when $x$ is.)

The [[trivial ring]] is formally real.  Every other formally real (or formally complex) ring is [[infinite set|infinite]] (because $1 = 1^2$, $2 = 1^2 + 1^2$, $3 = 1^2 + 1^2 + 1^2$, etc are all distinct).  Even without an identity (and even in the nonassociative case), if the ring is formally real and nontrivial, then it is infinite.  (If $x \ne 0$, consider $x^2$, $x^2 + x^2$, $x^2 + x^2 + x^2$, etc.)

There are finite formally real *rigs*, however, such as the [[multiplicatively idempotent rig]] $\{0, 1\}$.  Indeed, any [[distributive lattice]] (with a [[bottom element]]), viewed as a rig, is formally real.

Among [[Jordan algebras]], the formally real ones are especially important; it is these that (over the real numbers, in finite dimensions) have a nice [[classification theorem]].


## Properties

The [[trivial algebra]] is the only formally real algebra over any ring that is *not* formally real; more generally, if $A \to B$ is a [[monomorphism]] of rings (or of rigs, etc), then $A$ must be formally real if $B$ is.  Similarly, if $A \to B$ is a monomorphism of $*$-rings, then $A$ must be formally complex if $B$ is.

Formally real [[fields]] (like that of the real numbers) are particularly interesting; see [[formally real field]].

Every formally real (or formally complex) ring has a natural [[partial ordering]]: $a \leq b$ iff $b - a$ can be written as a sum of squares (or a sum of terms of the form $x^* x$).


[[!redirects formally real]]

[[!redirects formally real ring]]
[[!redirects formally real rings]]

[[!redirects formally real rig]]
[[!redirects formally real rig]]
[[!redirects formally real semiring]]
[[!redirects formally real semirings]]

[[!redirects formally real algebra]]
[[!redirects formally real algebras]]

[[!redirects formally complex]]
[[!redirects formally complex ring]]
[[!redirects formally complex rings]]
[[!redirects formally complex rig]]
[[!redirects formally complex rig]]
[[!redirects formally complex semiring]]
[[!redirects formally complex semirings]]
[[!redirects formally complex algebra]]
[[!redirects formally complex algebras]]
