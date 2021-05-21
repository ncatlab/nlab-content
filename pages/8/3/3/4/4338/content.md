# Zero-divisors
* table of contents
{: toc}

## Idea

A zero-divisor is something that, like zero itself, can be multiplied by something nonzero to produce zero as a product.


## Definitions

Let $R$ be a [[commutative ring]] (or any [[ring]]).

An element $x$ of $R$ is a __non-zero-divisor__ if, whenever $x y = 0$ or $y x = 0$, then $y = 0$.  An element $x$ is a __zero-divisor__ if there exists $y \ne 0$ such that $x y = 0$ or $y x = 0$.

In [[constructive mathematics]], we want $\ne$ to be a [[tight apartness relation]] on $R$ in the definition of zero-divisor.  We also say that $x$ is a __strong non-zero-divisor__ if, whenever $y \ne 0$, then $x y \ne 0$ and $y x \ne 0$.  (The notion of (weak) non-zero-divisor makes sense even without any apartness relation.)

If $R$ is (or may be) non-commutative, then we may distinguish __left__ and __right__ (non)-zero-divisors in the usual way.

Note that, in a ring, an element is a non-zero-divisor if and only if the operation of multiplication by that element is [[injection|injective]].  This is probably the right definition of zero-divisor to use in a [[rig]], even though then it no longer literally has anything to do with being a divisor of [[zero]].


## Properties

By this definition, [[zero]] itself is a zero-divisor if and only if $R$ is non-trivial.  (Some authorities will differ on this point, but if you think about it, this is clearly the correct definition, by the same principle that the trivial ring is not a field, $1$ is not a prime number, etc.  See [[too simple to be simple]].)

An [[integral domain]] is precisely a [[commutative ring]] in which [[zero]] is the unique zero-divisor (or constructively, in which the strong non-zero-divisors are precisely the strong non-zero elements, that is those elements $x$ such that $x \ne 0$).

The non-zero-divisors of any rig $R$ form a [[monoid]] under multiplication, which may be denoted $R^{\times}$.  Note that if $R$ happens to be a [[field]], then this $R^{\times}$ agrees with the usual notation $R^{\times}$ for the [[group]] of invertible elements of $R$, but $R^{\times}$ is not a group in general.  (We may use $R^{\div}$ or $R^*$ for the group of invertible elements.)


## Generalisations

If $I$ is any [[ideal]] of $R$, then we can generalise from a zero-divisor to an $I$-[[divisor (ring theory)|divisor]].  In a way, this is nothing new; $x$ is an $I$-divisor in $R$ if and only if $[x]$ is a zero-divisor in $R/I$.  Ultimately, this is related to the notion of [[divisor]] in [[algebraic geometry]].

## Related concepts

* [[absorption magma]]

[[!redirects zero-divisor]]
[[!redirects zero-divisors]]
[[!redirects zero divisor]]
[[!redirects zero divisors]]
