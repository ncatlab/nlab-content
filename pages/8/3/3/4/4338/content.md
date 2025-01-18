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

A zero-divisor is something that, like [[zero]] itself, when [[multiplication|multiplied]] by something possibly nonzero still produces zero as a product.

## Definitions

Let $M$ be a [[absorption monoid]] (such as a [[commutative ring]] or any [[ring]]).

An element $x$ of $M$ is a __non-zero-divisor__ if, whenever $x \cdot y = 0$ or $y \cdot x = 0$, then $y = 0$.  

\begin{definition}
An element $x$ is a __zero-divisor__ if there exists $y \ne 0$ such that $x \cdot y = 0$ or $y \cdot x = 0$.

$$\mathrm{isZeroDivisor}(x) \coloneqq \exists y \in M.\neg(y = 0) \Rightarrow ((x \cdot y = 0) \vee (y \cdot x = 0))$$
\end{definition}

By this definition, [[zero]] itself is a zero-divisor if and only if $M$ is non-trivial (see [[too simple to be simple]])

Alternatively, one can define a zero-divisor using a weakened version of [[negation]] from [Lombardi & Quitté 2010](#LombardiQuitté2010) in the definition of zero divisor: 

\begin{definition}
An element $x$ is a **zero-divisor** if there exists an element $y$ such that if $y = 0$ then $1 = 0$, and $x \cdot y = 0$ or $y \cdot x = 0$.

$$\mathrm{isZeroDivisor}\prime(x) \coloneqq \exists y \in M.((y = 0) \Rightarrow (1 = 0)) \wedge ((x \cdot y = 0) \vee (y \cdot x = 0))$$
\end{definition}

By this definition, [[zero]] itself is also a zero divisor in the [[trivial monoid]]. 

### In constructive mathematics

By the [[antithesis interpretation]] of [[constructive mathematics]] we want $\ne$ to be an arbitrary [[irreflexive symmetric relation]] and we want the monoid operation to be strongly extensional with respect to $\ne$ as well. We also say that $x$ is a __strong non-zero-divisor__ if, whenever $y \ne 0$, then $x \cdot y \ne 0$ and $y \cdot x \ne 0$. 

If $M$ is (or may be) non-commutative, then we may distinguish __left__ and __right__ (non)-zero-divisors in the usual way.

## Properties

An [[integral domain]] is precisely a commutative ring (whose multiplicative monoid is an absorption monoid by definition) in which [[zero]] is the unique zero-divisor of the multiplicative monoid of the commutative ring (or constructively, in which the strong non-zero-divisors are precisely the strong non-zero elements in the multiplicative monoid, that is those elements $x$ such that $x \ne 0$).

The non-zero-divisors of any absorption monoid $M$ form a [[monoid]] under multiplication, which may be denoted $M^{\times}$.  Note that if $M$ happens to be a [[field]], then this $M^{\times}$ agrees with the usual notation $M^{\times}$ for the [[group]] of invertible elements of the multiplicative monoid $M$, but $M^{\times}$ is not a group in general.  (We may use $M^{\div}$ or $M^*$ for the group of invertible elements.)

## Generalisations

If $I$ is any [[ideal of a monoid|ideal]] of $M$, then we can generalise from a zero-divisor to an $I$-[[divisor]].  In a way, this is nothing new; $x$ is an $I$-divisor in $M$ if and only if $[x]$ is a zero-divisor in $M/I$.  Ultimately, this is related to the notion of [[divisor]] in [[algebraic geometry]].

## Related concepts

* [[absorption monoid]]

* [[integral domain]]

* [[cancellative element]]

## References

* {#LombardiQuitté2010} [[Henri Lombardi]], [[Claude Quitté]] (2010): *Commutative algebra: Constructive methods (Finite projective modules)* Translated by Tania K. Roblo, Springer (2015) ([doi:10.1007/978-94-017-9944-7](https://link.springer.com/book/10.1007/978-94-017-9944-7), [pdf](http://hlombardi.free.fr/CACM.pdf))

[[!redirects zero-divisor]]
[[!redirects zero-divisors]]
[[!redirects zero divisor]]
[[!redirects zero divisors]]
