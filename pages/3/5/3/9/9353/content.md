
# Radius of convergence
* table of contents
{: toc}

## Idea

The radius of convergence of a [[power series]] tells how far out the series will [[convergence|converge]].


## Definition

Let $a = (a_0, a_1, \ldots)$ be an [[infinite sequence]] of [[complex numbers]], let $\zeta$ be a particular complex number, and consider the [[power series]]
\[ \sum_n a_n (z - \zeta)^n .\label{series}\]
The __radius of convergence__ is the [[supremum]] of the [[positive numbers]] $\epsilon$ such that (eq:series) converges for ${|z - \zeta|} \lt \epsilon$.  (This supremum is a nonnegative [[lower real]] in $[0,\infty]$.)

The phrasing above is ambiguous.  If $\epsilon$ is less than the radius of convergence, does this mean that (eq:series) converges for *every* $z$ with ${|z - \zeta|} \leq \epsilon$ or for *some* such $z$?  It doesn\'t matter:

+-- {: .num_theorem #radii}
###### Theorem
If (eq:series) converges for some $z$ with ${|z - \zeta|} = \epsilon$, then (eq:series) converges for every $z$ with ${|z - \zeta|} \lt \epsilon$.
=--
(We do *not* say that (eq:series) converges for $z$ with ${|z = \zeta|} = \epsilon$, but this has no effect on the supremum.)


## Properties

The radius of convergence is clearly independent of $\zeta$.  It can be calculated quite easily from the coefficients $a_i$:

+-- {: .num_theorem #Hadamard}
###### Theorem (Cauchy&#8211;Hadamard)
The radius of converge of (eq:series) is
$$ R = \liminf_n {|a_n|}^{-1/n} .$$
=--

For ${|z - \zeta|} \lt R$, (eq:series) is (pretty much by definition) an [[analytic function]] of $z$.  There is a partial converse:

+-- {: .num_theorem #analytic}
###### Theorem
If a function $f$ is analytic at all $z$ with ${|z - \zeta|} \lt R$, then there is a power series (eq:series) that converges to $f(z)$ for all $z$ with ${|z - \zeta|} \lt R$.
=--
(Specifically, $a_n = f^{(n)}(\zeta)/n!$.)


+-- {: .num_remark}
###### Remark

Over the [[real numbers]], Theorem&#160;\ref{analytic} fails.  I\'m sure (says one of this pages authors) that there are interesting things to say about series in [[adic numbers]], [[matrices]], and things like that, but I don\'t know them.

=--

## Related concepts

* [[asymptotic series]]

[[!redirects convergence radius]]
[[!redirects convergence radii]]
[[!redirects convergence radiuses]]
[[!redirects radius of convergence]]
[[!redirects radii of convergence]]
[[!redirects radiuses of convergence]]
