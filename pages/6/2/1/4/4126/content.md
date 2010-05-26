category: physics

****
_This is a stub._

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

In [[quantum mechanics]], the _Kochen-Specker theorem_ -- developed in 1967 by [[Simon Kochen]] and [[Ernst Specker]] -- is a [[no-go theorem]] that places limits on the types of [[hidden variable theories]] that may be used to explain the apparent randomness of quantum mechanics in a causal way.  It roughly asserts that it is impossible to assign values to all physical quantities while simultaneously preserving the functional relations between them.  It is a complement to [[Bell's theorem]], developed by [[John Bell]] in 1964, and is related to [[Gleason's theorem]], developed in 1957 by Andrew Gleason (who incidentally is the person who communicated the original Kochen-Specker paper to the _Journal of Mathematics and Mechanics_ ).  Christopher Isham has recently shown that the Kochen-Specker theorem is equivalent to the statement that the spectral [[presheaf]] has no global elements.

## Kochen-Specker theorem

Let $\mathbb{H}$ be a separable complex Hilbert space and $\Sigma$ be a collection of observables.  We define $\mu: \Sigma \to \mathbb{R}$ to be a map that assigns a definite value to an observable.  Consider the following two "properties" of $\mu$: 

* Property 1: The values of the observables are well-determined at any time, i.e. $\mu$ is a total map. 

* Property 2: If $U_{0}, U_{1}, U_{2} \in \Sigma$ are compatible then, $U_{2} = U_{0} + U_{1} \longrightarrow \mu(U_{2}) = \mu(U_{0}) + \mu(U_{1})$ (the **sum rule**) and $U_{2} = U_{0}U_{1} \longrightarrow \mu(U_{2}) = \mu(U_{0})\mu(U_{1})$ (the **product rule**).

**Theorem** _Let $\mathbb{H}$ be a separable Hilbert space of dimension at least 3.  Then there exists a collection of observables $\Sigma$ such that Properties 1 and 2 cannot hold simultaneously._

+--{: .query}
[[Ian Durham]]: Should I have worded this more in line with how Isham presents it in the classical sense so we have more continuity with the next section?
=--

## Sheaf-theoretic interpretation

Isham has shown that the Kochen-Specker theorem is equivalent to the statement that there the spectral presheaf has no global elements.

## References

The original Kochen-Specker paper:

* S. Kochen and E.P. Specker, "The problem of hidden variables in quantum mechanics," Journal of Mathematics and Mechanics, [pdf](http://www.iumj.indiana.edu/IUMJ/dfulltext.php?year=1968&volume=17&artid=17004).

The original paper outlining Bell's theorem:

* J. S. Bell, "On the Einstein Podolsky Rosen Paradox," Physics, [pdf](http://www.drchinese.com/David/Bell_Compact.pdf).

The original paper outlining Gleason's theorem:

* A.M. Gleason "Measures on the closed subspaces of a Hilbert space," Journal of Mathematics and Mechanics, [pdf](http://www.iumj.indiana.edu/IUMJ/FULLTEXT/1957/6/56050).

## Discussion