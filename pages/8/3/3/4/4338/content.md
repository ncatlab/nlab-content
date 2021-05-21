+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Monoid theory
+-- {: .hide}
[[!include monoid theory - contents]]
=--
=--
=--

# Zero-divisors
* table of contents
{: toc}

## Idea

A zero-divisor is something that, like zero itself, can be multiplied by something nonzero to produce zero as a product.


## Definitions

Let $M$ be a [[absorption monoid]] (such as a [[commutative ring]] or any [[ring]]).

An element $x$ of $M$ is a __non-zero-divisor__ if, whenever $x \cdot y = 0$ or $y \cdot x = 0$, then $y = 0$.  An element $x$ is a __zero-divisor__ if there exists $y \ne 0$ such that $x \cdot y = 0$ or $y x = 0$.

In [[constructive mathematics]], we want $\ne$ to be a [[tight apartness relation]] on $M$ in the definition of zero-divisor.  We also say that $x$ is a __strong non-zero-divisor__ if, whenever $y \ne 0$, then $x y \ne 0$ and $y x \ne 0$.  (The notion of (weak) non-zero-divisor makes sense even without any apartness relation.)

If $M$ is (or may be) non-commutative, then we may distinguish __left__ and __right__ (non)-zero-divisors in the usual way.

## Properties

By this definition, [[zero]] itself is a zero-divisor if and only if $M$ is non-trivial.  (Some authorities will differ on this point, but if you think about it, this is clearly the correct definition, by the same principle that the trivial ring is not a field, $1$ is not a prime number, etc.  See [[too simple to be simple]].)

An [[integral domain]] is precisely a commutative ring (whose multiplicative monoid is an absorption monoid by definition) in which [[zero]] is the unique zero-divisor of the multiplicative monoid of the commutative ring (or constructively, in which the strong non-zero-divisors are precisely the strong non-zero elements in the multiplicative monoid, that is those elements $x$ such that $x \ne 0$).

The non-zero-divisors of any absorption monoid $M$ form a [[monoid]] under multiplication, which may be denoted $M^{\times}$.  Note that if $M$ happens to be a [[field]], then this $M^{\times}$ agrees with the usual notation $M^{\times}$ for the [[group]] of invertible elements of the multiplicative monoid $M$, but $M^{\times}$ is not a group in general.  (We may use $M^{\div}$ or $M^*$ for the group of invertible elements.)

## Generalisations

If $I$ is any [[ideal of a monoid|ideal]] of $M$, then we can generalise from a zero-divisor to an $I$-[[divisor]].  In a way, this is nothing new; $x$ is an $I$-divisor in $M$ if and only if $[x]$ is a zero-divisor in $M/I$.  Ultimately, this is related to the notion of [[divisor]] in [[algebraic geometry]].

## Related concepts

* [[absorption monoid]]

* [[integral domain]]

[[!redirects zero-divisor]]
[[!redirects zero-divisors]]
[[!redirects zero divisor]]
[[!redirects zero divisors]]
