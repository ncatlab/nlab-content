# Totally convex spaces
* table of contents
{: toc}


## Idea

Essentially, the totally convex spaces are what you get if you try to build an [[algebraic theory]] out of [[Banach spaces]].


## Definition

+-- {: .num_defn #tcs}
###### Definition
A __totally convex space__ is a [[module for a monad|module]] for the [[monad]] on [[Set]] which sends a set $X$ to the closed unit ball of the Banach space $\ell^1(X)$.
=--

This is an example of an [[algebraic theory]] (in the strong sense that it is [[monadic category|bounded monadic]]) but not finitary, hence not a [[Lawvere theory]].  The [[free object|free]] totally convex space on $X$ is the unit ball of the Banach space $\ell^1(X)$, and thus an operation in this theory is a formal sum $\sum_{x \in X} a_x$ with $a_x \in \mathbb{R}$ with the property that $\sum_{x \in X} |a_x| \le 1$.  The finiteness of this sum forces it to have only countably many non-zero terms, and thus it factors through an operation on $\mathbb{N}$.  Hence there is a presentation of this theory with operations in $\ell^1(\mathbb{N})$.  The corresponding identities are simply the substitution rules -- namely that substituting a sum into another works as expected -- and the reordering rules.


## Properties

1. A totally convex space is a [[pointed object|pointed]] [[convex space]].  The operations of a convex space are encoded in the operations $(r, 1 - r, 0,0,0, \dots)$ and the "point" comes from the operation $(0,0,\dots)$.  This functor preserves underlying sets and so has a [[left adjoint]]; thus any convex space can be "completed" to a totally convex space.

1. The operations for this theory are [[commutative algebraic theory|commutative]], hence the [[category]] of totally convex spaces is a [[closed symmetric monoidal category]].


## Examples

1. Clearly, the closed unit ball $B X$ of any Banach space $X$ is a totally convex space.

1. Bizarrely, the **open** unit ball of a Banach space is a totally convex space.  This is because if a sum, $\sum_{x \in B X} a_x x$ for $\sum_x |a_x| \leq 1$, lies on the boundary of $B X$ then every $x$ for which $a_x \ne 0$ must have norm $1$.  Thus if the series only contains terms from the interior of $B X$, the sum remains in the interior.  Hence the open unit ball is a [[subalgebra]] of the closed unit ball.

1. Continuing, the quotient of the closed unit ball by the open unit ball is a totally convex space.

1. In particular, the three-point space $\{-1,0,1\}$ is a totally convex space.  The operations on this space are as follows:

   $$
   \sum a_j \epsilon_j = \begin{cases}
   1 & \epsilon_j = \operatorname{sign}(a_j), \sum |a_j| = 1 \\
   -1 & \epsilon_j = -\operatorname{sign}(a_j), \sum |a_j| = 1 \\
   0 & \;\text{otherwise}
   \end{cases}
   $$

1. Going back one step, $(-1,1)$ is a totally convex space.   It is illuminating to describe this as a [[coequaliser]] of free totally convex spaces.  Consider a functional $f \colon \ell^1(\mathbb{N}) \to \mathbb{R}$ which is bounded of norm $1$ but does not achieve its norm.  For example, let $f$ be represented by the sequence $(\frac12,\frac23,\frac34,\dots)$.  Then for any $x \in B\ell^1(\mathbb{N})$, $f(x) \in (-1,1)$.  Thus $(-1,1)$ is the coequaliser of the inclusion $\ker f \to \ell^1(\mathbb{N})$ and the [[zero map]] $\ker f \to \ell^1(\mathbb{N})$.


[[!redirects totally convex spaces]]