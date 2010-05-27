category: physics

****
_This is a stub._

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

In [[quantum mechanics]], the _Kochen-Specker theorem_ -- developed in 1967 by [[Simon Kochen]] and [[Ernst Specker]] -- is a [[no-go theorem]] that places limits on the types of [[hidden variable theories]] that may be used to explain the apparent randomness of quantum mechanics in a causal way.  It roughly asserts that it is impossible to assign values to all physical quantities while simultaneously preserving the functional relations between them.  It is a complement to [[Bell's theorem]], developed by [[John Bell]] in 1964, and is related to [[Gleason's theorem]], developed in 1957 by Andrew Gleason (who incidentally is the person who communicated the original Kochen-Specker paper to the _Journal of Mathematics and Mechanics_ ).  Christopher Isham has recently shown that the Kochen-Specker theorem is equivalent to the statement that the spectral [[presheaf]] has no global elements.

## Kochen-Specker theorem

+-- {: .un_defn}
###### Definition

Let _A_ be a physical quantity represented by a self-adjoint operator $\hat{A}$ on the Hilbert space $\mathcal{H}$ of the system.  A**valuation** is defined to be a real-valued function $\lambda$ on the set of all bounded, self-adjoint operators.  This function has the following two properties:

1. the value $\lambda(\hat{A})$ belongs to the spectrum of $\hat{A}$; and

2. the [[functional composition principle]] (FUNC) holds, i.e. $\lambda(\hat{B})=h(\lambda(\hat{A}))$, for any pair of self-adjoint operators $\hat{A}$, $\hat{B}$ such that $\hat{B}=h(\hat{A})$ for some real-valued function, _h_.

=--

Note that is $\hat{A}_{1}$ and $\hat{A}_{2}$ commute, it follows from the spectral theorem that there exists an operator $\hat{C}$ and functions $h_{1}$ and $h_{2}$ such that $\hat{A}_{1}=h_{1}(\hat{C})$ and $\hat{A}_{2}=h_{2}(\hat{C})$.  It follows from FUNC that

$$
  \lambda(\hat{A}_{1} + \hat{A}_{2}) = \lambda(\hat{A}_{1}) + \lambda(\hat{A}_{2})
$$

and

$$
  \lambda(\hat{A}_{1}\hat{A}_{2})=\lambda(\hat{A}_{1})\lambda(\hat{A}_{2}).
$$

+-- {: .un_theorem}
###### Kochen-Specker theorem 

No valuations exist if dim($\mathcal{H}$)>2.

=--

### Consequences

If a valuation _did_ exist and was restricted to a commutative sub-algebra of operators, it would be an element of the [[spectrum]] of the algebra.  Since such elements _do_ exist, valuations must exist on any commutative sub-algebra of operator but not on the _non_-commutative algebra, $\mathcal{B}(\mathcal{H})$, of all bounded operators.  Isham calls these valuations _local_.

## Sheaf-theoretic interpretation

Isham has shown that the Kochen-Specker theorem is equivalent to the statement that the spectral presheaf has no global elements.

## Contextuality

## References

The original Kochen-Specker paper:

* S. Kochen and E.P. Specker, "The problem of hidden variables in quantum mechanics," Journal of Mathematics and Mechanics, [pdf](http://www.iumj.indiana.edu/IUMJ/dfulltext.php?year=1968&volume=17&artid=17004).

The original paper outlining Bell's theorem:

* J. S. Bell, "On the Einstein Podolsky Rosen Paradox," Physics, [pdf](http://www.drchinese.com/David/Bell_Compact.pdf).

The original paper outlining Gleason's theorem:

* A.M. Gleason "Measures on the closed subspaces of a Hilbert space," Journal of Mathematics and Mechanics, [pdf](http://www.iumj.indiana.edu/IUMJ/FULLTEXT/1957/6/56050).

## Discussion