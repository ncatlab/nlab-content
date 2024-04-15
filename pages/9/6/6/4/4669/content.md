
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition


A [[Lie algebra]] $\mathfrak{g}$ is __abelian__ if its bracket is identically 0, in that for all $x,y \in \mathfrak{g}$ we have 

$$ 
  [x,y] = 0
  \,.
$$

## Examples

Every [[vector space]] has a (necessarily unique) abelian Lie algebra structure.  As such, we may identify an abelian Lie algebra with its underlying vector space.


Abelian Lie algebras play an important role in the theory of compact Lie groups.
This stems from the existence of [[maximal torus|maximal tori]] for those groups, whose Lie algebras are abelian.
Over an algebraically closed field of characteristic zero, these maximal tori present the [[Cartan subalgebra]] of $\mathfrak{g}$.

Over $\mathbb{R}$, the unique $n$-dimensional abelian Lie algebra $\mathbb{R}^n$ comes from the Lie group $U(1)^{\times n}$.


A $0$-dimensional or $1$-dimensional Lie algebra must be abelian.  The $0$-dimensional Lie algebra is the [[trivial Lie algebra]].  The $1$-dimensional Lie algebra is a [[simple object]] in [[LieAlg]], but it is traditionally *not* considered a [[simple Lie algebra]].

## Lie integration

Under [[Lie integration]] abelian Lie algebras integrate to [[abelian Lie group]]s.

In other words, if $G$ is a connected abelian Lie group then $\mathfrak{g}$ generates the whole group under exponentiation.
This can be deduced from the equation

$$
\exp(X)\exp(Y) = exp(X+Y),
$$

which follows for instance from the [[Baker-Campbell-Hausdorff formula]].
Hence the image of the exponential is a subgroup near the identity, which generates the whole group under group multiplication (e.g. see [here](https://math.stackexchange.com/questions/282442/a-neighbourhood-of-identity-u-generates-g-where-g-is-a-connected-lie-group)).

[[!redirects abelian Lie algebra]]
[[!redirects abelian Lie algebras]]
[[!redirects Abelian Lie algebra]]
[[!redirects Abelian Lie algebras]]
